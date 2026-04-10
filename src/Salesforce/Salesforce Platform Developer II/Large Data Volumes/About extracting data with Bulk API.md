Queries are split into 100,000 record chunks default - you can use chunkSize header field up to 250,000 or less.
```
chunkSize=30000
```

Recommend use [[PK Chunking]] for querying tables with more than 10 million records.