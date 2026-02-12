---
title: "C1S1: Orientation: Getting Started in Your Windows Environment"
description: Set up your Windows development environment and learn about the essential developer tools you'll use throughout this course and your career.
tags:
  - orientation
  - windows
  - setup
  - tools
  - prerequisites
draft: false
date: 2026-01-30
---

# Orientation: Getting Started in Your Windows Environment

Welcome to the orientation! Before you start building web applications, you need to set up your development environment. This section will guide you through installing and configuring the essential tools you'll use throughout this course.

---

## Prerequisites for Success

You don't need any prior programming experience to start this course, but here's what will help you succeed:

### Essential Requirements

- **A Windows Computer**: This course is taught for Windows users. While most development concepts are the same across Windows, Mac, and Linux, the instructions and examples in this course are Windows-specific. If you're using Mac or Linux, you may need to do additional research to adapt certain steps to your system.

- **Internet Connection**: You'll need reliable internet to access  essential web-based resources like GitHub, download tools, and of course access this material.

- **Time Commitment**: Set aside regular time for practice. Consistency matters more than long sessions. You should be able to do at least one reading assignment and exercise in 30 min or less each day.

- **Curiosity and Patience**: Learning to code takes time. Be patient with yourself and stay curious

- **Problem-Solving Mindset**: Enjoying puzzles and logical thinking will help you get through the hard parts and make the easy stuff more enjoyable.
### Basic Computer Skills Expected

This course assumes you have basic computer skills. We won't teach you how to:
- Open File Explorer or navigate folders
- Open a terminal or command prompt
- Create, rename, or delete files and folders
- Use basic keyboard shortcuts (copy, paste, save, etc.)

**We will teach you:**
- How to use the command line once it's open
- Git commands and workflows
- How to use VS Code
- Programming concepts and syntax

If you need help with basic computer operations (like opening a terminal or navigating File Explorer), use ChatGPT, Google, or other resources to fill those knowledge gaps. This keeps the course material focused on development skills rather than basic computer literacy.

**Most students will never have worked in a command-line environment before.** That's okay—we'll take you through how to use the command line interface step by step. You just need to be able to open it first.

### Helpful (But Not Required)

- **Attention to Detail**: Programming requires precision—small details matter. Get right the first time and save hours of debugging.
- **Willingness to Practice**: The more you code, the better you'll become
- **Comfort with Self-Directed Learning**: Being able to look up basic OS operations when needed (Google is your friend)

---

## Course Environment: Windows Focus

This course is designed for **Windows users**. While the core development concepts (Git, HTML, CSS, JavaScript) work the same across all operating systems, the specific instructions, file paths, and tool setup in this course are Windows-focused.

**If you're using Mac or Linux:**
- Most concepts will translate directly
- File paths may differ (Windows uses `\`, Mac/Linux use `/`)
- Some installation steps may vary
- Terminal commands are generally the same, but some Windows-specific commands won't apply
- You may need to do additional research to adapt certain steps

**Why Windows?**
Because I have a PC and I don't speak MAC, and...

Windows is the most widely used operating system, and many professional development environments run on Windows. Learning on Windows prepares you for the most common professional scenario. 

**If you encounter platform-specific issues:**
- Use ChatGPT or Google to find Mac/Linux equivalents
- The core concepts remain the same—only the specific commands or paths may differ
- Focus on understanding the "why" behind each step, not just the "what"

---

## Introduction to Command Line Interface 
Here comes the learning part (so pay attention)

Before you can start developing, you need to understand the command line. This is a fundamental tool that developers use daily.
### What is a Command Line?

A **command line** (also called terminal, console, or shell) is a text-based interface for interacting with your computer. Instead of clicking icons and menus, you type commands and see text output.

The command line comes in many shapes sizes and colors.
![](terminals.png)
But they all pretty much do the same thing.  Some are platform specific and others work universally.  We will be using the Terminal in VS Code for the most part.  I You will learn how to set ip up in this section.

**Why developers use command line:**
- The CL is much faster than graphical interfaces for most tasks
- It very easy to automate repetitive tasks
- The CL works the same across different operating systems
- It is essentially required for many development tools (Git, Node.js, etc.)
- You will be expected to know how to use the command line, because your peers, prospective employers, and other professional developers use it regularly
### Windows Terminal (Command Line Tool)
![[ss-terminal.png]]
The [Windows Terminal](https://www.bing.com/ck/a?!&&p=234f3d182e978cdd9ea4c77df3a19442304b6d55695ba2e5981358cf9c250113JmltdHM9MTc3MDg1NDQwMA&ptn=3&ver=2&hsh=4&fclid=07f802bb-eb29-6f86-2b0a-1404ea816ee4&u=a1aHR0cHM6Ly9lbi53aWtpcGVkaWEub3JnL3dpa2kvV2luZG93c19UZXJtaW5hbA) is Microsoft's modern terminal application for Windows. 

Windows Terminal is an upgraded version of the traditional Command Prompt window. Instead of opening separate black windows for different tools, it allows you to run multiple command-line environments inside one organized application.

**What it does:**

- You can open multiple tabs, just like a web browser. One tab might run Command Prompt, another PowerShell, and another Git Bash.
- You can switch between different shells without opening separate programs.
- It supports customization such as font size, themes, and layout, which makes long sessions easier on your eyes.
- It provides better compatibility with modern development tools.

---

### Why We Use It

- It is widely used in Windows development environments.
- It allows you to work with Git, Node, PowerShell, and other tools in one place.
- It keeps your workflow organized when managing projects.
- It makes command-line work cleaner and more manageable, especially as projects grow.

Now that you understand what a terminal is and why it matters, you're ready to install Windows Terminal. Complete [Exercise 1: Installing Windows Terminal](c01-found/s0-welcome/exercise-1-installing-windows-terminal) to set up your command-line environment.

---

## Introduction to Git and Version Control

**Git** is a version control system—a tool that tracks changes to your files over time. Think of it like a time machine for your code.

### What is Version Control?

Version control lets you:
- See what changed and when
- Go back to previous versions if something breaks
- Work on different features simultaneously (using branches)
- Collaborate with others without conflicts
- Keep a history of all your work

**Why version control matters:**
- Professional developers use it for every project
- It's essential for collaboration
- It protects you from losing work
- It helps you understand how your project evolved

### Git Bash
![[ss-gbterm.png]]
**Git Bash** is a command-line interface that comes with Git for Windows. It provides:
- Access to Git commands
- A Unix-like shell environment
- Tools for working with files and directories
- Integration with Windows Terminal

**Why we use Git Bash:**
- Git commands work the same across all platforms
- Professional developers use command-line Git regularly
- Gives you more control and flexibility
- Works alongside graphical tools like GitHub Desktop

Now that you understand Git and version control, you're ready to install Git. Complete [[s0-welcome/exercise-2-installing-git-bash|Exercise 2: Installing Git Bash]] to set up version control on your computer.

---

## Introduction to Code Editors

A **code editor** is a specialized text editor designed for writing code. While you could write code in Notepad, code editors provide features that make development much easier.

### What Code Editors Provide

- **Syntax Highlighting**: Colors code to make it easier to read
- **Auto-completion**: Suggests code as you type
- **Error Detection**: Highlights mistakes before you run your code
- **Integrated Terminal**: Run commands without leaving the editor
- **Extensions**: Add features for specific languages and tools
- **Git Integration**: See file changes and commit directly from the editor
### Visual Studio Code (VS Code)
![[ss-vs-code.png]]
**Visual Studio Code** has become the industry standard for code editors. Here's why:

- **Free and Open Source** - Available to everyone, regardless of budget
- **Extensible** - Thousands of extensions available
- **Cross-Platform** - Works on Windows, Mac, and Linux
- **Widely Adopted** - Most developers and teams use it
- **Well-Supported** - Regular updates and strong community support

When you use VS Code, you're using the same tool that most developers use. This means:
- Tutorials and guides are written for VS Code
- Your teammates can help you with VS Code-specific questions
- Extensions and plugins are readily available
- You'll fit into most development teams

**That's why we use VS Code in this course.** It's not the only good editor, but it's the one you're most likely to encounter in professional settings.

Now that you understand code editors and why VS Code is the standard, you're ready to install it. Complete [[s0-welcome/exercise-3-installing-vs-code|Exercise 3: Installing VS Code]] to set up your code editor.

---

## Introduction to GitHub

**GitHub** is a website that hosts Git repositories online. Think of it as cloud storage specifically designed for code.

### What GitHub Provides

- **Online Backup**: Your code is stored in the cloud, safe from computer failures
- **Portfolio**: Your GitHub profile becomes a showcase of your work
- **Collaboration**: Share code with others and work on projects together
- **Version History**: See all changes to your code over time
- **Access Anywhere**: Work on your code from any computer

### Why You Need a GitHub Account

Even though you'll primarily use command-line Git, you need a GitHub account to:
- Store your repositories online (backup and access)
- Build your professional portfolio
- Learn how Git and GitHub work together
- Prepare for collaboration in professional settings

**GitHub accounts are free** and essential for modern web development. Every professional developer has one.

Now that you understand what GitHub is and why you need it, you're ready to create your account. Complete [[s0-welcome/exercise-4-creating-github-account|Exercise 4: Creating GitHub Account]] to set up your GitHub account.

---

## Introduction to GitHub Desktop

**GitHub Desktop** is a visual interface for Git and GitHub. While this course focuses on command-line Git (the industry standard), GitHub Desktop provides a helpful visual way to understand Git concepts.

### What GitHub Desktop Provides

- **Visual Interface**: See your changes, commits, and history in a graphical format
- **Easier Learning**: Understand Git concepts visually before mastering command-line
- **Quick Operations**: Perform common Git tasks with clicks instead of commands
- **Integration**: Works seamlessly with your GitHub account

### Why Install It Now

While you'll primarily use command-line Git in this course (because that's what employers expect), GitHub Desktop helps you:
- **Visualize Git concepts** as you learn them
- **Understand the workflow** before memorizing commands
- **Have a backup tool** if you get stuck with command-line
- **See the big picture** of how Git and GitHub work together

**Note:** This course teaches command-line Git because it's the professional standard. GitHub Desktop is a learning aid and backup tool, not the primary method you'll use.

Now that you understand GitHub Desktop and its role as a learning tool, you're ready to install it. Complete [[s0-welcome/exercise-5-installing-github-desktop|Exercise 5: Installing GitHub Desktop]] to set up the visual interface.

---

## Tools You'll Install in This Section

In the exercises below, you'll install:
- **Windows Terminal** - Modern terminal application (optional but recommended)
- **Git for Windows** - Version control system (includes Git Bash)
- **VS Code** - Industry-standard code editor
- **GitHub Account** - Online code hosting platform
- **GitHub Desktop** - Visual interface for Git and GitHub

**Later in the course:**
- **Node.js** - JavaScript runtime (installed in a later section)
- **Browser Developer Tools** - Already in your web browser

Don't worry if these sound unfamiliar now. We'll walk you through everything step by step.

---

## How This Course Is Structured

This course follows a **section/lecture/exercise** structure, similar to how technical manuals are organized:

- **Section**: Overall concept folder (orientation, file-systems, version-control)
- **Lecture (index.md)**: Comprehensive lecture covering ALL concepts for that section (like a PowerPoint/PDF lesson)
- **Exercises (exercise-N-name.md)**: Focused exercises, each covering ONE specific concept from the lecture

**Learning Pattern:**
1. Read the comprehensive lecture (index.md) to understand all concepts
2. Complete focused exercises (exercise-1.md, exercise-2.md, etc.) to practice individual concepts
3. Each exercise reinforces one specific concept from the lecture
4. Complete the section Capstone (blends all section lessons into one final project)

This structure allows you to:
- Get the big picture from the lecture
- Practice concepts individually through exercises
- Jump to any exercise if you already understand the prerequisite concepts
- Work at your own pace

---

---

## Ready to Begin?

When you're ready to start, complete the exercises above to set up your development environment. Once you have all tools installed, proceed to [[s1-files/index|Section 1: File Systems and Organization]] to understand how course materials are organized, followed by [[s2-vers-ctrl/index|Section 2: Version Control Foundations]] to begin building your first repository.

Good luck, and welcome to the journey of becoming a full stack engineer!

**Next Steps:** [[s1-files/index|Section 1: File Systems and Organization]] - Learn about file organization principles. 

---
## Exercises in This Section

Complete these exercises in order to set up your development environment:

1. **[[s0-welcome/exercise-1-installing-windows-terminal|Exercise 1: Installing Windows Terminal]]**
   - Install and configure Windows Terminal
   - Learn basic terminal navigation
   - Set up your command-line environment

2. **[[s0-welcome/exercise-2-installing-git-bash|Exercise 2: Installing Git Bash]]**
   - Install Git for Windows
   - Verify Git installation
   - Integrate Git Bash with Windows Terminal

3. **[[s0-welcome/exercise-3-installing-vs-code|Exercise 3: Installing VS Code]]**
   - Install Visual Studio Code
   - Configure terminal integration
   - Set up your code editor

4. **[[s0-welcome/exercise-4-creating-github-account|Exercise 4: Creating GitHub Account]]**
   - Create and verify your GitHub account
   - Set up your profile
   - Understand the GitHub interface

5. **[[s0-welcome/exercise-5-installing-github-desktop|Exercise 5: Installing GitHub Desktop]]**
   - Install GitHub Desktop
   - Sign in to your GitHub account
   - Learn the basic interface
---
## Navigation

### Section Navigation
- [[r61-fsd-university/content/c01-found/s0-welcome/index|Home]] - Return to the main course page
- [[s0-welcome/index|Orientation]] - This page
- [[s1-files/index|File Systems]] - Next section

### Course Sections
- [[r61-fsd-university/content/c01-found/s0-welcome/index|Home]] - Return to the main course page
- [[s0-welcome/index|Section 0: Orientation]] - Get started here
- [[s1-files/index|Section 1: File Systems]] - Organization principles
- [[s2-vers-ctrl/index|Section 2: Version Control]] - Git and GitHub basics
- [[s3-html-css/index|Section 3: HTML & CSS]] - Web page fundamentals
- [[s4-js/index|Section 4: JavaScript Basics]] - Programming fundamentals
- [[s5-opt-js/index|Section 5: JavaScript Functions]] - Functions and optimization
- [[s6-adv-js/index|Section 6: Advanced JavaScript]] - Advanced concepts
- [[s7-tailwind/index|Section 7: Tailwind CSS]] - Modern styling
- [[s8-tailwind-adv/index|Section 8: Advanced Tailwind]] - Advanced styling
