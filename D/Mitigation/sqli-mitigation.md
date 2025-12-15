
## Issue: SQL Injection Risk

SQL Injection vulnerabilities occur when user input is directly
concatenated into SQL queries without proper validation or parameterization.
This can allow attackers to manipulate database queries.

**Although no SQL Injection vulnerability was detected during testing,
secure coding practices are required to prevent future risk.**

---

## Recommended Fix

- Use prepared statements (parameterized queries)
- Avoid dynamic SQL query construction using string concatenation
- Use ORM frameworks where possible
- Apply least-privilege access to database accounts
- Validate and sanitize user inputs at server side

Example (Parameterized Query):

SELECT * FROM users WHERE username = ? AND password = ?

---

## Reference

OWASP Top 10:
- A03:2021 – Injection

OWASP Cheat Sheet:
- SQL Injection Prevention Cheat Sheet
