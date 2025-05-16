Room Title: OWASP Top 10 - 2021
Difficulty: Easy
Time to Complete: 120 minutes
Skills Covered:

    Broken Access Control
    Cryptographic Failures
    Injection
    Insecure Design
    Command Injection
    Security Misconfiguration
    Vulnerable and Outdated Components
    Identification and Authentication Failures
    Software and Data Integrity Failures
    Security Logging and Monitoing Failures
    SSRF
    
🏛️ Key Concepts and Lessons Learned
🔹 Broken Access Control
  
    Websites have pages that are protected from regular visitors. For example, only the site's admin user should be able to access a page to manage other users. 
    If a website visitor can access protected pages they are not meant to see, then the access controls are broken.

    A regular visitor being able to access protected pages can lead to the following:

    Being able to view sensitive information from other users
    Accessing unauthorized functionality

    Simply put, broken access control allows attackers to bypass authorisation, allowing them to view sensitive data or perform tasks they aren't supposed to.

🔹 Cryptographic Failures
     
    A cryptographic failure refers to any vulnerability arising from the misuse (or lack of use) of cryptographic algorithms for protecting sensitive information. 
    Web applications require cryptography to provide confidentiality for their users at many levels. 

🔹 Injection

    Injection flaws are very common in applications today. These flaws occur because the application interprets user-controlled input as commands or parameters. 
    Injection attacks depend on what technologies are used and how these technologies interpret the input. Some common examples include:

    SQL Injection: This occurs when user-controlled input is passed to SQL queries. As a result, an attacker can pass in SQL queries to manipulate the outcome of such queries. 
    This could potentially allow the attacker to access, modify and delete information in a database when this input is passed into database queries. 
    This would mean an attacker could steal sensitive information such as personal details and credentials.
    Command Injection: This occurs when user input is passed to system commands. As a result, an attacker can execute arbitrary system commands on application servers, potentially allowing them to access users' systems.

    The main defence for preventing injection attacks is ensuring that user-controlled input is not interpreted as queries or commands. There are different ways of doing this:

    Using an allow list: when input is sent to the server, this input is compared to a list of safe inputs or characters. If the input is marked as safe, then it is processed. Otherwise, it is rejected, and the application throws an error.
    Stripping input: If the input contains dangerous characters, these are removed before processing.

  🔹 Insecure Design

    Insecure design refers to vulnerabilities which are inherent to the application's architecture. 
    They are not vulnerabilities regarding bad implementations or configurations, but the idea behind the whole application (or a part of it) is flawed from the start. 
    Most of the time, these vulnerabilities occur when an improper threat modelling is made during the planning phases of the application and propagate all the way up to your final app. Some other times, 
    insecure design vulnerabilities may also be introduced by developers while adding some "shortcuts" around the code to make their testing easier. 
    A developer could, for example, disable the OTP validation in the development phases to quickly test the rest of the app without manually inputting a code at each login but forget to re-enable it when sending the application to production.

  🔹 Security Misconfiguration

    Security Misconfigurations are distinct from the other Top 10 vulnerabilities because they occur when security could have been appropriately configured but was not. 
    Even if you download the latest up-to-date software, poor configurations could make your installation vulnerable.

    Security misconfigurations include:

    Poorly configured permissions on cloud services, like S3 buckets.
    Having unnecessary features enabled, like services, pages, accounts or privileges.
    Default accounts with unchanged passwords.
    Error messages that are overly detailed and allow attackers to find out more about the system.
    Not using HTTP security headers.

    This vulnerability can often lead to more vulnerabilities, such as default credentials giving you access to sensitive data, XML External Entities (XXE) or command injection on admin pages.

  🔹 Identification and Authentication Failures

    Authentication and session management constitute core components of modern web applications. Authentication allows users to gain access to web applications by verifying their identities. 
    The most common form of authentication is using a username and password mechanism. 
    A user would enter these credentials, and the server would verify them. 
    The server would then provide the users' browser with a session cookie if they are correct. A session cookie is needed because web servers use HTTP(S) to communicate, which is stateless. 
    Attaching session cookies means the server will know who is sending what data. The server can then keep track of users' actions. 

    If an attacker is able to find flaws in an authentication mechanism, they might successfully gain access to other users' accounts. This would allow the attacker to access sensitive data (depending on the purpose of the application). 
    Some common flaws in authentication mechanisms include the following:

    Brute force attacks: If a web application uses usernames and passwords, an attacker can try to launch brute force attacks that allow them to guess the username and passwords using multiple authentication attempts. 
    Use of weak credentials: Web applications should set strong password policies. If applications allow users to set passwords such as "password1" or common passwords, an attacker can easily guess them and access user accounts.
    Weak Session Cookies: Session cookies are how the server keeps track of users. If session cookies contain predictable values, attackers can set their own session cookies and access users' accounts. 

    There can be various mitigation for broken authentication mechanisms depending on the exact flaw:

    To avoid password-guessing attacks, ensure the application enforces a strong password policy. 
    To avoid brute force attacks, ensure that the application enforces an automatic lockout after a certain number of attempts. This would prevent an attacker from launching more brute-force attacks.
    Implement Multi-Factor Authentication. 
    If a user has multiple authentication methods, for example, using a username and password and receiving a code on their mobile device, it would be difficult for an attacker to get both the password and the code to access the account.

  🔹 Software and Data Integrity Failures

    This vulnerability arises from code or infrastructure that uses software or data without using any kind of integrity checks. 
    Since no integrity verification is being done, an attacker might modify the software or data passed to the application, resulting in unexpected consequences. There are mainly two types of vulnerabilities in this category:

    Software Integrity Failures
    Data Integrity Failures

  🔹 Software and Data Integrity Failures
    
🔍 Reflection

This room helped me to know some more about the security headers in HTTP Requests
