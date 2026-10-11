title: Load the fixtures before the migration runs
expect: VOICE-28
grade: fail
commit: Test fixtures load before the migration
---
The migration read a table the fixtures had not yet filled.
