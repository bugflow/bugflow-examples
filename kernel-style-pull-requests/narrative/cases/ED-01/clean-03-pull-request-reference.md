title: Publish internal stack ports on 127.0.0.1 only
expect: 
---
Follows #27, which added the secret scanner.

Postgres, the Temporal server and the Temporal UI published their ports on
every interface, and none of them authenticates beyond the local Postgres
password. They now publish on 127.0.0.1. The ingress still publishes on every
interface, because the forge has to reach it.
