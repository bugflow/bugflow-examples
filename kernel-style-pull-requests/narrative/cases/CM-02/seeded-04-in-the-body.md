title: Bound the delivery queue
expect: VOICE-28
grade: warn
commit: Bound the delivery queue
|
| While the worker polls the queue fills. The queue now holds at most
| 500 deliveries.
---
The ingress answers 503 when the queue is full.
