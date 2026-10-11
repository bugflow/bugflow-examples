title: Count dropped retries against the quota
expect:
commit: Count dropped retries against the quota
file: src/judge/quota.py +3 -1
---
A retry the judge drops now counts against the quota.
=== patch src/judge/quota.py
@@ -41,5 +41,7 @@ class Quota:
     def spend(self, call: Call) -> None:
-        if call.reached_model:
+        # A dropped retry counts against the quota, and so does a retry
+        # that reached the model.
+        if call.reached_model or call.dropped:
             self._used += call.cost
