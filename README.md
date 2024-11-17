## Stateless Streaming Aggregation

### Explanation

This code processes unbounded streaming data by calculating incremental aggregates without relying on Spark's built-in state store. 

Instead, it uses the foreachBatch API to handle each micro-batch, performing custom upserts through a SQL MERGE statement. 

Aggregated results are updated or inserted into a database, where state tracking is managed externally. 

This approach avoids maintaining in-memory state, making it lightweight, scalable, and suitable for handling unbounded streams efficiently.
