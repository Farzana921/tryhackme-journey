# Linux Fundamentals Part 1 Summary

🔗 Room Link: [Red Team Engagements](https://tryhackme.com/room/linuxfundamentalspart1)

## Introduction

Welcome to the first part of the **"Linux Fundamentals"** room series.

- Linux is just another operating system like Windows or macOS.
- It powers smart cars, Android devices, supercomputers, enterprise servers, and more.
- This module introduces:
  - Running Linux commands in-browser
  - Basic filesystem commands
  - File searching and shell operators



## A Bit of Background on Linux

### Where is Linux Used?

Linux powers:
- Websites
- Car entertainment systems
- Point of Sale (PoS) systems
- Critical infrastructure (traffic lights, sensors)

### Flavours of Linux

- "Linux" refers to many operating systems based on UNIX.
- Common distributions: **Ubuntu**, **Debian**
- We're using **Ubuntu** in this course.
- Ubuntu Server can run on just **512MB RAM**.

> 🗓 **First Linux OS release**: 1991



## Interacting with Your First Linux Machine

- Launch via the green **Start Machine** button.
- Once deployed, you'll get:
  - IP address
  - Expiry timer
  - Machine controls
- All interaction is done via the **terminal** (no GUI).



## 🧪 Running Your First Few Commands

### Terminal Basics

- **Terminal**: A text-based interface to run commands.

### Key Commands

| Command   | Description                        |
|----------|------------------------------------|
| `echo`   | Output any text you provide        |
| `whoami` | Shows current logged-in user       |

#### Examples
```bash
echo Hello
echo "Hello Friend!"
whoami
