title: Keep the poll window after a failure
expect: VOICE-11
grade: warn
---
So what happens when the ingress is down? The poller keeps its time window
and posts the same deliveries on the next poll.
