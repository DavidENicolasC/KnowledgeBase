Test code save against Salesforce API version 23.0 or earlier access has access to all data in the organization. Apex test methods in API version 24.0 and later can´t access pre-existing data such as standard objects, custom objects, and custom settings data.

Test methods from API version 24.0 or later calling to methods in API version 23.0 or earlier applies their data access restrictions in the called method.

-------
References:
[Isolation of Test Data from Organization Data in Unit Tests](https://developer.salesforce.com/docs/atlas.en-us.apexcode.meta/apexcode/apex_testing_data_access.htm)