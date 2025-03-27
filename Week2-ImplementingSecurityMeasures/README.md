# Week 2: Implementing Security Measures

## Overview
This report documents the security enhancements implemented on the OWASP Juice Shop web application during Week 2. The focus was on mitigating identified vulnerabilities by incorporating key security measures such as input validation and sanitization, password hashing, token-based authentication, and securing HTTP headers.

## Objectives
- **Input Validation & Sanitization:** Ensure that all user inputs (e.g., email addresses) are validated using the Validator library to prevent attacks like XSS and SQL Injection.
- **Password Hashing:** Secure user credentials by hashing passwords with Bcrypt before storage.
- **Token-Based Authentication:** Implement Jsonwebtoken (JWT) to generate secure tokens for managing user sessions.
- **Securing HTTP Headers:** Utilize Helmet.js to set secure HTTP headers and protect against common web attacks.

## Implementation Details

### 1. Input Validation and Sanitization
- **Description:**  
  Validation of user inputs is critical to protect the application against malicious payloads. The Validator library is used to ensure proper email format and sanitize inputs.
- **Steps:**
  - Modified the main server file to include custom routes.
  - Created a `validateInput.js` file in the routes folder.
  - Integrated email validation and error logging.
- **Testing:**  
  POST requests were sent using Postman to verify the registration and login endpoints. Console logs and response messages confirmed proper input validation.

### 2. Password Hashing
- **Description:**  
  Using Bcrypt, plain-text passwords are securely hashed before being stored. This prevents exposure of sensitive credentials even if the database is compromised.
- **Steps:**
  - Installed Bcrypt using `npm install bcrypt`.
  - Integrated Bcrypt in the registration endpoint within `validateInput.js`.
  - Hashed passwords using 10 salt rounds.
- **Testing:**  
  Successful password hashing was verified via console logs displaying the hashed output and confirmation messages.

### 3. Token-Based Authentication
- **Description:**  
  Secure user sessions by implementing token-based authentication using the Jsonwebtoken library.
- **Steps:**
  - Installed Jsonwebtoken with `npm install jsonwebtoken`.
  - Updated the login endpoint to generate and return a secure token upon successful login.
- **Testing:**  
  Testing with curl/Postman showed that a JSON token was generated and returned, confirming correct implementation.

### 4. Securing HTTP Headers
- **Description:**  
  Helmet.js was used to set security-related HTTP headers to protect the application from attacks like clickjacking and MIME sniffing.
- **Steps:**
  - Installed Helmet using `npm install helmet`.
  - Integrated Helmet in the server file by adding `app.use(helmet());`.
  - Optionally configured a Content Security Policy (CSP) for additional security.
- **Testing:**  
  Verification was done by inspecting HTTP response headers using browser developer tools and curl commands.

## Testing and Verification
- All endpoints were tested using Postman and curl.
- Detailed console logs, screenshots, and video recordings were captured to verify that each security measure was implemented correctly.
- Each step of the process was documented to ensure reproducibility and clarity.

## Conclusion
The security measures implemented in Week 2 significantly enhance the overall protection of the OWASP Juice Shop application. Input validation, secure password hashing, token-based authentication, and secured HTTP headers form a robust defense against common web vulnerabilities. These enhancements lay the foundation for a secure application environment and provide a clear guide for future improvements.

## References
- [Validator Library Documentation](https://www.npmjs.com/package/validator)
- [Bcrypt Documentation](https://www.npmjs.com/package/bcrypt)
- [Jsonwebtoken Documentation](https://www.npmjs.com/package/jsonwebtoken)
- [Helmet.js Documentation](https://helmetjs.github.io/)

