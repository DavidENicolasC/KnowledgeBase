Custom table that contains a subset of fields from a standard or custom base Salesforce object.

By having narrower rows and less data to scan than the base Salesforce object, skinny tables allows more rows per database to be fetched, increasing throughput when reading from a large object.

Don´t include soft-deleted rows.

Platform automatically synchronizes rows between base object and skinny table, so the data is always kept current.

Platform determines at query runtime when it would make sense to use skinny tables.

Can be created on the following objects:
Custom Objects
Account
Contact
Opportunity
Lead
Case

Can enhance performance for:
- Reports
- List Views
- SOQL