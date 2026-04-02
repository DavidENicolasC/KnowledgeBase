a) When [[Implementing the HTTPCalloutMock interface]], use the following syntax to set the callout Mock:
1. HttpCalloutMock.class - Implemented interface.
2. Interface instantiation - new instance of the interface implementation.
```
Test.setMock(HttpCalloutMock.class, new ExampleCalloutMock());
```

b) When [[Creating a StaticResourceCalloutMock]] to test, use the following syntax to set the callout Mock:
```
Create the mock object.
StaticResourceCalloutMock objMock = new StaticResourceCalloutMock();
objMock.setStaticResource('GetAnimalResource');
objMock.setStatusCode(200);
objMock.setHeader('Content-Type', 'application/json;charset=UTF-8');

// Associate the callout with a mock response.
Test.setMock(HttpCalloutMock.class, objMock);
```
