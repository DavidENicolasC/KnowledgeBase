PK for Primary Key (object's record Id). Splits bulk queries on very large tables into chuncks based on the record Ids.

To get enabled, specify the header Sforce-Enable-PKChunking on the hob request for the Bulk API query.
```
Sforce-Enable-PKChunking: chunkSize=50000
```

Results must be downloaded separately for each chunk.

Each chunk is processed as a separate batch that counts toward your daily batch limit.

When a query is successfully chunked, original batch's status shows as NOT_PROCESED.

Supports custom objects.

Supported Standard objects:
* Account
* Campaing
* CampaingMember
* Case
* Contact
* Lead
* LoginHistory
* Opportunity
* Task
* User