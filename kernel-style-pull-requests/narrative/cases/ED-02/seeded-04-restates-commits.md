title: Skip drafts and bump the interval
expect: VOICE-2
grade: fail
commit: Skip draft pull requests in the poller
commit: Poll every 60 seconds
file: src/bugflow/usecases/poll_pull_requests.py +8 -2
---
There are two commits here. The first skips draft pull requests in the poller. The second polls every 60 seconds.
