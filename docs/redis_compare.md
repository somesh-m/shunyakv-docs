The experiment was conducted using a 1KB value size per key and a total keyspace of 10 million keys. Both systems were evaluated under this configuration to measure throughput and latency characteristics at scale.

|  | Ops | conns | Pipeline | Ops/sec | p50 | p99 | p99.9 |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Shunya KV | SET | 4 | 150 | 14,97,570 | 0.093 | 0.651 | 0.863 |
| Shunya KV | GET | 4 | 150 | 10,71,875 | 0.078 | 0.727 | 1.074 |
| Redis (Standalone) | SET | 4 | 20 | 7,38,124 | 0.863 | 1.039 | 1.159 |
| Redis (Standalone) | GET | 4 | 20 | 8,60,098 | 0.743 | 0.911 | 1.047 |

### Set Comparison Result

* Throughput: ShunyaKV is 2.03× faster
* Median latency: ~9.3× lower
* Tail latency: ~25% tighter

### GET Comparison Result

* Throughput: ShunyaKV is 1.25× faster-
* Median latency: ~9.5× lower
* Tail latency: essentially equal (~1ms)
