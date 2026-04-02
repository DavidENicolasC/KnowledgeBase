Use Bulk and batch Apex.
Bulk can query results larger than 100K records.
For manipulate data, batch is a better option. You can trigger additional Apex Batch jobs in the finish() call.