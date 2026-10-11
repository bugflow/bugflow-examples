title: Fail closed on a missing secret
expect: 
commit: Fail closed when the webhook secret is unset
---
The ingress refuses to start without a secret rather than accepting deliveries it cannot verify.
