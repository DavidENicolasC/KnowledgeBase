#### Domain Model
> An object model of the domain that incorporates both behavior and data. At it´s worst business logic can be very complex. Rules and logic describe many different cases and slants of behavior, and it´s this complexity that objects were designed to work with.

It's used for:
- **Apex Triggers** - [[CRUD]] operations including undelete, occur on your custom objects as users or tools interact via the Standard Salesforce UIs or one of the platform APIs. Operations are routed to the appropiate Domain class code corresponding to that object and operation.
- **Apex Services** - Service Layer code should be easy to identify and make it easy to reuse code relating to one or more of the objects that each of its operations interacts via Domain classes. Keeps the code in the Service layer focused on orchestrating whatever business process or task it is exposing.