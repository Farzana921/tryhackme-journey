# Web Application Security Summary
🔗 Room Link: [Web Application Security](https://tryhackme.com/room/introwebapplicationsecurity)

## What Is a Web Application?
A web application is like a regular program, but instead of installing it, you access it through a web browser (e.g., Chrome, Firefox).  
Examples include Gmail, Google Docs, Amazon, and Online Banking.

## What Do You Need to Access a Web Application?
- A **modern web browser**  
- An **internet connection**  
- No need to install software — just open the website  

## Web Applications – Typical User Actions:
When shopping online, you usually:  
1. Log in  
2. Search for products  
3. Add items to the cart  
4. Enter shipping details  
5. Provide payment information  

# Common Web Application Vulnerabilities (from OWASP Top Ten)

### 1. Identification and Authentication Failure
- Weak login security.  
- **Examples:**  
  - No limit on password attempts, allowing brute-force attacks  
  - Weak or reused passwords  
  - Passwords stored in plain text  

### 2. Cryptographic Failures
- Poor use of encryption.  
- **Examples:**  
  - Sending sensitive data in cleartext (e.g., HTTP instead of HTTPS)  
  - Using weak encryption algorithms or default keys  

### 3. Broken Access Control
- Users accessing data or functions they shouldn’t.  
- **Examples:**  
  - One user viewing or editing another’s account  
  - Unauthorized users accessing admin pages  
  - Customers changing product data they shouldn’t  

### 4. Injection Attacks
- Input is not properly validated.  
- Attackers insert malicious code into forms or URLs.  
- This can expose data or even allow control of the server.  

# IDOR (Insecure Direct Object Reference)

## What is IDOR?
- A type of **Broken Access Control** vulnerability.  
- It occurs when an attacker changes an **ID in the URL** to access other users' data or system objects they shouldn't have access to.  
- Example:  
  `https://site.com/user?id=16` → change to `id=17` to view another user’s data.

## TryHackMe Scenario:
- You investigate an **Inventory Management System** vulnerable to IDOR.  
- Your tasks:  
  1. Explore URLs with different user IDs  
  2. Identify the malicious user  
  3. Revert sabotage (wrong tire assignments)  
  4. Receive the flag  

## Final Flag:  
`THM{IDOR_EXPLORED}`

Here is a screenshot of the flag received after fixing the issue:  
![Flag Screenshot](../Flag.jpg)
