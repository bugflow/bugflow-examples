title: Stop the poller sending an update twice
expect:
commit: Drop the updates the poller sends twice
---
The poller sent an update again when its acknowledgement was late.
