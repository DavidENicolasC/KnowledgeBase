```
public class Opportunities extends fflib_SObjectDomain {
    public Opportunities(List<Opportunity> sObjectList) {
        super(sObjectList);
    }
    public class Constructor implements fflib_SObjectDomain.IConstructable {
        public fflib_SObjectDomain construct(List<SObject> sObjectList) {
            return new Opportunities(sObjectList);
        }
    }
}
```

```
public class Accounts extends fflib_SObjectDomain {
    public Accounts(List<Account> sObjectList) {
        super(sObjectList);
    }
    public void updateOpportunityActivity(fflib_SObjectUnitOfWork uow) {
        for(Account account : (List<Account>) Records) {
            account.Description = 'Last Opportunity Raised ' + System.today();
            uow.registerDirty(account);
        }
    }
}
```