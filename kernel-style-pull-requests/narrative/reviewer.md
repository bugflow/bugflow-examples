agent_id: narrative
summary: What a change says about itself: its description, its commits, its scope
runner: judge
governs: yes
policies: CM-01, CM-02, ED-01, ED-02, ED-03, ED-04, ED-05, PR-04, SC-01, SC-02
checks: em-dash ED-04 VOICE-21
---

The narrative reviewer reads what a pull request says about itself: its
title, its description, its commit messages and the list of files it
changes. It does not review code for correctness. Two policies are also
shown the patches: PR-04 compares the description with them, and ED-05
reads the comments and docstrings they add.

Each file in `policies/` is one policy. A model judges the pull request
against that policy's instructions and the clauses of `doctrine/` its
header names. ED-04 has no file: the `checks` line gives it to the
server's em dash check, which runs without a model and cites VOICE-21.

`governs: yes` means this reviewer's verdict decides the label a pull
request is given.
