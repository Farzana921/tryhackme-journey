#  Metasploit Framework

🔗 Room Link: [Red Team Engagements](https://tryhackme.com/room/metasploitintro)

This document summarizes the fundamentals of using the **Metasploit Framework** as covered in Tasks 1 to 4. It includes basic usage, module components, msfconsole commands, and the exploitation workflow.

---

## Task 1: Introduction to Metasploit

Metasploit is the most widely used **exploitation framework** in cybersecurity. It supports the full lifecycle of a penetration test:

*  Information Gathering
*  Vulnerability Scanning
*  Exploitation
*  Post-Exploitation
*  Exploit Development
*  Vulnerability Research

### Versions

* **Metasploit Pro**: Paid version with GUI, automation, and team collaboration features.
* **Metasploit Framework**: Free, open-source, command-line version (used in this course/module).

### Core Components

* `msfconsole`: Main CLI to interact with modules.
* **Modules**:

  * Exploits
  * Scanners
  * Payloads
* **Tools**:

  * `msfvenom`: Payload generator.
  * `pattern_create`, `pattern_offset`: Used for exploit dev (not covered in this module).


## Task 2: Main Components of Metasploit

### Key Concepts

* **Vulnerability**: A flaw in code or logic.
* **Exploit**: Code that takes advantage of a vulnerability.
* **Payload**: Code executed after exploitation (e.g., reverse shell).

### Module Categories

* **Auxiliary**: Scanners, crawlers, and fuzzers.
* **Encoders**: Obfuscate payloads (limited success against modern AV).
* **Evasion**: Bypass antivirus/security tools.
* **Exploits**: Actual attack code, organized by target (Windows, Linux, etc.).
* **NOPs**: No-operation instructions used as padding (e.g., `0x90`).
* **Payloads**:

  * **Singles**: Standalone payloads (e.g., `calc.exe`).
  * **Stagers**: Initial communication setup.
  * **Stages**: Fetched after stager, carry larger/more complex payloads.
  * **Adapters**: Convert payloads into different formats (e.g., PowerShell).
* **Post**: Used after a successful exploit (e.g., data exfiltration, privilege escalation).

### Payload Examples

* `generic/shell_reverse_tcp` → Single payload (`_` format)
* `windows/x64/shell/reverse_tcp` → Staged payload (`/` format)
* `windows/x64/pingback_reverse_tcp` → Single payload

### Modules are stored in:

```
/opt/metasploit-framework/embedded/framework/modules/
```


## Task 3: msfconsole

`msfconsole` is the main CLI for the Metasploit Framework. It allows users to search, configure, and run modules.

### Starting Metasploit

```bash
msfconsole
```

* The prompt will look like: `msf6 >` or `msf5 >` depending on your version.

### Common Commands

| Command                    | Description                       |
| -------------------------- | --------------------------------- |
| `help` or `help <command>` | Show help                         |
| `search <keyword>`         | Search for modules                |
| `use <module>`             | Load a module                     |
| `show options`             | Show required/optional parameters |
| `show payloads`            | List compatible payloads          |
| `info <module>`            | Show detailed info                |
| `back`                     | Exit module context               |
| `history`                  | Show command history              |

### Context Awareness

When using a module, the prompt changes to reflect the context:

```
msf6 exploit(windows/smb/ms17_010_eternalblue) >
```

Parameters set here are **module-specific**, unless set globally using `setg`.

### Advanced Search Examples

```bash
search cve:2017-0144
search type:exploit apache
search platform:windows
```

### Exploit Ranking System

* Excellent
* Great
* Good
* Normal
* Average
* Low
* Manual

Higher rankings indicate better reliability and stability.


## Task 4: Working with Modules

Modules are the core of Metasploit's functionality.

### Setting Parameters

```bash
set RHOSTS 10.10.165.39
set LPORT 4444
```

### Global Parameters

Use `setg` to set a parameter across all modules:

```bash
setg RHOSTS 10.10.19.23
unsetg RHOSTS
```

### Clearing Parameters

```bash
unset PAYLOAD     # Clear one parameter
unset all         # Clear all parameters
```

### Running Modules

* `exploit`: Run the exploit.
* `run`: Alias for `exploit` (used for scanners, etc.).
* `exploit -z`: Run and background the session automatically.

### Sessions

Once a target is exploited, a **session** is created.

```bash
sessions             # List all sessions
sessions -i <id>     # Interact with session
background           # Background the session
CTRL + Z             # Shortcut to background
```



## Quick Reference

| Task   | Question          | Answer                    |
| ------ | ----------------- | ------------------------- |
| Task 4 | Set LPORT to 6666 | `set LPORT 6666`          |
| Task 4 | Set global RHOSTS | `setg RHOSTS 10.10.19.23` |
| Task 4 | Clear a payload   | `unset PAYLOAD`           |
| Task 4 | Run an exploit    | `exploit`                 |



## Final Notes

This is just the beginning. Metasploit is a powerful and flexible tool that goes far beyond basic exploitation. Upcoming modules will go deeper into:

* Meterpreter
* Post-exploitation
* Persistence techniques
* Custom payload creation

