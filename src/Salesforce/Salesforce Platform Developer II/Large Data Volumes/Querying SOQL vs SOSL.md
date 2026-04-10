SOQL query child-to-parent relationships which are often many-to-one, and to query parent-to-child relationships, which are one to many.

SOSL can tokenize multiple terms within a field, and can build a search index off of this.

Limitations:
- Limit for multiple SOSL searches in a single transaction is 20. Maximum records returned by each of the one is 2,000
- If only there is a single SOSL search in a single transaction, can return 40,000 records. With a SOQL search in the same transaction, can return 50,000 records.