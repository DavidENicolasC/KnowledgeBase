Can retrieve up to 15 GB of data, divided into fifteen up to 1 GB files.

Supports both query and queryAll operations.
queryAll returns deleted records because of a merge or delete. Also returns information about archived Task and Event records.

When adding a batch to a bulk query job:
* Content-Type in header must be:
	- text/csv
	- application/xml
	- application/json
* SOQL statement supplied for the batch is in plain text format

If the query doesn´t execute within the standard two-minute timeout limit, the job fails and a QUERY-TIMEOUT error is returned. You can rewrite a simpler query and resubmit the batch.

Salesforce attempts to retrieve results. If exceed 1 GB file size limit or take longer than 5 minutes to retrieve, completed results are cached and another attempt is made. After 30 attempts, job fails and the error message **Retried more than thirty times** is returned. When happens, consider using the PK Chunking header to split the query results into smaller chunks. When succeed, results are returned and stored for seven days.