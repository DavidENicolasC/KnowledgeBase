1. Add the data in a CSV file.
2. Create a Static Resource for this file.
3. Call Test.loadData within your test method and passing it the sObject type token and the static resource name.
```
	List<sObject> lstData = Test.loadData(Account.sObjectType, 'ResourceName');
```
The resource will be assigned to one of the [[Supported MIME Types]].