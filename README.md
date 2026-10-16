# Bugflow examples

Policies a [Bugflow](https://github.com/bugflow/bugflow) server can
review with. Each directory is one example, laid out as a policy
repository, and its README says what it reviews.

To use one, copy its directory into a repository of your own, name your
repositories in `declarations.toml`, and send it to your server:

    bugflow deploy-policies . --repository OWNER/NAME --commit SHA --api URL

Add `--check` to have the server report every problem and store nothing.
The Bugflow repository's `docs/deploying.md` says how a pipeline does
this on each merge.

## Licence

This repository is free software under the GNU General Public License,
version 3 or any later version. The text is in `COPYING`.
