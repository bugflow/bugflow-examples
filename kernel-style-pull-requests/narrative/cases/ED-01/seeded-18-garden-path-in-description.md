title: Count dropped retries against the quota
expect: VOICE-28
grade: warn
---
Retries the judge drops count against the quota. Before this change only a
retry that reached the model was counted, so a run of timeouts spent
nothing and was never stopped.
