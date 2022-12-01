1. Broken access Control
 * Violation of least ptivilege
 * CORS miconfiguration
 * IDOR to view/access another's account
 * Cookie manipulation to elevate privileges

2. Cryptographic failures
 * Is data sent in cleartext (HTTP, FTP, SMTP)
 * Deprecated hash functions (MD5)
 * Old or weak crypto algorithms
 * Weak crypto keys
 * Are IVs weak/reused 
 * Insecure mode of operation (ECB)

3. Injection
 * User supplied data not sanitised/validated
 * User supplied data directly used in queries

4. Insecure Design
 * Limit resource consumption by user or service
 * Establish and use a secure development lifecycle with AppSec professionals
 * Use threat modeling for critical authentication, access control, business logic, and key flows
 * Establish and use a library of secure design patterns

5. Security Misconfiguration
 * Default accounts and passwords in use
 * Unnecessary features (ports, services, pages, accounts, privileges) installed
 * Overly verbose error messages/ stack traces
 * Software out of data/vulnerable
 * Proper CSP configuration

6. Vulnerable and outdated components
 * Scan for vulnerabilities
 * Inventory client-side and server-side components
 * Check OS, web server, DBMS, APIs, libraries etc for vulnerabilities

7. Identification and Authentication Failures
 * Permits brute force attacks
 * Permits automated attacks like credential stuffing
 * Permits weak/default passwords
 * Lack of MFA
 * Weak or ineffective credential recovery like questions and answers

8. Software and data integrity failures
 * Use digital signtures to verify software
 * Ensure there is a review process for code before deployment
 * Ensure CI/CD pipeline has proper segregation, configuration and access control

9. Security logging and monitoring failures
 * Logins, failed loging and high-value transactions are not logged
 * Logs are only stored locally
 * Warnings and errors generate insufficient log messages
 * Application and API logs are not monitroed for suspicious activity
 * Pen testing tools (Sqlmap, gobuster, burp) don't trigger alerts

10. Server Side Request Forgery
 * Ocurrs when a web app fetches a remote resource without validating the user supplied url
 * Segment remote resource access functionality (separate servers vulnersble to SSRF away from high value resources)
 * Enforce firewall policies to reject all but essential intranet traffic
 * Sanitize and validate user input
 * Enfore url schema, destination and port from a whitelist
 * Disable HTTP redirections
 * Don't return rw output to clients
