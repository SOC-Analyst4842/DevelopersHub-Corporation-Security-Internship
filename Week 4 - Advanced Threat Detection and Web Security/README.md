# Week 4 – Advanced Threat Detection & Web Security Enhancements

## 🎯 Goal:
Implement advanced security measures, detect threats in real-time, and secure API endpoints.

---

## 🔐 Tasks Breakdown:

### 1. Intrusion Detection & Monitoring
- Set up real-time monitoring using **Fail2Ban** or **OSSEC**.
- Configure alerts for multiple failed login attempts.
- Monitor logs and visualize patterns of brute-force attacks.

### 2. API Security Hardening
- Applied **rate limiting** using `express-rate-limit` to prevent brute-force and DoS.
- Proper **CORS configuration** to restrict unauthorized origins.
- Integrated **OAuth2** or **API key** based authentication for API access control.

### 3. Security Headers & CSP Implementation
- Implemented **Content Security Policy (CSP)** to protect against XSS attacks.
- Enforced **Strict-Transport-Security (HSTS)** for HTTPS-only traffic.
- Added headers via `helmet` in Node.js:
  - `X-Content-Type-Options`
  - `X-Frame-Options`
  - `X-XSS-Protection`

---

## 🧪 Tools & Technologies Used:
- **Fail2Ban**, **OSSEC**, **Node.js**, **Express**
- **express-rate-limit**, **helmet**, **CORS**
- **OAuth**, **API Keys**, **Postman**

---

## 📂 Folder Contents:
- `fail2ban-config/` – Fail2Ban config files and logs
- `api-security-demo/` – Node.js API with CORS, rate limiting, and OAuth
- `screenshots/` – Setup screenshots
- `report.pdf` – Summary of implementations and testing

---

## ✅ Outcome:
- Enhanced backend and API security posture.
- Real-time alerts configured for suspicious login behavior.
- Hardened API endpoints against unauthorized access and abuse.
