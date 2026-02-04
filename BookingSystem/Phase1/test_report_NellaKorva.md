# 1️⃣ Introduction

**Tester(s):**  
- Name:  Nella Korva

**Purpose:**  
Identifying vulnerabilities in a booking system using automated testing with ZAP. (AI used to help compile report)

**Scope:**  
- Tested components: Web application hosted at http://10.0.2.15:8001, registration page
- Exclusions:  Backend, Database
- Test approach: Black-box

**Test environment & dates:**  
- Start:  04/02/2026
- End:  04/02/2026
- Test environment details
- Kali Linux (Virtual Machine)
- Web server: Docker container
- Runtime: Not disclosed
- Database: Not disclosed
- Browser: Firefox
- Tools: OWASP ZAP

**Assumptions & constraints:**  
- Deadline

---

# 2️⃣ Executive Summary

OWASP ZAP test identified several high and medium risk vulnerabilities that need attention, with the main risks being SQL injection and Path traversal.

**Overall risk level:** High

**Top 5 immediate actions:**  
1.  Implement server-side input validation, and add a list of allowed characters to eliminate SQL Injection
2.  Validate and sanitize all user-supplied input
3.  Introduce Anti-CSRF tokens
4.  Configure a Content Security Policy (CSP)
5.  Enable Clickjacking protections (frame-ancestors or X-Frame)

---

# 3️⃣ Severity scale & definitions

|  **Severity Level**  | **Description**                                                                                                              | **Recommended Action**           |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
|      🔴 **High**     | A serious vulnerability that can lead to full system compromise or data breach (e.g., SQL Injection, Remote Code Execution). | *Immediate fix required*         |
|     🟠 **Medium**    | A significant issue that may require specific conditions or user interaction (e.g., XSS, CSRF).                              | *Fix ASAP*                       |
|      🟡 **Low**      | A minor issue or configuration weakness (e.g., server version disclosure).                                                   | *Fix soon*                       |
| 🔵 **Info** | No direct risk, but useful for system hardening (e.g., missing security headers).                                            | *Monitor and fix in maintenance* |


---

# 4️⃣ Findings (filled with examples → replace)

> Fill in one row per finding. Focus on clarity and the most important issues.

| ID | Severity | Finding | Description | Evidence / Proof |
|------|-----------|----------|--------------|------------------|
| F-01 | 🔴 High | SQL Injection| The registration endpoint does not properly sanitize user input, leading to unauthorized data access.| ZAP successfully altered query logic using boolean-based payloads |
| F-02 | 🔴 High | Path Traversal| User input allows traversal to files not meant to be accessed| Traversal payloads in POST requests |
| F-03 | 🟠 Medium | Absence of Anti-CSRF Tokens |  A cross-site request forgery is possible due to lack of Anti-CSRF tokens| ZAP detected HTML forms without any recognized Anti-CSRF token. |
| F-04 | 🟠 Medium | Content Security Policy (CSP) Header Not Set |App doesnt implement CSP, which can detect and mitigate XSS and data injection| ZAP detected responses missing the CSP header. |
| F-05 | 🟠 Medium | Missing Anti-clickjacking Header |No protection against 'ClickJacking' attacks.| ZAP detected responses missing X-Frame-Options/frame-ancestors directives |

---

# 5️⃣ OWASP ZAP Test Report (Attachment)


> https://github.com/Mellemy/Cybersecurity/blob/main/BookingSystem/Phase1/zap_report_round1.md

---