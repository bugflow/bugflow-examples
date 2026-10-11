title: Bound the delivery queue
expect:
commit: Bound the delivery queue
|
| While the worker polls, the queue fills, and a queue that nothing
| bounds grows until the ingress is killed for the memory it holds. The
| queue now holds at most 500 deliveries.
---
The ingress answers 503 when the queue is full.
