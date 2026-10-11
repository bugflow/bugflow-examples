title: Bring cleanup.org and todo.org up to date
expect:
commit: Bring cleanup.org and todo.org up to date
|
| The owner answered eight questions on 2026-09-24, and an audit checked
| every open cleanup item against master. cleanup.org records each answer
| where it was asked and the items it opens or closes: the judge is
| fingerprinted by its rendered probe requests (C1.2, C1.18); CODE-4 gains
| a carve-out for what the platform contract mandates (C3.1, C3.12), which
| cancels two findings that were wrong (C3.2, C3.3) and the two that
| waited on them; the worktree chain is retired, pending a confirmation
| the audit raised (C4.2); the engine code is wired now (C4.7 to C4.11);
| and grounding and canon are specified in index.org (C6.18). Four items
| are marked partly done by commits since the stocktake, and eleven items
| whose text the audit found misleading are corrected.
|
| todo.org gains the plan those answers imply: a section for wiring the
| engine's library, specification first, and under the bars on Haiku the
| calibration cases from 2026-09-24's pull requests, ED-02 capped at warn
| until it meets a bar, and ED-02 tuned first.
file: cleanup.org +135 -20
file: todo.org +57 -0
---
One answer is held back: the owner decided to retire the worktree chain on a briefing that nothing plans a checkout runner, and d2fd0c3, merged since, hardened that code for "the checkout runner in M5". The deletion waits on the owner confirming, which is in their intray.
