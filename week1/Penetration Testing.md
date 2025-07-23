# Penetration Testing Summary

[TryHackMe - Pentesting Fundamentals](https://tryhackme.com/room/pentestingfundamentals)


## What is Penetration Testing?

Penetration Testing (or Pentesting) is the ethical and authorized process of simulating cyberattacks to identify and fix security vulnerabilities in systems, networks, or applications. Pentesters use tools and methods similar to real attackers to evaluate defenses.

- Goal: Discover vulnerabilities before malicious actors do.
- Importance: With cyberattacks happening every 39 seconds (Security Magazine), pentesting helps protect data and systems.

## Penetration Testing Ethics

- Pentesting is only legal when authorized by the system owner.
- Rules of Engagement (ROE):
  - Permission: Legal consent to test.
  - Scope: Systems and services to be tested.
  - Rules: What techniques are/aren’t allowed (e.g., phishing, MITM).

### Hacker Types
| Hat Type   | Description                                                                 
|------------|------------------------------------------------------------------
| White Hat  | Ethical hacker working legally to improve security.                        
| Grey Hat   | May break rules but with good intentions (e.g., exposing scams).           
| Black Hat  | Malicious hacker aiming to steal, harm, or extort.                         


## Penetration Testing Methodology

### General Stages:
1. Information Gathering – OSINT; collect public data (no scanning).
2. Enumeration/Scanning – Identify active systems/services.
3. Exploitation – Use vulnerabilities to gain access.
4. Privilege Escalation – Increase access (horizontal or vertical).
5. Post-Exploitation – Pivoting, data gathering, covering tracks, reporting.


## Testing Frameworks

### OSSTMM
- Use: Telecommunications, networks, communications.
- Advantages: Detailed and flexible.
- Disadvantages: Complex and uses unique terms.

### OWASP
- Use: Web application testing.
- Advantages: Easy to use, frequently updated, covers all phases.
- Disadvantages: No formal accreditation.

### NIST Cybersecurity Framework 1.1
- Use: Organization-wide cybersecurity risk management.
- Advantages: Detailed standards and accreditation.
- Disadvantages: Not pentesting-focused; limited auditing; weak cloud coverage.

### NCSC CAF
- Use: Critical infrastructure and vital services.
- Advantages: Government-backed, covers 14 security principles.
- Disadvantages: Still new, less prescriptive.


## Black Box, Grey Box, and White Box Testing

| Type         | Description                                                                
|--------------|----------------------------------------------------------------------------
| Black Box    | No internal info. Tester simulates outsider. Info gathering is key.        
| Grey Box     | Partial internal knowledge. Saves time while testing real-like scenarios.  
| White Box    | Full access to source code. Deep and thorough testing, often by developers.


## Practice Recap: ACME Penetration Test

- Completed full engagement on a simulated infrastructure.
- Flag: `THM{PENTEST_COMPLETE}`

