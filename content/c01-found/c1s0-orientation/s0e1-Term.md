---
title: "C1S0E1: Installing Windows Terminal"
description: Install and configure Windows Terminal for a better command-line experience on Windows.
tags:
  - windows-terminal
  - setup
  - tools
  - beginner
  - workbook
  - windows
draft: false
date: 2026-01-30
---
#  Exercise 1: Installing Windows Terminal
In this exercise you will be downloading and installing the Windows Terminal application. 

---
## Getting Started
Windows Terminal gives you access to the Command Line(CL) which is a powerful text base interface.
### Prerequisites
Make sure you have:

- A Windows computer (Turn it on)
- Reliable Internet Connection
- Access to the Microsoft Store (or ability to download from GitHub)
- About 5 minutes
### What to Expect?
By the end of this exercise, you will have:

- Windows Terminal (also called the Command Line Interface) installed
- Windows Terminal configured as your default terminal
- Verified that Windows Terminal is working

**Note:** Windows Terminal is optional but recommended. If you prefer, you can skip this exercise and use Git Bash directly (which you'll install in the next exercise).

---
## Step 1: Install Windows Terminal

Instructions
1. Press the Windows key![](windows-key-icon.png)
2. Type "Microsoft store" and press Enter
3. In the store, search for "windows terminal"
4. Click on [Windows Terminal](https://apps.microsoft.com/detail/9N0DX20HK701?hl=en-us&gl=US&ocid=pdpshare) (published by Microsoft Corporation)
5. Click **Install** or **Get**
6. Wait for installation to complete

**Alternative method (if store doesn't work):**
1. Go to [github.com/microsoft/terminal/releases](https://github.com/microsoft/terminal/releases)
2. Download the latest [.msixbundle ](https://github.com/microsoft/terminal/releases/tag/v1.23.20211.0)file
3. Double-click to install

### Verify
1. Press the Windows key![](windows-key-icon.png)
2. Type "windows terminal"
3. Press Enter
4. Windows Terminal should open

If Windows Terminal opens, the installation is successful.

---
## Step 2: Configure Windows Terminal (Optional)

### What This Step Does
This sets up Windows Terminal to use [Git Bash](https://git-scm.com/video/what-is-git) as a profile option (you'll install Git Bash in the next exercise).
### Instructions
1. Open Windows Terminal
2. Click the dropdown arrow next to the new tab button
3. You should see options like "powershell", "command prompt", etc.
4. ![](ss-terminal-opts.png)
5. After you install Git Bash (in Exercise 2), it will automatically appear here

**Note:** We'll configure Git Bash integration after installing Git in Exercise 2.

### Verify
You should see:
- ✅ Windows Terminal opens successfully
- ✅ You can see the terminal interface
- ✅ You can create new tabs

---
## Expected State at the End of This Exercise

You should now have:
- **Windows Terminal**: Installed and accessible from the start menu
- **Basic Configuration**: Ready to add Git Bash in the next exercise

---
## Why This Matters

Windows Terminal provides:
- Better visual experience than default command prompt
- Multiple tabs for different shells
- Better customization options
- Integration with Git Bash, PowerShell, and other tools

While optional, Windows Terminal makes working with the command line more pleasant and professional.

---
#### Next Steps: Return to the [Orientation Lecture](c01-found/c1s0-orientation/index.md#Introduction-to-git-and-versionc-control)
2. Introduction to Git and Version Control

---
## Navigation
[Back to the Top](#Getting%20Started)
### Section 0 Map
- [C1S0E1:](s0e1-Term.md) Installing Windows Terminal
- [C1S0E2:](s0e2-gitbash.md) Installing Git Bash
- [C1S0E3:](s0e3-vscode.md) Installing VS Code
- [C1S0E4:](s0e4-github.md) Create and Configure Your GitHub Account
- [C1S0E5:](s0e5-desktop.md) Installing GitHub Desktop
- [C1S0E6:](s0e6-opts.md) Installing Optional Tools

---
### Global Navigation
- [HOME:](index) JASYTI's Full Stack Development Foundations Course -
- [Course 01:](c01-found/index) Foundations of Front End Development
- [Course 02:](c02-genai-fun/index.md) Fundamentals of Generative AI
- [Course 03:](c03-fe-react/index) Designing a Dynamic Frontend with React
- [Course 04:](c04-genai-design/index.md) Harnessing Gen AI: From Design to Code Optimization
- [Course 05:](c05-data/index) Understanding Data Structures and Algorithms
- [Course 06:](c06-mongol/index) Using MongoDB to Design and Manage Databases
- [Course 07:](c07-express/index) Developing a Reliable Back-end with Node and Express
- [Course:08](c08-ai-test/index) The Power of Generative AI Software Testing
- [Course 09:](c09-publish/index) Publishing your Website to the Live Internet
