title: Let bugflow replay read its default doctrine
expect: VOICE-19
grade: warn
---
Found by the whole-repository stocktake. Nothing tested the command with its own defaults, which is how `make replay` calls it; the new test does, from the repository root.
