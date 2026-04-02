Define your class as global, and define methods as global static. Add the following annotations:

1. @RestResource(urlMapping='/OBJECT') for the class, where OBJECT is the Salesforce to be modified.
2. @HttpGet - for the GET methods. You can use other [[Common HTTP annotations for Apex Web Services]].

The urlMapping is appended to the base endpoint https://MyDomain.my.salesforce.com/services/apexrest/ to form the endpoint for your REST service. Is case sensitive and can contain (*) character.