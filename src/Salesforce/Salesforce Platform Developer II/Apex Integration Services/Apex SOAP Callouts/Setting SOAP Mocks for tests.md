1. Implement the WebServiceMock interface. The method doInvoke() returns the response.
2. Use the Test.setMock() method with the following arguments:
	1. WebServiceMock.class - Implemented interface.
	2. Interface instantiation - new instance of the interface implementation.
```
Test.setMock(WebServiceMock.class, new ExampleWebService());
```
