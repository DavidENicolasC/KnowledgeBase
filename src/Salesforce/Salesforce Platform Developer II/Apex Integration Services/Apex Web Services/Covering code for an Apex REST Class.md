For methods that don´t take parameters or that rely on information in the REST request, create a test REST request. Add the request for the method as follows:

```
RestRequest request = new RestRequest();
request.requestUri = 'https://MyDomain.my.salesforce.com/services/apexrest/OBJECT/' + recordId;
request.httpMethod = 'GET';
request.params.put('status', 'Working');

//We assign the request to RestContext when we are accessing to the request values.
RestContext.request = request;
```

For all others, just call the methods by passing in parameter values and verifying results.