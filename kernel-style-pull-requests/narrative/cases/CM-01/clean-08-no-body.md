title: Skip drafts in the poller
expect: 
commit: Skip draft pull requests in the poller
---
An open draft is not evaluated until it is marked ready. The commit has a summary and no body, which GIT-3 does not require.
