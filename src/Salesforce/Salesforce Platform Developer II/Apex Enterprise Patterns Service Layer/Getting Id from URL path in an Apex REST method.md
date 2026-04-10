After [[Exposing a class as a REST web service]], In your URL mapping you must have something like:
```
'OBJECT/*/operation'
```

Here, `*` is referencing to the record Id. Then, you can extract the Id from the request context, like follows:
```
Id caseId;
RestRequest request = RestContext.request;
List<String> URIParts = request.requestURI.split('/');
caseId = URIParts[2];
```