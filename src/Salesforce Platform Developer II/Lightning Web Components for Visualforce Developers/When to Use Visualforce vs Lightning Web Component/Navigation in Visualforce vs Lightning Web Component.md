Visualforce: URLFOR function with <apex:commandButton> and <apex:commandLink> tags to navigate inside or outside of Salesforce. Apex methods returns PageReferences.

Lightning Web Component: Use Lightning Navigation Service.
1. Import lightning/navigation Javascript module into the Lightning web component.
2. Make the Lightning web component´s class extend NavigationMixin
3. Call the Navigate method, passing the page reference of the page you want to navigate to.
This also generate URLs, navigate to a page reference, work with URL parameters, and open files. Support page reference types as App, Lightning Component, Navigation Item (tab) and Record Page. Uses meaningful PageReference objects to perform navigation. If Salesforce changes a specific URL, code that links to it doesn´t break. This way, eliminates hardcoded URLs. The mixin is a special Javascript class.