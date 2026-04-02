* **Naming conventions** - Ensure they are expressed in general terms of the application or task rather than relating to specific client caller.

* **Platform / Caller sympathy** - Design methods that support platform's best practices, specially bulkification.

* **SOC Considerations** - Service layer code encapsules task or process logic using multiple objects in your application, as an orchestrator. Code relating to validation, field values or calculations on CRUD operations, os the concern of the related object. Is typically written in Apex triggers and can remain there.

* **Security** - Service Layer code should by default run with user security specified, using `with sharing` modifier on Apex service classes. If need to access to records outside of the user's visibility, a good approach is use a private Apex inner class with `without sharing` modifier.

* **Marshalling** - Avoid prescribing how aspects of interacting with the service layer are handled cause certain aspects are better left to the callers of your service. Often they have their own means to interpret and handle these, like <apex:pagemessages>, chatter posts, or logs. Alternatively, you can provide partial database update feedback.

* **Compound services** - Create compound services that internally group multiple service calls together in one service call, rather than execute multiple service calls one after another. You also should give the callers the option to use a more specific single service if needed.

* **Transaction management and statelessness** - Encapsulate database operations and service state within the method call to the service layer, making stateless to give calling contests the flexibility to employ their own state management solutions. Its scope should also be contained within each service method to avoid caller have to consider this with its own SavePoints, like [[Using SavePoints to avoid partial database updates]].

* **Configuration** - Leave common configuration or options to behavioral overrides in a service layer, as control not to commit changes or send emails. Might be useful when the client is implementing preview or what-if-type functionality.