title: Retire the deterministic policies
expect: 
commit: Retire the deterministic policies from the corpus
file: src/bugflow/policy/deterministic.py +0 -266
---
ADR-013 says a mechanical check belongs to the tool that can make it, and ADR-013 is what retires these eight: a hook or a linter decides them, and every repository runs those already.
