title: Say plainly what the quota counts
expect:
commit: Say plainly what the quota counts
file: src/judge/quota.py +1 -1
---
The comment read as "retries the judge" before it read as intended.
=== patch src/judge/quota.py
@@ -42,3 +42,3 @@ class Quota:
-        # Retries the judge drops count against the quota.
+        # The retries that the judge drops count against the quota.
         if call.reached_model or call.dropped:
