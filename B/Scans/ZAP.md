# ShadowInject – Phase 2: Automated Scanning with OWASP ZAP

## Target
- Application: WebGoat (Local)
- URL: http://127.0.0.1:8080/WebGoat
- Tool: OWASP ZAP
- Mode: Standard Mode
- Scan Type: Mapping → Spidering → Passive Scan → Active Scan

---

## STEP 1 — Mapping WebGoat with ZAP

### Action Performed
- Manually browsed WebGoat using Firefox for 1–2 minutes
- Visited:
  - Login page
  - Register page
  - Injection lesson
  - Multiple sidebar links

### Objective
Allow ZAP to observe site structure and populate the Sites tree.

### Evidence
<img width="951" height="542" alt="mapping 1" src="https://github.com/user-attachments/assets/22eb78bc-f26d-469b-ad91-14efed90810b" />


---

## STEP 2 — Spidering (Automatic Crawling)

### Action Performed
- Initiated Spider from ZAP against the WebGoat application
- Allowed crawler to discover URLs automatically

### Objective
Discover hidden paths and endpoints not manually visited.

### Evidence
<img width="950" height="893" alt="Spidering (Automatic Crawling)" src="https://github.com/user-attachments/assets/074c17eb-1064-42f4-8694-3bbfb7d55fea" />


---

## STEP 3 — Passive Scanning

### Action Performed
- Browsed application traffic through ZAP proxy
- Allowed passive scanners to analyze responses

### Objective
Identify vulnerabilities without modifying requests.

### Evidence
<img width="952" height="901" alt="Passive Scanning" src="https://github.com/user-attachments/assets/67dbe43c-9e71-485d-bf35-96bc3b405b55" />


---

## STEP 4 — Active Scanning

### Action Performed
- Initiated Active Scan on WebGoat target
- ZAP attempted common attack vectors:
  - SQL Injection
  - XSS
  - CSRF
  - Path traversal
  - Header misconfigurations

### Objective
Actively test application for known vulnerabilities.

### Evidence

<img width="950" height="988" alt="zap_automated_scan" src="https://github.com/user-attachments/assets/b1d5aa9d-ffff-44fb-83e0-573d2042ec54" />


---

## STEP 5 — Findings & Alerts Review

### Overview
<img width="941" height="862" alt="zap_alerts_overview" src="https://github.com/user-attachments/assets/a9a68472-fca8-4869-acc9-c49767d4b2b8" />


### Key Findings Identified

#### 1. Absence of Anti-CSRF Tokens
<img width="553" height="867" alt="zap_csrf_alert" src="https://github.com/user-attachments/assets/9a3e4704-cdef-43e4-9199-c2c0b0850a6e" />


#### 2. Content Security Policy (CSP) Header Not Set
<img width="552" height="898" alt="zap_csp_alert" src="https://github.com/user-attachments/assets/f118114a-cf5b-4b34-8992-d7146b94db59" />


#### 3. Missing Anti-clickjacking Header
<img width="563" height="917" alt="zap_clickjacking_alert" src="https://github.com/user-attachments/assets/7b24c124-77d6-442a-9278-838bdcc8bc84" />


---

## Scan Summary

- No SQL Injection detected
- No XSS detected
- CSRF protection missing on authentication endpoints
- Multiple security headers missing
- Informational findings present (user-agent fuzzing)

---

## Notes
- WebGoat is an intentionally vulnerable application
- Findings align with OWASP Top 10 categories
- Full automated scan report exported separately

### Full Report




