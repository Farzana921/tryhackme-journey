Windows Fundamentals Summary


🔗 Room Link: [Windows Fundamentals 1](https://tryhackme.com/room/windowsfundamentals1xbx)


## 1. Introduction to Windows  
Windows is a complex operating system with many components including system files, utilities, and settings. This overview covers the basic navigation, system changes, and key Windows features. A virtual machine can be used for hands-on practice.

## 2. Windows Editions  
- Windows has evolved since 1985 and dominates both home and corporate use.  
- Popular versions: XP, Vista (poorly received), 7, 8.x (short-lived), 10, and the current Windows 11 (Home and Pro).  
- Windows Server 2019 Standard is used for servers (VM edition here).  
- Pro edition supports BitLocker encryption; Home does not.

## 3. The Desktop (GUI)  
- The GUI includes components like the Desktop, Start Menu, Search Box (Cortana), Task View, Taskbar, Toolbars, and Notification Area.  
- Desktop contains shortcuts and files for quick access; it’s customizable via right-click options and Personalize settings.  
- The Start Menu offers access to apps, settings, and power options, organized with recently added and alphabetized apps, plus tiles for pinned apps.  
- Taskbar shows running apps; icons can be pinned or previewed on hover.  
- Notification Area displays time, volume, network, and Action Center icons.

## 4. The File System  
- Modern Windows uses NTFS (New Technology File System), which supports:  
  - Files larger than 4GB  
  - Permissions on files/folders  
  - Compression and encryption (EFS)  
- NTFS is a journaling file system that can self-repair after crashes.  
- Permissions include Full Control, Modify, Read & Execute, etc.  
- Alternate Data Streams (ADS) allow hidden data streams within files, sometimes used maliciously.

## 5. The Windows\System32 Folder  
- Located under the Windows directory (environment variable `%windir%`).  
- Contains critical system files; accidental deletion can break the OS.  
- Many essential Windows tools reside here.

## 6. User Accounts, Profiles, and Permissions  
- Two main user types: Administrator (full control) and Standard User (limited).  
- User profiles are created at first login under `C:\Users\Username`.  
- User and group management is done via `lusrmgr.msc`, where users can be assigned to groups with defined permissions.

## 7. User Account Control (UAC)  
- Protects systems by running admin users with standard privileges by default.  
- When elevated privileges are needed, UAC prompts for confirmation or credentials.  
- Helps reduce malware risk by limiting automatic admin rights.

## 8. Settings and Control Panel  
- Two main interfaces for system configuration:  
  - **Settings** (modern interface introduced in Windows 8, touch-friendly)  
  - **Control Panel** (traditional interface with more advanced options)  
- Some settings start in Settings but open Control Panel for detailed configuration.

## 9. Task Manager  
- Shows running applications, processes, CPU, and RAM usage.  
- Access by right-clicking the taskbar or pressing `Ctrl+Shift+Esc`.  
- Default view is simple; “More details” reveals extensive info.