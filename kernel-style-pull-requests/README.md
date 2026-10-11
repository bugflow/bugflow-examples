# Kernel-style pull requests

A reviewer named `narrative`, which reads what a pull request says about
itself and judges it against a doctrine of plain prose, Linux kernel
commit messages and one reason for each change.

`narrative/doctrine/` holds the rules, `narrative/policies/` holds what a
model is asked about them, and `narrative/cases/` holds the example pull
requests each policy was measured against. `pace-layers.toml` runs the
review whenever a pull request changes.

The cases are pull requests of the Bugflow project, so they name its
files.
