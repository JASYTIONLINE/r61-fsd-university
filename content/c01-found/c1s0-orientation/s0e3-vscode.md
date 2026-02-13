---
title: "C1S0E3: Installing VS Code"
description: Install and configure Visual Studio Code, the industry-standard code editor.
tags:
  - vs-code
  - setup
  - tools
  - beginner
  - workbook
  - windows
draft: false
date: 2026-01-30
---
# Exercise 3 Installing VS Code
In this excercise you wil download install and configure VS Code.

## Getting Started
VS Code is the industry-standard code editor. This is where you'll write all your code throughout this course.
### Prerequisites
Before You Start-Make sure you have:

- A Windows computer with administrator access
- A working internet connection
- About 5-10 minutes
- Git Bash installed (from Exercise 2)
### What to Expect
By the end of this exercise, you will have:

- Visual Studio Code installed on your computer
- VS Code configured with terminal access
- Verified that VS Code is working correctly
- **Important:** If you're using Mac or Linux, the installation process differs. Use ChatGPT or Google to find the equivalent steps for your operating system.

---
## Step 1: Download VS Code

### What This Step Does
This downloads the VS Code installer to your computer.
#### Instructions
1. Open your web browser
2. Go to [code.visualstudio.com](https://code.visualstudio.com)
3. Click **Download for Windows** (stable build)
4. The download should start automatically
5. Wait for the download to complete
### Verify
You should see a file named something like `vscodeusersetup-x.x.x.exe` in your downloads folder.

---
## Step 2: Install VS Code

### What This Step Does
This installs VS Code on your computer and sets up important integrations.
#### Instructions
1. Find the downloaded file in your downloads folder
2. Double-click the installer (vscodeusersetup-x.x.x.exe)
3. If Windows asks for permission, click **Yes**
4. Follow the installation wizard:
   - Accept the license agreement
   - Choose installation location (default is fine)
   - **Select additional tasks**: Check these boxes:
     - ✅ Add "open with code" action to Windows Explorer file context menu
     - ✅ Add "open with code" action to Windows Explorer directory context menu
     - ✅ Add to path (this allows you to use `code` command in terminal)
   - Click **Next** and then **Install**
5. Wait for installation to complete (this may take a few minutes)
6. Click **Finish**
7. Check the box to launch VS Code
### Verify
1. VS Code should open automatically
2. You should see the welcome screen with options like "new file", "open folder", etc.
3. If VS Code didn't open, press the Windows key, type "visual studio code", and press Enter

If you can see the VS Code interface, the installation is successful.

---
## Step 3: Verify Terminal Access

### What This Step Does
This confirms that VS Code can access the terminal, which you'll use throughout the course.

#### Instructions
1. In VS Code, open the integrated terminal:
   - Press `Ctrl + ~` (control key + tilde key)
   - Or go to **Terminal** → **New Terminal** in the menu bar
2. A terminal panel should appear at the bottom of VS Code
3. You should see a command prompt (something like `PS C:\Users\YourName>` or a Git Bash prompt)

### Verify
You should see:
- ✅ A terminal panel at the bottom of VS Code
- ✅ A command prompt ready for input
- ✅ The terminal is functional (you can type in it)

If you can see and use the terminal, VS Code is fully set up.

---
## Step 4: Verify Git Integration (Optional)

### What This Step Does
This confirms that VS Code can detect Git, which you installed in Exercise 2.
#### Instructions
1. In VS Code, open a folder (File → Open Folder)
2. Choose any folder on your computer
3. VS Code should detect if the folder is a Git repository (if it is, you'll see Git information in the sidebar)

**Note:** You don't have a Git repository yet—that's fine. We're just verifying that VS Code can work with Git when you create one.
### Verify
VS Code should:
- ✅ Open folders without errors
- ✅ Show the file explorer in the sidebar
- ✅ Be ready to work with Git repositories (when you create them)

---
## Expected State at the End of This Exercise

You should now have:
- **Visual Studio Code**: Installed and accessible from the start menu
- **Terminal Access**: Working integrated terminal in VS Code
- **File Associations**: Can right-click files/folders and "open with code"

---
## Why This Matters

VS Code is the industry-standard code editor. By installing it now, you're:
- Using the same tool most professional developers use
- Preparing for all future exercises in this course
- Setting up a professional development environment

Every exercise from now on will use VS Code. You're ready to start coding.

---
#### Next Steps: Return to the [[c01-found/c1s0-orientation/index|Orientation Lecture]] 
4. Introduction to GitHub

---
## Troubleshooting

If something didn't work:

1. **VS Code won't install**: Make sure you have administrator rights. Right-click the installer and choose "run as administrator."

2. **Terminal won't open**: Try restarting VS Code. If that doesn't work, go to **View** → **Terminal** in the menu.

3. **Can't find VS Code after installation**: Press Windows key, type "visual studio code", and it should appear.

If you're still stuck, use ChatGPT or Google to search for your specific error message.

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
