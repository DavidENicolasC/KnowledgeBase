This can provide standard hooks to implement common domain logic for validation of records via a onValidate() method and defaulting field values via a onApplyDefaults() method.

You can also provide methods for create a new instance of the trigger handler logic for a domain class and passes in the sObject list, as Trigger.new.

```
public override void onApplyDefaults() {
    // Apply defaults to Opportunities
    for(Opportunity opportunity : (List<Opportunity>) Records) {
        if(opportunity.DiscountType__c == null) {
            opportunity.DiscountType__c = OpportunitySettings__c.getInstance().DiscountType__c;
        }               
    }
}
```

```
public override void onValidate() {
    // Validate Opportunities
    for(Opportunity opp : (List<Opportunity>) this.records) {
        if(opp.Type.startsWith('Existing') && opp.AccountId == null) {
            opp.AccountId.addError('You must provide an Account when ' +
                'creating Opportunities for existing Customers.');
        }
    }
}
```

```
public override void onValidate(Map<Id,SObject> existingRecords) {
    // Validate changes to Opportunities
    for(Opportunity opp : (List<Opportunity>) Records) {
        Opportunity existingOpp = (Opportunity) existingRecords.get(opp.Id);
        if(opp.Type != existingOpp.Type) {
            opp.Type.addError('You cannot change the Opportunity type once it has been created');
        }
    }
}
```

```
public override void onAfterInsert() {
    // Related Accounts
    List<Id> accountIds = new List<Id>();
    for(Opportunity opp : (List<Opportunity>) Records) {
        if(opp.AccountId!=null) {
            accountIds.add(opp.AccountId);
        }
    }
    // Update last Opportunity activity on related Accounts via the Accounts domain class
    fflib_SObjectUnitOfWork uow =
      new fflib_SObjectUnitOfWork(
        new Schema.SObjectType[] { Account.SObjectType });
    Accounts accounts = new Accounts([select Id from Account
      where id in :accountIds]);
    accounts.updateOpportunityActivity(uow);
    uow.commitWork();              
}
```