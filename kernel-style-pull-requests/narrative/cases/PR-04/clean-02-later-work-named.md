title: Record dismissals as journal facts
expect: 
commit: Record a dismiss comment as a journal fact
file: src/bugflow/domain/journal.py +1 -0
file: src/bugflow/usecases/receive_delivery.py +14 -0
---
A comment whose first line is /dismiss, a policy id and a reason is recorded
as a finding.dismissed entry in the journal, with the policy, the reason and
the comment's author.

The summary comment does not list dismissed findings yet, and they still
count for the label; that follows in its own pull request.
=== patch src/bugflow/domain/journal.py
@@ -22,6 +22,7 @@ EventType = Literal[
     "evaluation.completed",
     "judge.invoked",
     "findings.published",
+    "finding.dismissed",
 ]
=== patch src/bugflow/usecases/receive_delivery.py
@@ -118,6 +118,20 @@ class ReceiveDelivery:
         entries = [received_entry(delivery, outcome, occurred_at)]
+        dismissal = parse_dismissal(delivery.comment.body) if delivery.comment else None
+        if dismissal is not None:
+            entries.append(
+                JournalEntry(
+                    event_type="finding.dismissed",
+                    correlation=correlation,
+                    occurred_at=occurred_at,
+                    payload={
+                        "policy_id": dismissal.policy_id,
+                        "reason": dismissal.reason,
+                        "actor": delivery.comment.author,
+                    },
+                )
+            )
         self._journal.append(entries)
