---
title: "Orientation: So You Want to be an Engineer?"
description: "Comprehensive orientation covering full stack engineering, course structure, prerequisites, and introduction to essential development tools."
tags: [orientation, full-stack, introduction, prerequisites, tools]
draft: false
date: "2026-01-30"
---

# Orientation: So You Want to be an Engineer?

Welcome! You're about to embark on a journey to become a **full stack engineer**. This comprehensive orientation will help you understand what that means, what you'll need to succeed, and what lies ahead in this course.

---

## What is a Full Stack Engineer?

A **full stack engineer** is a developer who can work on both the **front-end** and **back-end** of web applications. This means you'll be able to:

- **Front-end Development**: Build the user interface that people see and interact with in their browsers. This includes HTML, CSS, JavaScript, and modern frameworks like React.

- **Back-end Development**: Create the server-side logic, databases, and APIs that power web applications. This includes working with Node.js, Express, and databases like MongoDB.

- **Full Stack Integration**: Connect front-end and back-end systems to create complete, functional web applications.

The term "full stack" refers to working across the entire technology stack—from the user interface all the way down to the database and server infrastructure.

---

## What This Course Covers

This course is part of a comprehensive full stack development program that will teach you the **MERN stack**:

- **M**ongoDB - Database for storing application data
- **E**xpress - Web framework for building APIs and server logic
- **R**eact - Front-end library for building interactive user interfaces
- **N**ode.js - JavaScript runtime for server-side development

In this **Foundations of Front-end Development** section, we focus on building the essential skills you'll need:

1. **File Systems and Organization** - Understanding why logical file structures matter and how to organize projects professionally
2. **Version Control** - Professional Git and GitHub workflows
3. **HTML & CSS** - Building and styling web pages
4. **JavaScript Fundamentals** - Core programming concepts
5. **Advanced JavaScript** - Functions, optimization, and modern features
6. **Modern Tools** - Tailwind CSS and advanced front-end techniques

Each lesson builds on the previous one, and you'll work with a single repository that becomes a portfolio piece demonstrating your professional development skills.

---

## Prerequisites for Success

You don't need any prior programming experience to start this course, but here's what will help you succeed:

### Essential Requirements

- **A Windows Computer**: This course is taught for Windows users. While most development concepts are the same across Windows, Mac, and Linux, the instructions and examples in this course are Windows-specific. If you're using Mac or Linux, you may need to do additional research to adapt certain steps to your system.

- **Internet Connection**: You'll need reliable internet to access GitHub, download tools, and follow along

- **Time Commitment**: Set aside regular time for practice. Consistency matters more than long sessions

- **Curiosity and Patience**: Learning to code takes time. Be patient with yourself and stay curious

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

- **Problem-Solving Mindset**: Enjoying puzzles and logical thinking will help
- **Attention to Detail**: Programming requires precision—small details matter
- **Willingness to Practice**: The more you code, the better you'll become
- **Comfort with Self-Directed Learning**: Being able to look up basic OS operations when needed

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
Windows is the most widely used operating system, and many professional development environments run on Windows. Learning on Windows prepares you for the most common professional scenario.

**If you encounter platform-specific issues:**
- Use ChatGPT or Google to find Mac/Linux equivalents
- The core concepts remain the same—only the specific commands or paths may differ
- Focus on understanding the "why" behind each step, not just the "what"

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

This structure allows you to:
- Get the big picture from the lecture
- Practice concepts individually through exercises
- Jump to any exercise if you already understand the prerequisite concepts
- Work at your own pace

---

## Introduction to Command Line Interface

Before you can start developing, you need to understand the command line. This is a fundamental tool that developers use daily.

### What is a Command Line?

A **command line** (also called terminal, console, or shell) is a text-based interface for interacting with your computer. Instead of clicking icons and menus, you type commands and see text output.

**Why developers use command line:**
- Faster than graphical interfaces for many tasks
- Can automate repetitive tasks
- Works the same across different operating systems
- Required for many development tools (Git, Node.js, etc.)
- Professional developers use it regularly

### Windows Terminal

**Windows Terminal** is Microsoft's modern terminal application for Windows. It provides a better experience than the default Command Prompt:
- Multiple tabs for different shells
- Better customization options
- Integration with PowerShell, Git Bash, and other tools
- Modern, professional interface

**Why we use it:**
- Industry standard for Windows development
- Better visual experience
- Supports multiple command-line tools
- Makes working with command line more pleasant

Now that you understand what a terminal is and why it matters, you're ready to install Windows Terminal. Complete [[s0-welcome/exercise-1-installing-windows-terminal|Exercise 1: Installing Windows Terminal]] to set up your command-line environment.

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

## What Makes This Course Different

This course is designed as a **workbook**—meaning you can learn at your own pace without needing an instructor present. Here's what to expect:

- **Self-Paced Learning**: Work through lectures and exercises when it fits your schedule
- **One Continuous Project**: All lessons build on a single repository, not throwaway demos
- **Professional Habits**: Learn industry-standard practices from day one, starting with file organization
- **Portfolio Ready**: Your final project will be something you can show to employers
- **Beginner Friendly**: No prior experience assumed—we explain everything

---

## Welcome to the Course

You're about to learn skills that are in high demand. Full stack engineers work at startups, large tech companies, agencies, and as freelancers. The skills you'll develop here are the foundation of modern web development.

**Remember**: Every expert was once a beginner. Don't be discouraged if things feel challenging at first. That's normal and expected. The key is to keep going, practice regularly, and build on what you learn each day.

This course is designed to take you from zero to building real web applications. We start with understanding file organization—a fundamental skill that makes everything else easier. Then you'll learn version control, web development, and programming. Take your time, follow the lectures, complete the exercises, and work through the labs. Don't skip the explanations—they're there for a reason.

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

---

## Navigation

### Course Sections
- [[s0-welcome/index|Section 0: Orientation]] - Get started here
- [[s1-files/index|Section 1: File Systems and Organization]] - Organization principles
- [[s2-vers-ctrl/index|Section 2: Version Control Foundations]] - Git and GitHub basics
- [[s3-html-css/index|Section 3: HTML & CSS Foundations]] - Web page fundamentals
- [[s4-js/index|Section 4: JavaScript Basics]] - Programming fundamentals
- [[s5-opt-js/index|Section 5: JavaScript Functions]] - Functions and optimization
- [[s6-adv-js/index|Section 6: Advanced JavaScript]] - Advanced concepts
- [[s7-tailwind/index|Section 7: Tailwind CSS]] - Modern styling
- [[s8-tailwind-adv/index|Section 8: Advanced Tailwind]] - Advanced styling

### Getting Started
New to the course? Start with [[s0-welcome/index|Section 0: Orientation]] to set up your development environment, then proceed through each section in order.
