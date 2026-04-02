## Bulkification
Has bearing on the [[About Domain Layer]]´s design guidelines to ensure that domain class constructors, parameters, methods, and properties deal with data in terms of lists and not singular instances. Helps promote and thus propagate further down the layers, this critical best practice more visibly. After all, there is no point in having a bulkified service if the rest of your application code does not support it.
## Extension by containment
Domain logic must encapsulate both data and behavior. Apex represents data as sObject classes. You can´t extend an sObject class, but you can wrap it or contain it with another class that complements data with appropiate behavioral code (method, properties and so on).
## Naming conventions
Domain data is a data set or list per the bulkification convention, your domain class ideally reflects this in its name, for example, `public class Invoices`.
## Object-oriented programming
One custom object cannot extend another in the same way classes do in OOP languages such as Java. Often end up creating a number of custom objects that share similar aspects, sets of fields, and relationships. When defining your domain classes for such objects, consider using inheritance or interfaces to abstract common behavioral aspects into a shared base class or interface, allowing you to create and reuse logic that applies across such objects.
## Security
Use `with sharing`, `without sharing`, `inherited sharing` keywords on Domain Apex classes to specify whether sharing rules must be enforced. Typically, this is the Service class logic that, per its design guidelines, ,must specify with sharing to enforce sharing rules.

## [[Separation of Concerns (SOC)]]
Be consistent regarding where common types of domain logic, such as validation, defaulting, and calculations go. While it is possible to mix this in with other Domain logic solely related to database and trigger events, you have the option to split this logic across different methods in the Domain class. Consider if it is useful to expose this code to make it accessible in contexts not driven by database operations, such as services that provide validation or defaulting-only behavior.