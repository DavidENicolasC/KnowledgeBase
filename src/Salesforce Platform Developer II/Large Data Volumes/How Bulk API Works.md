The records are streamned to create a new job. It's stored in temporary storage and then sliced up into user-defined batches (10,000 records max.)

Batches are processed in parallel or serially depending on your needs. Work from the client application to the server. Logs the status of each job and tries to reprocess failed records automatically. If a job times out, automatically puts it back in the queue.

Each batch is processed independently.