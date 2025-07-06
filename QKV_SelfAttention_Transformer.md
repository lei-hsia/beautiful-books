## How to intuitively understand Q,K,V of Self Attention in Transformers (BERT) ?

This is inspired by KV Cache acceleration in vLLM

- Q: Query
- K: Key
- V: Value

Old days: in database: have a Query in mind to query the DB; DB use Q to check against (K,V); if Key is similar to Query then you can unlock some specific (K,V)

In other words, Dot-Product (cosine similarity) yields high similarity, then we unlock Values

This is exactly what's QKV in the famous paper "Attention is all you need"

#### QKV examples
![QKV examples](https://github.com/lei-hsia/beautiful-books/blob/master/qkv1.png)

#### How QKV is used in Attention paper
![How QKV is used in Attention paper](https://github.com/lei-hsia/beautiful-books/blob/master/qkv2.png)

#### How MHA is used and QKV calculations can be parallelized
![How MHA is used and QKV calculations can be parallelized](https://github.com/lei-hsia/beautiful-books/blob/master/qkv3.png)


The reason I reviewed these params is that this is the foundation how they are used and accelerated via KV Cache in [vLLM](https://github.com/vllm-project/vllm)
