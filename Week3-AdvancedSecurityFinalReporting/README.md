# Week 3: Advanced Security and Final Reporting

## Overview
This report details the advanced security tasks performed on the OWASP Juice Shop web application. Week 3 focused on comprehensive penetration testing using Nmap, implementing secure logging with the Winston library, and creating a complete security best practices checklist. These measures further enhance the application's defense by identifying vulnerabilities, ensuring effective monitoring, and establishing ongoing security guidelines.

## Objectives
- **Advanced Penetration Testing:**  
  Execute multiple types of scans (basic, full, aggressive, and vulnerability scans) using Nmap to identify potential weaknesses.
- **Secure Logging Implementation:**  
  Configure logging in a Node.js environment using Winston to capture critical application events and errors.
- **Security Best Practices Checklist:**  
  Develop a comprehensive checklist in MS Word that outlines essential security measures such as input validation, HTTPS enforcement, password hashing, vulnerability scanning, and secure logging.

## Implementation Details

### 1. Basic Penetration Testing
- **Description:**  
  Utilize Nmap to perform a range of scans to gather detailed information about the target system.
- **Scans Performed:**
  - **Basic Port Scan:**  
    Identify open ports on the target (e.g., `nmap localhost -p 3000`).
  - **Service Version Detection:**  
    Determine service versions with `nmap -sV localhost -p 3000`.
  - **Full Port Scan:**  
    Scan all ports using `nmap -p- localhost`.
  - **Aggressive Scan:**  
    Combine OS detection, version detection, script scanning, and traceroute using `nmap -A localhost -p 3000`.
  - **Vulnerability Scanning with NSE Scripts:**  
    Run vulnerability scripts via `nmap --script vuln localhost -p 3000`.
  - **External IP Scanning:**  
    Simulate scanning from outside the local network (e.g., `nmap -sV [External_IP_Address] -p 3000`).
- **Testing:**  
  Screenshots of terminal outputs and browser tests (such as XSS payload execution) document the findings.

### 2. Secure Logging Implementation
- **Description:**  
  Implement secure logging in a Node.js environment using Winston to log application events to both the console and a dedicated file (`security.log`).
- **Steps:**
  - **Installation:**  
    Run `npm install winston`.
  - **Configuration:**  
    Created a `logger.js` file with code that sets up Winston to log in JSON format with timestamps.
  - **Testing:**  
    Executed `node logger.js` to verify console output and confirmed that the `security.log` file contains the same log entries.
- **Verification:**  
  Console and file outputs were compared to ensure consistency in logging.

### 3. Security Best Practices Checklist
- **Description:**  
  Develop a detailed security checklist using MS Word that documents industry-standard practices.
- **Checklist Items Include:**
  - **Validate All Inputs:** Ensure inputs are validated and sanitized.
  - **Use HTTPS for Data Transmission:** Enforce encrypted data transfer.
  - **Hash and Salt Passwords:** Securely store user credentials using strong hashing algorithms.
  - **Regular Vulnerability Scanning:** Schedule and perform scans using tools like Nmap and OWASP ZAP.
  - **Implement Secure Logging:** Use tools like Winston to log application events.
  - **Keep Software and Dependencies Updated:** Regularly update all components to address vulnerabilities.
- **Documentation:**  
  Screenshots and a copy of the checklist document are attached as evidence of task completion.

## Testing and Verification
- **Penetration Testing:**  
  Verified each Nmap scan type through terminal outputs and documented findings with screenshots.
- **Logging:**  
  Confirmed proper logger setup by matching console outputs with entries in the `security.log` file.
- **Checklist:**  
  Reviewed and formatted the checklist in MS Word; screenshots of the document are included for reference.

## Conclusion
The advanced security tasks in Week 3 significantly enhance the OWASP Juice Shop application’s security posture. Detailed penetration testing identifies vulnerabilities, while secure logging facilitates proactive monitoring. The security checklist provides a comprehensive guide to maintain and improve security over time. These efforts collectively contribute to a robust, secure application environment.

## References
- [Nmap Documentation](https://nmap.org/)
- [Winston Logging Library](https://github.com/winstonjs/winston)
- [OWASP Juice Shop GitHub](https://github.com/juice-shop/juice-shop)
- [Helmet.js Documentation](https://helmetjs.github.io/)
