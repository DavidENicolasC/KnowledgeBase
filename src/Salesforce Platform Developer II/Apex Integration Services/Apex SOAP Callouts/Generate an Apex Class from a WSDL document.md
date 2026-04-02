1. From Setup, enter `Apex Classes` in the Quick Find box, then click **Apex Classes**.  
2. Click **Generate from WSDL**.  
3. Click **Choose File** and select the downloaded WSDL file.  
4. Click **Parse WSDL**. The application generates a default class name for each namespace in the WSDL document and reports any errors.
5. Click **Generate Apex code**. The final page of the wizard shows the generated classes, along with any errors. The page also provides a link to view successfully generated code.

Two classes are generated for both synchronous and asynchronous callouts. The generated classes always have a method with the ImplPort suffix.

The methods call to WebServiceCallout.invoke(), which performs the callout to the external service.

You can cover this code by [[Setting SOAP Mocks for tests]]
