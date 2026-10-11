title: Count dropped retries against the quota
expect:
---
The retries that the judge drops now count against the quota. Before this
change only a retry that reached the model was counted, so a run of
timeouts spent nothing and was never stopped.
