# ShadowInject Lab – Final Security Assessment Report

## Project Overview
ShadowInject is a hands-on web application security lab focused on
automated scanning, manual validation, and mitigation planning
using OWASP ZAP and WebGoat.

---

## Scope
- Target Application: WebGoat (Local)
- Tools Used: OWASP ZAP
- Testing Type:
  - Automated scanning
  - Manual validation
  - Mitigation analysis

---

## Phase Summary

### Phase 1 – Setup
- Installed and configured WebGoat
- Installed and configured OWASP ZAP
- Verified proxy interception

---

### Phase 2 – Automated Scanning
- Application mapping completed
- Spidering and passive scanning performed
- Active scanning executed
- Security misconfigurations identified

Key Findings:
- Missing Anti-CSRF tokens
- Missing security headers (CSP, X-Frame-Options)
- No SQL Injection detected
- No XSS detected

---

### Phase 3 – Manual Validation
- Manually verified CSRF vulnerability
- Tested SQL Injection manually (not exploitable)
- Tested XSS manually (not exploitable)

---

### Phase 4 – Mitigation & Secure Design
- CSRF mitigation documented
- SQL Injection prevention strategies documented
- XSS prevention strategies documented
- OWASP Top 10 aligned recommendations provided

---

## Conclusion
This project demonstrates a complete web security assessment workflow
from discovery to validation and mitigation. The lab reflects realistic
pentesting methodology and defensive security practices.

---

## Disclaimer
This project was conducted on an intentionally vulnerable application
for educational purposes only.
