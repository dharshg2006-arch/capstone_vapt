# Enterprise Infrastructure Security Architecture Audit
### VAPT Capstone Assessment Portfolio & Engineering Case Study
**Assessor Identity:** Senior Security Consultant (Rabtech Capstone Candidate)  
**Classification:** STRICTLY CONFIDENTIAL / PROPRIETARY SYSTEM DATA  
**Target Environment Baseline:** Isolated Virtual Corporate Subnet Map  

---

## 1. Executive Summary & Assessment Scope
This repository houses the formal verification logs, offensive testing payloads, and the comprehensive, multi-page security report documenting a full Vulnerability Assessment and Penetration Testing (VAPT) exercise. The core focus of this assessment was to systematically scan, uncover, map, and remediate high-risk entry vectors hidden across production authentication pipelines and critical data tiers.

### 1.1 Scope Boundaries Matrix
Our offensive testing framework applied black-box and grey-box threat tactics across three core segments of the enterprise ecosystem:

* **Production Authentication Ingress Gateway:** Audited for input sanitization limits and session token manipulation.
* **Corporate Core Database Server:** Evaluated against raw command injection vectors and unauthorized column reading.
* **Internal Application Routing Daemons:** Tested for legacy component patch management and memory serialization flaws.

### 1.2 Discovered Flaw Scoreboard Summary
- 🔴 **Critical Severity Vulnerabilities Discovered:** 2 Flaws
- 🟠 **High Severity Vulnerabilities Discovered:** 1 Flaw
- 🟡 **Medium Severity Vulnerabilities Discovered:** 1 Flaw

---

## 2. Threat Metric Dashboard & Risk Assessments
All vulnerabilities identified during active mapping scenarios have been scored using the global **Common Vulnerability Scoring System (CVSS v3.1)** quantitative metric criteria and accurately cross-mapped to official **OWASP Top 10 Application Security Risks**.

| Discovered Vulnerability | Threat Tier | Base CVSS 3.1 Vector Code | Target OWASP 2021 Reference |
| :--- | :--- | :--- | :--- |
| **SQL Injection (SQLi)** | 🔴 Critical (9.8) | `CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H` | A03:2021-Injection |
| **Remote Code Execution (RCE)** | 🔴 Critical (9.8) | `CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H` | A06:2021-Vulnerable Components |
| **Broken Object Level Auth (BOLA)** | 🟠 High (8.6) | `CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:L/A:N` | A01:2021-Broken Access Control |
| **Stored Cross-Site Scripting (XSS)** | 🟡 Medium (6.5) | `CVSS:3.1/AV:N/AC:L/PR:L/UI:R/S:C/C:L/I:L/A:N` | A03:2021-Injection |

---

## 3. Core Portfolio Project Deliverables
To view the complete breakdown of our findings, open the files in the directory root layout above:

1. **`Capstone_Final_Report.pdf`**: The master bound enterprise document containing professional formatting, full proof-of-concept verification HTTP headers, terminal capture logs, and step-by-step patch codes.
2. **`master_report.md`**: The raw source documentation layout compiling all Nmap infrastructure logs, target scanning ports, and secure code samples.

---

## 4. Prioritized Patch Engineering Roadmap
Defensive engineering actions have been provided to development teams and network administrators to eliminate open vulnerabilities systematically:

* **Immediate Remediation (0 - 48 Hours):** Transition database ingress calls to strict **parameterized query arguments** to permanently break SQL Injection strings. Completely block external access to legacy serialization network sockets.
* **Short-Term Actions (2 - 4 Weeks):** Deploy deep server-side session token validation to verify tenant ownership boundaries on every API identifier parameter call.
* **Long-Term Continuity Strategy:** Build automated static analysis (SAST) engines into the continuous integration / continuous deployment (CI/CD) pipelines to review packages before production deployment.
*
