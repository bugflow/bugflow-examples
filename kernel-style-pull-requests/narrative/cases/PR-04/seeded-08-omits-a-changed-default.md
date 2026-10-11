title: Make the poll interval a setting
expect: GIT-5
grade: warn
commit: Make the poll interval a setting
file: src/bugflow/app/poller.py +3 -1
---
The poller reads POLL_INTERVAL from the environment, so a laptop can poll
less often than the stack does.
=== patch src/bugflow/app/poller.py
@@ -10,3 +10,5 @@
-INTERVAL = 30.0
+DEFAULT_INTERVAL = 300.0
+
+INTERVAL = float(os.environ.get("POLL_INTERVAL", DEFAULT_INTERVAL))
