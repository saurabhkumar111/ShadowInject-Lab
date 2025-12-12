# 🔧 ShadowInject — Setup Requirements

This project uses an intentionally vulnerable web application and a web security scanner to identify and exploit common vulnerabilities.

## ✅ Tools Required

### 1. **WebGoat**
A deliberately insecure web application used as the target for vulnerability testing.

Download/Run 

- **JAR File:**
  
Download from: https://github.com/WebGoat/WebGoat/releases


java -jar webgoat-server-*.jar

### 2. **OWASP ZAP**

A web application security scanner used to detect and analyze vulnerabilities.

Download:
https://www.zaproxy.org/download/

After installation, use:
**Automated Scan**
**Manual Explore + Proxy Mode**


## 📦 Other Recommended

**Firefox / Chrome (for proxy testing)**

**Burp Suite Community (optional comparison tool)**

**Docker Desktop (if using Docker for WebGoat)**


## ✔ Summary

ShadowInject requires:

**WebGoat** → vulnerable target

**OWASP ZAP** → scanner

**Browser** → routing traffic through ZAP

This setup is  for performing:- SQLi, XSS, CSRF, scanning and exploitation.
