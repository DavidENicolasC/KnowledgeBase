It´s good to keep the logic minimal in Trigger. Apex Triggers are not classes and have limited means for factoring code or using OO principles like [[Inheritance]].

Example:
```
trigger OpportunitiesTrigger on Opportunity (
  after delete, after insert, after update, after undelete, before delete, before insert, before update) {
   // Creates Domain class instance and calls appropriate methods
   fflib_SObjectDomain.triggerHandler(Opportunities.class);
}
```