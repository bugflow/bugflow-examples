title: Declare deploy-check phony
expect:
commit: Declare deploy-check phony
|
| Every other target in the Makefile is in .PHONY and deploy-check was
| not, so a file of that name in the repository root would stop make
| running it.
|
| Closes C1.17 in cleanup.org.
file: Makefile +1 -1
file: cleanup.org +1 -1
file: index.org +1 -1
---
The cleanup.org line marks this item done in the same change, as AGENTS.md asks of every plan update.
