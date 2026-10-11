title: Improve the ingress
expect: VOICE-6, VOICE-9, VOICE-19
grade: VOICE-6 fail, VOICE-9 warn, VOICE-19 warn
---
Essentially, this makes the ingress more robust.

I started by rewriting the signature check, then noticed the tests already
covered it, so I reverted that and only changed the logging.
