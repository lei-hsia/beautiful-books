## How to intuitively understand Q,K,V of Self Attention in Transformers (BERT) ?

This is inspired by KV Cache acceleration in vLLM

- Q: Query
- K: Key
- V: Value

Old days: in database: have a Query in mind to query the DB; DB use Q to check against (K,V); if Key is similar to Query then you can unlock some specific (K,V)

In other words, Dot-Product (cosine similarity) yields high similarity, then we unlock Values

This is exactly what's QKV in the famous paper "Attention is all you need"

