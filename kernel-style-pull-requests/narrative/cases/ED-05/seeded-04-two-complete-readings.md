title: Compare the records with the journal before the sweep
expect: VOICE-28
grade: fail
commit: Compare the records with the journal before the sweep
file: src/journal/sweep.py +2 -0
---
The sweep removed a record the journal still held.
=== patch src/journal/sweep.py
@@ -30,3 +30,5 @@ class Sweep:
     def run(self) -> None:
+        # Check records match the journal before the sweep.
+        self._compare()
         self._remove_stale()
