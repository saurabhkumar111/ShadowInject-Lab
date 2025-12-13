## Issue: Missing Anti-CSRF Protection

The application does not include anti-CSRF tokens in state-changing requests,
making it vulnerable to Cross-Site Request Forgery attacks.



## Recommended Fix

- Implement synchronizer token pattern
- Generate unique CSRF tokens per session
- Validate token on every state-changing request
- Reject requests without valid tokens

Example:
<input type="hidden" name="csrf_token" value="{{random_token}}">



## csrf_mitigation/reference

OWASP Top 10:
- A01:2021 – Broken Access Control

OWASP Cheat Sheet:
- Cross-Site Request Forgery Prevention Cheat Sheet
