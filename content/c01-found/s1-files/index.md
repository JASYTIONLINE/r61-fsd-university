---
title: "File Systems and Organization"
description: "Comprehensive introduction to file organization principles, infrastructure concepts, and why logical file structures matter in professional development."
tags: [file-systems, organization, structure, beginner, fundamentals, infrastructure]
draft: false
date: "2026-01-30"
---

# File Systems and Organization

This section introduces you to the fundamental principles of organizing files and folders. You'll learn why good organization matters, see examples of effective structures, understand how the organizational patterns used in this course help you (and others) find what you need quickly, and discover why developers need personal infrastructure that matches organizational standards.

This is a **level 2 understanding**—enough to grasp the "why" behind our organizational choices, not a deep dive into every possible file structure pattern. By the end, you'll understand why we organize repositories the way we do, and you'll be able to navigate and contribute to well-organized projects.

---

## Why File Organization Matters

Imagine you're a new employee at a software company. On your first day, your manager says: "Welcome! Your first task is to update the user authentication system. All the files you need are somewhere in our codebase. Good luck!"

You open the project folder and see this:

```
project/
├── stuff/
├── files/
├── old/
├── new/
├── temp/
├── backup/
├── final/
├── final-final/
└── really-final-this-time/
```

How would you know where to start? What's in "stuff"? Is "old" actually old, or just poorly named? Is "really-final-this-time" actually the current version?

Now imagine you open the project and see this:

```
project/
├── src/
│   ├── components/
│   │   ├── auth/
│   │   │   ├── login.js
│   │   │   ├── register.js
│   │   │   └── password-reset.js
│   │   └── dashboard/
│   ├── services/
│   │   └── auth-service.js
│   └── utils/
├── tests/
│   └── auth/
├── docs/
│   └── authentication.md
└── README.md
```

Even without instructions, you can immediately see:
- Authentication-related files are in `src/components/auth/`
- There's a service file for authentication logic
- Tests are organized in a `tests/` folder
- Documentation exists in `docs/`

**Good file organization is self-documenting.** A well-organized project tells a story. Anyone—including future you—should be able to look at the folder structure and understand:
- What the project does
- Where different types of files belong
- How to find what they need
- Where to add new files

---

## The New Employee Test

A simple test for good organization: **Can a new team member find what they need without asking?**

If someone can look at your file tree and answer these questions without help, you have good organization:

1. **Where do I add a new feature?**
2. **Where are the tests?**
3. **Where is the documentation?**
4. **Where are configuration files?**
5. **What's the entry point of this application?**

When files are organized logically, the structure itself becomes a form of communication. It reduces the need for:
- Long onboarding sessions
- Extensive documentation about "where things go"
- Questions like "where should I put this?"
- Mistakes from putting files in the wrong place

---

## Industry Standard Project Structures

The software development industry has converged on certain organizational patterns. These aren't arbitrary—they exist because they work well for collaboration and productivity across different programming languages, frameworks, and team sizes.

### The Standard Structure

Most professional projects follow this pattern:

```
my-project/
├── src/           # Source code (the actual application code)
├── tests/         # Test files (or __tests__, test/, spec/)
├── docs/          # Documentation
├── assets/        # Images, fonts, static files
├── config/        # Configuration files
└── README.md      # Project overview and setup instructions
```

**Why this structure is industry standard:**

1. **Separates concerns**: Code, tests, and documentation are clearly separated
2. **Language-agnostic**: Works for JavaScript, Python, Java, C#, and more
3. **Framework-agnostic**: Used by React, Vue, Angular, Django, Flask, etc.
4. **Immediately understandable**: Any developer can navigate it without explanation
5. **Scales well**: Works for small projects and large codebases
6. **Tool compatibility**: Build tools, IDEs, and CI/CD systems expect this structure

### Variations You'll See

While the core pattern is consistent, you'll see variations:

- **`lib/` or `app/`** instead of `src/` (common in some frameworks)
- **`__tests__/` or `test/` or `spec/`** instead of `tests/` (depends on testing framework)
- **`public/` or `static/`** instead of `assets/` (common in web projects)
- **`dist/` or `build/`** for compiled output (created by build tools, not manually organized)

The key is that the **separation of concerns** remains: code, tests, docs, and assets are always separated.

**This is what you'll use in your projects.** When you create repositories in this course, you'll follow this industry-standard structure. It's what employers expect, what tools are designed for, and what makes collaboration possible.

---

## Principles of Good Organization

While different projects use different structures, good organization follows these principles:

### 1. **Logical Grouping**
Files that belong together should be together. Authentication files go with authentication files, not scattered across the project.

### 2. **Consistent Naming**
Use consistent naming conventions. If you use `kebab-case` for folders, use it everywhere. If you number things, be consistent with the numbering system.

### 3. **Self-Explanatory Names**
Folder and file names should tell you what's inside. `user-authentication` is better than `auth` or `stuff`.

### 4. **Shallow When Possible**
Avoid deeply nested folders when you can. `src/components/auth/login.js` is better than `src/components/user/authentication/forms/login/login.js`.

### 5. **Scalable Structure**
Organize for growth. A structure that works for 10 files should still make sense with 1000 files.

These principles apply whether you're organizing a single project or your entire development workspace.

---

## Understanding Git Repositories

When you initialize a Git repository (using `git init` or through GitHub Desktop), Git creates a hidden `.git` folder in that directory. **This `.git` folder is what makes a directory a Git repository.**

**Important: Repositories should not be nested inside each other.**

Here's what NOT to do:

```
my-projects/
├── .git/                    # This is a repository
├── project-a/
│   ├── .git/                # ❌ Another repository nested inside!
│   └── src/
└── project-b/
    ├── .git/                # ❌ Another repository nested inside!
    └── src/
```

**Why this is a problem:**
- Git gets confused about which repository you're working in
- Commands may affect the wrong repository
- Version control becomes unreliable
- It's difficult to manage multiple projects

**The correct approach:**

```
my-projects/                 # Just a regular folder (no .git here)
├── project-a/               # Separate repository
│   ├── .git/
│   └── src/
└── project-b/               # Separate repository
    ├── .git/
    └── src/
```

Or even better, keep repositories completely separate:

```
Documents/
├── project-a/               # Repository 1
│   ├── .git/
│   └── src/
└── project-b/               # Repository 2
    ├── .git/
    └── src/
```

**Key takeaway:** If you're setting up multiple repositories, make sure each one is in its own separate folder at the same level, not nested inside another repository. Each project should have its own `.git` folder at the root of that project, and no other `.git` folders should exist inside it.

Now that you understand how repositories work and why they shouldn't be nested, you're ready to plan where yours will live. Complete [[s1-files/s1e1-planning-knowledge-base-structure|Exercise 1: Planning Your Knowledge Base Structure]] to get started.

---

## Your Personal Knowledge Base Structure

Before you start creating repositories, you need a place to organize all your development work. This is your **knowledge base**—a well-organized folder structure that will hold your projects, learning materials, and notes.

### The Knowledge Base Structure

Your knowledge base will follow this pattern:

```
knowledge-base/
├── projects/          # Your actual coding projects (each will be a separate Git repository)
│   ├── my-first-app/  # Repository 1 (has its own .git folder)
│   ├── portfolio/     # Repository 2 (has its own .git folder)
│   └── practice/      # Repository 3 (has its own .git folder)
├── learning/          # Course materials, tutorials, practice code
│   ├── courses/       # Materials from courses
│   ├── practice/      # Practice exercises
│   ├── tutorials/     # Tutorials you're following
│   └── resources/     # Reference materials
├── notes/             # Personal notes, documentation, ideas
└── archive/           # Completed projects or old work
```

**Why this structure works:**

1. **Prevents nested repositories**: The **`projects/`** folder itself is NOT a repository. Each project inside it is its own separate repository.
2. **Clear separation**: Projects, learning materials, and notes are organized by purpose
3. **Scalable**: As you add more projects, the structure stays organized
4. **Self-documenting**: Anyone (including future you) can understand the organization

**Important points:**
- The **knowledge-base** folder itself is **NOT** a Git repository
- Each project in `projects/` will be its own separate repository
- This structure prevents the nested repository problem we discussed earlier
- You'll create this structure in the exercises

With these organizational principles in mind, you're ready to create your own organized structure. Complete [[s1-files/s1e2-creating-project-organization-structure|Exercise 2: Creating Your Project Organization Structure]] to build your knowledge base.

---

## Special Cases: Obsidian Knowledge Management

Some tools have special organizational requirements. [Obsidian](https://obsidian.md/)  is a note-taking and knowledge management tool that uses Markdown files, and it's great for documenting what you're learning and organizing your knowledge.

**Note about Obsidian folder structure:** If you plan to use Obsidian for publishing (like this course does), be aware that Obsidian typically publishes from a `content` folder rather than the root directory. This means your folder structure needs to be planned differently—your actual content goes inside a `content/` subfolder, and the Obsidian configuration stays at the root.

**Standard repository structure:**
```
my-repo/
├── .git/
├── src/
└── README.md
```

**Obsidian publishing structure:**
```
obsidian-vault/
├── .obsidian/          # Obsidian config (not published)
├── content/            # This is what gets published!
│   ├── index.md
│   └── notes/
└── README.md
```

This is a special case that requires a slightly different organizational approach than standard repositories. If you're just using Obsidian for personal notes, you don't need to worry about this, but if you plan to publish your vault, you'll need to structure it accordingly.

To learn more about Why you should consider using Obsidian check out [this ~30min](https://www.bing.com/videos/riverview/relatedvideo?q=why+use+obsidian+effectively&&mid=A9D3E4E06F582D97E5D1A9D3E4E06F582D97E5D1&churl=https%3a%2f%2fwww.youtube.com%2fchannel%2fUCQjBsscIa_mgEnSvWpm_9vw&FORM=VCGVRP) video that explains everything you need to know to get started. 

or 

If you want to set up a KB in Obsidian with the proper structure, complete [[s1-files/s1e3-setting-up-obsidian-knowledge-base|Exercise 3: Setting Up Obsidian Knowledge Base]] (optional).

---

## Why Infrastructure Matters

As a developer, you don't work in isolation. You're part of a team, an organization, and an industry. The tools and systems you use need to work with everyone else's tools and systems.

**This is why infrastructure matters.** When everyone uses similar tools and follows similar standards, collaboration becomes easier. Code flows smoothly between team members. Problems get solved faster. New team members can get up to speed quickly.

### The Organization Connection

Most developers work within organizations—companies, agencies, or teams. These organizations have policies and standards:

- **Communication tools** - Your company might use Microsoft Teams, Slack, or Discord
- **Project management** - They might use [Jira](https://www.atlassian.com/software/jira), [Trello](https://trello.com/), or [Asana](https://asana.com/)
	- **Code hosting** - They might use [GitHub](https://github.com/), [GitLab](https://gitlab.com/), or [Bitbucket](https://www.atlassian.com/software/bitbucket)
- **Code editors** - They might standardize on [VS Code](https://code.visualstudio.com/), [IntelliJ](https://www.jetbrains.com/idea/), or [Vim](https://www.vim.org/)

If your organization uses [Teams](https://support.microsoft.com/en-us/topic/what-is-microsoft-teams-3de4d369-0167-8def-b93b-0eb5286d7a29) for communication, you need to be proficient in Teams. If they use GitHub for code, you need to understand GitHub. If they standardize on VS Code, you should use VS Code.

**Your personal infrastructure should mirror your organization's infrastructure.** This doesn't mean you can't have personal preferences, but it does mean you need to be comfortable with the tools your team uses.

---

## Organizational Structures in This Course

Throughout this course, you'll encounter several organizational patterns. Understanding these patterns helps you navigate the material and prepares you for real-world projects.

### 1. Section-Based Organization

Our course content is organized by sections. Each section is designed to be reviewed in sequence, but also works as a stand alone work package:

```
content/
├── orientation/
├── file-systems/
├── version-control/
├── html-css/
└── ...
```

**Why this works:**
- Clear progression from one topic to the next
- Easy to find material for a specific section
- Each section folder contains everything related to that topic
- Descriptive names show the learning sequence

**When you'd use this:**
- Educational materials
- Documentation organized by topic
- Training programs
- Sequential learning resources

### 2. Section Content Organization

Within each section, content is organized by type:

```
file-systems/
├── index.md              # Comprehensive lecture
├── s1e1-name.md          # Focused exercise 1
├── s1e2-name.md          # Focused exercise 2
└── s1e3-name.md          # Focused exercise 3
```

**Why this works:**
- Clear separation between learning materials (lecture) and practice (exercises)
- Easy to find what you need: want to learn? Read the lecture. Want to practice? Do an exercise. (this is where an Obsidian knowledge base shines by allowing you to store your material using separation of concerns while accessing it in sequence)
- Consistent structure across all sections
- Each exercise focuses on one concept from the lecture

**When you'd use this:**
- Educational courses with multiple content types
- Training programs with lectures and hands-on work
- Structured learning materials (like this site)
- Courses that combine theory and practice

---

## Building Your Knowledge Base

By completing this section and its exercises, you will have:

- ✅ A well-organized knowledge base folder structure
- ✅ Clear separation between projects, learning materials, and notes
- ✅ Understanding of where future Git repositories will live
- ✅ A system that prevents nested repositories
- ✅ Documentation of your organizational structure
- ✅ (Optional) An Obsidian vault set up with proper structure for publishing

This foundation will support all your development work throughout this course and your career. Every project you create will have a clear place to live, and you'll never struggle with "where should I put this?" or accidentally create nested repositories.

**The knowledge base you build now will become the foundation for everything you create as a developer.**

---

## Exercises in This Section

Complete these exercises to set up your knowledge base and understand file organization:

1. **[[s1-files/s1e1-planning-knowledge-base-structure|Exercise 1: Planning Your Knowledge Base Structure]]**
   - Choose a location for your knowledge base
   - Understand the difference between a knowledge base folder and a Git repository
   - Create your top-level knowledge base folder
   - Plan your folder structure

2. **[[s1-files/s1e2-creating-project-organization-structure|Exercise 2: Creating Your Project Organization Structure]]**
   - Create organized folders for projects, learning materials, and notes
   - Set up a structure that prevents nested repositories
   - Document your organization with README files
   - Understand where future Git repositories will be placed

3. **[[s1-files/s1e3-setting-up-obsidian-knowledge-base|Exercise 3: Setting Up Obsidian Knowledge Base]]** (Optional)
   - Set up Obsidian with the special `content/` folder structure for publishing
   - Understand how Obsidian's organization differs from standard repositories
   - Create your first notes in the proper structure
   - Document the Obsidian vault structure

---

## How This Applies to Your Learning

As you work through this course:

1. **Notice the patterns** - Pay attention to how files are organized in each section
2. **Follow the structure** - When creating files, put them where the structure suggests they belong
3. **Ask why** - When you see a particular organization, think about why it was chosen
4. **Apply the principles** - Use these organizational principles in your own projects

OOUTSTANDING WORK!!!   
The repository you'll build throughout this course will follow professional organizational standards. By the end of this course, you'll have a portfolio piece that demonstrates not just coding skills, but also professional organizational habits.

Next Steps: [[s2-vers-ctrl/index|Version Control]] - Git and GitHub basics

---

## Navigation

### Section Navigation
- [[index|Home]] - Return to the main course page
- [[s0-welcome/index|Orientation]] - Previous section
- [[s1-files/index|File Systems]] - This page
- [[s2-vers-ctrl/index|Version Control]] - Next section

### Course Sections
- [[s0-welcome/index|Orientation]] - Get started here
- [[s1-files/index|File Systems]] - Organization principles
- [[s2-vers-ctrl/index|Version Control]] - Git and GitHub basics
- [[s3-html-css/index|HTML & CSS]] - Web page fundamentals
- [[s4-js/index|JavaScript Basics]] - Programming fundamentals
- [[s5-opt-js/index|JavaScript Functions]] - Functions and optimization
- [[s6-adv-js/index|Advanced JavaScript]] - Advanced concepts
- [[s7-tailwind/index|Tailwind CSS]] - Modern styling
- [[s8-tailwind-adv/index|Advanced Tailwind]] - Advanced styling
