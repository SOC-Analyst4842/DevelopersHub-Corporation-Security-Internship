# Week 1: Security Assessment Report

## Overview
This report details the security assessment performed on the OWASP Juice Shop web application. The focus of this week was to evaluate the application's vulnerabilities using both automated and manual testing techniques in a controlled Kali Linux environment.

## Objectives
- **Environment Setup:** Deploy and configure the OWASP Juice Shop on a local machine.
- **Automated Vulnerability Scanning:** Utilize tools like OWASP ZAP to detect common security weaknesses.
- **Manual Vulnerability Testing:** Conduct targeted tests (e.g., XSS, SQL Injection) using browser developer tools.
- **Documentation:** Record all findings with detailed screenshots, logs, and observations for future remediation.

## Environment Setup
- **Operating System:** Kali Linux
- **Dependencies:** Git, Node.js, npm
- **Application Deployment:**
  - Cloned the OWASP Juice Shop repository from GitHub.
  - Installed necessary packages using `npm install`.
  - Launched the application using `npm start`.
  - Verified the deployment by accessing [http://localhost:3000](http://localhost:3000) in the browser.

## Tools Used
- **OWASP ZAP:** For automated scanning to identify vulnerabilities such as missing security headers and potential XSS issues.
- **Browser Developer Tools:** For manual testing including payload injections to simulate attacks like XSS and SQL Injection.

## Vulnerability Assessment Process

### Automated Scan (OWASP ZAP)
- **Setup:** Launched OWASP ZAP and configured the target URL to [http://localhost:3000](http://localhost:3000).
- **Execution:** Ran a full automated scan using both the Quick Start and Active Scan options.
- **Outcome:** OWASP ZAP identified several potential vulnerabilities which were recorded for further manual verification.

### Manual Testing
- **XSS Testing:**
  - Opened the application in a browser.
  - Activated Developer Tools (F12) to inspect input fields.
  - Tested by injecting payloads such as `<script>alert('XSS');</script>`.
  - **Result:** An alert popup indicated a successful XSS vulnerability demonstration.
  
- **SQL Injection Testing:**
  - Attempted login using payloads like `admin' OR '1'='1` in the email and password fields.
  - **Result:** The login form rejected the injection with an "Invalid email or password" message, indicating resistance against SQL injection.

## Findings and Observations
- **Port Accessibility:** Confirmed that the application is accessible at the designated port.
- **Automated Scan:** OWASP ZAP provided a comprehensive overview of potential vulnerabilities.
- **Manual Testing:** 
  - XSS vulnerability was demonstrated by successful payload execution.
  - SQL Injection tests indicated that the login mechanism is secure against basic injection attempts.
- **Overall Assessment:** The findings serve as a foundation for the subsequent implementation of security measures to remediate identified vulnerabilities.

## Conclusion
The security assessment successfully identified key vulnerabilities in the OWASP Juice Shop web application. The combination of automated scanning and manual testing provided valuable insights into the current security posture, guiding the necessary remediation steps in the upcoming tasks. Continued testing and periodic reassessment are recommended to maintain robust security.

## References
- [OWASP ZAP Documentation](https://www.zaproxy.org/)
- [OWASP Juice Shop GitHub Repository](https://github.com/juice-shop/juice-shop)

