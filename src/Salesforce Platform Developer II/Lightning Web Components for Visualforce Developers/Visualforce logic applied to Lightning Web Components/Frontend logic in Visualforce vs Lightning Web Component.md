## Properties
The properties track the page state.

Visualforce: Properties are defined in an Apex Controller and referenced in the page markup

Lightning Web Component: Properties are defined in the component´s Javascript file and referenced in the page markup (HTML).

A getter (method preceeded by the get keyword) executes logic when a property is read.
A setter (method preceeded by the set keyword) executes logic when a property is written to.

## Conditional rendering
Visualforce: rendered attribute.
Lightning Web Component: lwc:if and lwc:else template directives.

## Rendering lists
Visualforce: <apex:repeat>
Lightning Web Component: for:each and iterator:iteratorName

## Executing Javascript logic
Visualforce: You bind the Javascript logic to the onclick attribute of the button.
Lightning Web Component: The method must be bound to the event in the HTML code, like onclick. You can use the event object to access to state or data carried by the event.

## Composition
Visualforce: Use tags such as <apex:component> and <apex:include>. Passing information from and included Visualforce page is easily handled by the <apex:attribute> tag. Information backup to the page involves more complex patterns, like hierarchies of Apex controllers.

Lightning Web Components:
Use public properties and public method to pass information from a parent component down to a child component.
Dispatch a standard DOM event or a custom event from the Javascript to pass information from the child up to its parent component.
You can include a child component under a parent component. Use the kebab cases preceded by its namespace. The namespace for custom components (Default): c, and the namespace for base components: lightning.