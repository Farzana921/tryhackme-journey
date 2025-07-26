# Hydra Brute Force Tool – Notes & Usage

🔗 Room Link: [Red Team Engagements](https://tryhackme.com/room/hydra)

## Introduction

Hydra is a powerful and fast online password cracking tool used for brute-forcing login credentials on various services. I recently got hands-on with it during a lab, and here's a breakdown of what I learned.

Hydra is especially useful when you have a list of passwords and need to test them quickly against login forms or services like **SSH**, **FTP**, **HTTP**, and many more. It's commonly used in penetration testing to check for weak or default credentials on systems.

> One of the biggest takeaways: **weak passwords = wide open doors**. Even default creds like `admin:password` can be easily cracked.



## Supported Protocols

Hydra supports a ton of protocols for brute-forcing. Some notable ones include:

- **SSH, FTP, Telnet, RDP, VNC**
- **HTTP/HTTPS (GET, POST forms)**
- **MySQL, PostgreSQL, Oracle, MongoDB**
- **SNMP, LDAP, SMB**
- **Email services like IMAP, POP3, SMTP**
- Even IRC, XMPP, Cisco services, and more

> You can check the full list in Hydra's help or official repo.



## Installing Hydra

I used Hydra on a **Kali Linux** AttackBox, where it comes pre-installed. But it’s also easy to install on other systems:

- On **Ubuntu/Debian**:
  ```bash
  sudo apt install hydra
