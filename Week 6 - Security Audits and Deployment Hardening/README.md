# Week 6 – Advanced Security Audits & Final Deployment Security

## 🎯 Goal:
Conduct detailed security audits, ensure compliance with standards, and prepare the application for a secure production deployment.

---

## 🛠️ Tasks Breakdown:

### 1. Security Audits & Compliance
- Performed vulnerability scanning using:
  - **OWASP ZAP** – for finding web vulnerabilities.
  - **Nikto** – for web server misconfigurations.
  - **Lynis** – for Linux system audits.
- Verified application against **OWASP Top 10** best practices.
- Documented all security issues with recommended fixes.

### 2. Secure Deployment Practices
- Implemented:
  - **Automatic security updates** for OS and libraries.
  - **Dependency scanning** using `npm audit` and `Docker scan`.
  - **Docker Hardening**: Used `docker-slim` and scanned images via `Trivy`.

### 3. Final Penetration Testing
- Full penetration test using **Metasploit Framework**.
- Included:
  - Port scanning and service enumeration.
  - Payload crafting and exploitation of vulnerable components.
- All results documented with screenshots and remediation steps.

---

## 🧪 Tools & Technologies Used:
- **OWASP ZAP**, **Nikto**, **Lynis**, **Metasploit**
- **Docker**, **npm audit**, **Trivy**
- **Kali Linux**, **Ubuntu Server**

---

## 📂 Folder Contents:
- `audit-reports/` – Detailed output of ZAP and Nikto.
- `metasploit-testing/` – Exploit logs and vulnerability reports.
- `screenshots/` – Test execution proof
- `final-report.pdf` – Consolidated documentation of Week 6

---

## ✅ Outcome:
- Audited application and server configurations for real-world threats.
- Secured the deployment pipeline and infrastructure.
- Gained experience in full-cycle security testing and compliance checks.
