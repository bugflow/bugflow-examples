title: Count dropped retries against the quota
expect: VOICE-28
commit: Count dropped retries against the quota
|
| Retries the judge drops count against the quota. Only a retry that
| reached the model was counted before.
---
A run of timeouts spent nothing and was never stopped.
