# Summary of Windows Utilities and Tools

🔗 Room Link: [Windows Fundamentals 2](https://tryhackme.com/room/windowsfundamentals2x0x)

This document provides an overview of several important Windows system utilities, many of which can be accessed through the System Configuration tool (MSConfig) or directly from the Start Menu. These utilities help manage, troubleshoot, and monitor different parts of the operating system.



## 1. System Configuration (MSConfig)

MSConfig is mainly used for troubleshooting startup issues. It has five tabs:

- **General:** Choose what to load on startup (normal, selective, or diagnostic).
- **Boot:** Configure boot options.
- **Services:** See all services installed, whether running or stopped.
- **Startup:** Used to be for startup programs, but Microsoft recommends using Task Manager now.
- **Tools:** Quick access to many Windows utilities, with descriptions and commands to launch them.



## 2. User Account Control (UAC) Settings

- UAC controls how Windows notifies you about changes to your system.
- You can adjust UAC settings by moving a slider, but turning it off completely is not recommended.
- Command to open UAC settings: `UserAccountControlSettings.exe`



## 3. Computer Management (`compmgmt.msc`)

This utility has three main parts:

- **System Tools:** Includes Task Scheduler (automate tasks), Event Viewer (review system logs), Shared Folders (view network shares), Local Users and Groups, Performance Monitor, and Device Manager.
- **Storage:** Mainly Disk Management, which handles partitions, drive letters, and disks.
- **Services and Applications:** Manage services and WMI Control for scripting and remote management.



## 4. System Information (`msinfo32.exe`)

- Displays detailed hardware, software, and system environment information.
- Divided into Hardware Resources, Components, and Software Environment.
- View environment variables (key system data like Windows install folder).
- Useful for diagnosing issues or learning system specs.



## 5. Resource Monitor (`resmon.exe`)

- Shows detailed real-time info about CPU, memory, disk, and network usage.
- Helps advanced users troubleshoot performance or resource conflicts.
- Multiple tabs with detailed views and live graphs.



## 6. Command Prompt (`cmd.exe`)

- A text-based interface for Windows interaction.
- Useful commands:
  - `hostname` — shows computer name.
  - `whoami` — shows logged-in user.
  - `ipconfig` — network config (`/all` for detailed info).
  - `netstat` — network connections and stats.
  - `net` — manage network resources, with sub-commands like `net help user`.
- Powerful for troubleshooting and system info.



## 7. Registry Editor (`regedt32.exe`)

- The Registry stores system and application settings.
- Editing the registry can affect system behavior — only for advanced users.
- Registry Editor lets you view and modify this configuration data.



## 8. Conclusion

- Many Windows utilities can be launched from MSConfig’s Tools tab, but can also be accessed directly.
- Knowing commands and shortcuts speeds up working with Windows internals.
- Be careful when changing settings in tools like Registry Editor or UAC.



## Key Takeaways

- Windows includes built-in tools for managing startup programs, services, user accounts, system performance, and hardware.
- MSConfig is a handy troubleshooting start but not the only way to access these tools.
- Proper knowledge of these utilities can greatly help system management and troubleshooting.



*Feel free to explore these tools further for advanced system management!*

