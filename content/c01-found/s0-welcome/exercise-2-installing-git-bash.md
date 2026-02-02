---
title: "Exercise 2: Installing Git Bash"
description: "Install Git for Windows, which includes Git Bash for command-line version control."
tags: [git, git-bash, setup, tools, beginner, workbook, windows]
draft: false
date: "2026-01-30"
---

# Exercise 2: Installing Git Bash

This exercise is written so you can complete it **without an instructor present**.
Read each section fully before performing the steps.

This exercise is part of the [[s0-welcome/index|Orientation section]]. Git is the foundation of version control, and Git Bash provides a command-line interface for using Git on Windows.

---

## What You Are Building

By the end of this exercise, you will have:
- Git for Windows installed
- Git Bash accessible and working
- Git configured and ready to use
- Git integrated with Windows Terminal (if you installed it in Exercise 1)

---

## Before You Start

Make sure you have:
- A Windows computer with administrator access
- A working internet connection
- About 10-15 minutes
- Windows Terminal installed (from Exercise 1, optional but recommended)

---

## Step 1: Download Git for Windows

### What This Step Does
This downloads the Git installer to your computer.

### Instructions
1. Open your web browser
2. Go to [git-scm.com/download/win](https://git-scm.com/download/win)
3. The download should start automatically
4. If it doesn't, click the download button
5. Wait for the download to complete

### Verify
You should see a file named something like `git-x.x.x-64-bit.exe` in your downloads folder.

---

## Step 2: Install Git for Windows

### What This Step Does
This installs Git and Git Bash on your computer with the recommended settings.

### Instructions
1. Find the downloaded file in your downloads folder
2. Double-click the installer (git-x.x.x-64-bit.exe)
3. If Windows asks for permission, click **Yes**
4. Follow the installation wizard:
   - **Select components**: Leave all default options checked
   - **Default editor**: If you see the option, choose "use visual studio code as git's default editor"
   - **Adjusting your path environment**: Choose **"git from the command line and also from 3rd-party software"** (recommended)
   - **Choosing https transport backend**: Use the default openssl library
   - **Line ending conversions**: Choose "checkout windows-style, commit unix-style line endings" (default)
   - **Terminal emulator**: Choose "use windows' default console window"
   - **Default behavior**: Use the default options
5. Click **Install** and wait for installation to complete
6. Click **Finish**

### Verify
1. Press the Windows key
2. Type "git bash"
3. Press Enter
4. A terminal window should open
5. You should see a prompt ending with `$` (like `username@computername MINGW64 ~ $`)

If you can see the Git Bash prompt, Git is installed correctly.

---

## Step 3: Verify Git Installation

### What This Step Does
This confirms that Git is installed and accessible from the command line.

### Instructions
1. In Git Bash, type: `git --version`
2. Press Enter
3. You should see something like: `git version 2.x.x`

### Verify
You should see:
- ✅ A version number displayed (like `git version 2.42.0`)
- ✅ No error messages

If you see a version number, Git is installed and working.

**Note:** You don't need to understand what that command does yet. We're just verifying the installation works.

---

## Step 4: Integrate Git Bash with Windows Terminal (Optional)

### What This Step Does
If you installed Windows Terminal, this adds Git Bash as a profile option.

### Instructions
1. Open Windows Terminal
2. Click the dropdown arrow next to the new tab button
3. You should now see "git bash" as an option
4. Click on "git bash"
5. A new tab should open with Git Bash

**Note:** If Git Bash doesn't appear automatically, it should after a restart. If it still doesn't appear, you can manually add it later.

### Verify
You should see:
- ✅ Git Bash available as a profile in Windows Terminal
- ✅ You can open Git Bash from Windows Terminal
- ✅ Git commands work in the Windows Terminal Git Bash tab

---

## Expected State at the End of This Exercise

You should now have:
- **Git for Windows**: Installed and working
- **Git Bash**: Accessible from start menu and Windows Terminal
- **Git command**: Working from command line (`git --version` shows a version)

---

## Why This Matters

Git is the foundation of version control. By installing it now, you're:
- Setting up the tool you'll use for all version control in this course
- Preparing to work with GitHub
- Learning industry-standard version control

In later sections, you'll learn how to use Git and authenticate with GitHub from the command line.

---

## Next Steps

- [[s0-welcome/index|Orientation Lecture]] - Return to the lecture and move on to the next exercise in the setup sequence.

---

## Troubleshooting

If something didn't work:

1. **Git not found in terminal**: Make sure you selected "git from the command line" during installation. You may need to restart your computer.

2. **Git Bash won't open**: Try restarting your computer, then try again.

3. **Installation failed**: Make sure you have administrator rights. Right-click the installer and choose "run as administrator."

If you're still stuck, use ChatGPT or Google to search for your specific error message.

---

## Navigation

### Section Navigation
- [[index|Home]] - Return to main course page
- [[s0-welcome/index|Orientation Index]] - Return to orientation overview
- [[s0-welcome/exercise-1-installing-windows-terminal|Exercise 1: Installing Windows Terminal]] - Previous exercise
- [[s0-welcome/exercise-2-installing-git-bash|Exercise 2: Installing Git Bash]] - This page
- [[s0-welcome/exercise-3-installing-vs-code|Exercise 3: Installing VS Code]] - Next exercise

### Related Materials
- [[s0-welcome/index|Orientation Lecture]] - Review the concepts
