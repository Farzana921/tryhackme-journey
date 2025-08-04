Windows Fundamentals Summary


🔗 Room Link: [Windows Fundamentals 1](https://tryhackme.com/room/windowsfundamentals1xbx)


1. Introduction to Windows


Windows is a widely used, feature-rich operating system.

Practice using a Windows VM with provided credentials.

The module covers basic Windows components and administration.

2. Windows Editions
Windows versions: XP → Vista → 7 → 8.x → 10 → 11.

Windows 10 support ends Oct 2025; Windows 11 is the latest desktop version.

Editions include Home and Pro; Pro supports features like BitLocker encryption.

The VM uses Windows Server 2019 Standard edition.

3. The Desktop (GUI)
The Desktop appears after login (requires username/password).

Key components: Desktop, Start Menu, Search Box (Cortana), Task View, Taskbar, Toolbars, Notification Area.

Desktop contains shortcuts and can be personalized (right-click to access options).

Start Menu sections: user shortcuts (account settings, power options), recently added apps and full app list, and live tiles.

Taskbar shows open/pinned apps; hovering shows preview thumbnails.

Notification Area includes clock, network, volume, and Action Center icons.

4. File System
Windows uses NTFS (New Technology File System).

NTFS supports large files (>4GB), permissions, compression, and encryption (EFS).

Older FAT16/FAT32 still used on USB drives and SD cards.

NTFS is journaling, allowing recovery after crashes.

Permissions include Full Control, Modify, Read & Execute, List Folder Contents, Read, Write.

Alternate Data Streams (ADS) allow extra data attached to files, sometimes used by malware.

5. Windows\System32 Folder
The %windir%\System32 folder contains critical system files.

Deleting/modifying System32 files can break Windows.

Many Windows tools reside in System32.

%windir% is an environment variable pointing to the Windows folder location.

6. User Accounts, Profiles, and Permissions
Two main account types: Administrator (full system control) and Standard User (limited to personal files).

User profiles stored in C:\Users\Username. Created at first login.

Users belong to groups (e.g., Users, Remote Desktop Users) that define permissions.

Use lusrmgr.msc (Local Users and Groups) to view/manage accounts and groups.

7. User Account Control (UAC)
Prevents programs from running with elevated rights unless authorized.

Admins don’t run with full privileges by default; UAC prompts on high-privilege actions.

The shield icon indicates programs that require elevation.

UAC helps reduce malware risk by requiring explicit permission for system changes.

8. Settings and Control Panel
Two interfaces for system settings: modern Settings and legacy Control Panel.

Settings is touch-friendly and the primary interface in Windows 10.

Control Panel is for advanced settings; some Settings options open Control Panel dialogs.

Use Start Menu search to find where to change settings (Settings or Control Panel).

Example: Changing wallpaper is done via Settings.

9. Task Manager
Shows running apps, processes, CPU/RAM usage, and more.

Open via right-clicking taskbar or shortcut Ctrl+Shift+Esc.

Starts in Simple View; click “More details” for full information.

Useful for monitoring system health and troubleshooting.

Key Terms & Shortcuts
NTFS: New Technology File System

%windir%: Environment variable for Windows folder

UAC: User Account Control

lusrmgr.msc: Local Users and Groups management console

Task Manager shortcut: Ctrl + Shift + Esc

