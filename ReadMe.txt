 Web Application Security Assessment

 Project Overview
This project involves performing a security assessment of a mock web application.  
The goal was to identify potential vulnerabilities, analyze their risk level, and recommend solutions to improve the overall security posture of the application.  

The testing was performed manually and with the help of automated security tools.

---

 Steps Performed

1. Application Setup
   - Installed required dependencies using:
     ```
     npm install
     npm start
     ```
   - Accessed the web application at `http://localhost:3000`

2. Exploration of the Application
   - Created a test account using the following credentials:
     - **Email**: `hahuu@hi.ji`
     - **Password**: `123456`
   - Explored login, signup, and profile functionalities.
   - Checked for user input validation and session management.

3. Vulnerability Assessment
   - Identified multiple potential vulnerabilities such as:
     - Missing **Content Security Policy (CSP)**
     - Insecure password policy (weak password allowed)
     - Potential XSS and injection risks
     - Error handling and information disclosure

4. Mitigation Recommendations
   - Configure the server to send a **Content-Security-Policy header**.
   - Enforce strong password policies (minimum length, complexity).
   - Implement input sanitization and output encoding.
   - Restrict error messages to avoid exposing sensitive details.

---

Sample Vulnerability Report (Example)

Vulnerability: Missing Content Security Policy (CSP)  
Severity: Medium  
Description: Without a CSP header, the application is vulnerable to XSS and injection attacks.  
Recommendation: Configure the application server to send a strict `Content-Security-Policy` header.  

---

 Tools Used
- Browser (manual exploration)
- Basic Node.js server setup
- Security testing tools (ZAP, Burp Suite – optional if available)

---

 Conclusion
The assessment highlighted the importance of implementing security best practices such as CSP, secure authentication, input validation, and proper error handling.  
These measures reduce the attack surface and protect both the application and its users from common web-based threats.

 Author
- Security Assessment performed by: Rimsha Bibi
- Submitted as part of Week 1 Security Task
