# Weekly security review

A reviewer named `security`, which reads everything merged into a
repository in the last week and reports what makes the system easier to
attack. It finds nothing in most weeks and says so.

It is run by an agent in a checkout of the repository, so the server's
worker needs a runner: `REVIEW_RUNNER` in the worker's settings.
`security/reviewer.md` is the agent's instructions.
