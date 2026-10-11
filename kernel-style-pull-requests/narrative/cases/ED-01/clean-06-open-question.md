title: Close pull request workflows when the poller sees a close
expect: 
---
The poller posts `closed` for a pull request closed since its last poll, and
the pull request's workflow ends.

Not settled: whether a pull request reopened with nothing changed should be
evaluated again. Deciding it needs the forge's reopened event, which the
pull request listing does not report.
