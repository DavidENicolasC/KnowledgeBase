Design pattern that reduces repetitive code when implementing transaction management and the coding overheads of adhering to DML bulkification through extensive use of maps and lists.

>Maintains a list of objects affected by a business transaction and coordinates the writing out of changes and the resolution of concurrency problems.

Handles the following use cases:
* Recording record updates, insert and deletes to implement specific business requeriment.
* Recording record relationships to make inserting child or related records easier with less coding
* When asked to write to database, bulkifies all records captured.
* Wrapping DML performed in SavePoint, freeing the developer from implementing this each time for every service method that is written.

There are some cases for [[When not to use Unit of Work]].