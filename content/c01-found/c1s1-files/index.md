---
title: "C1S1: File Systems and Organization"
description: A Comprehensive introduction to file organization principles, infrastructure concepts, and why logical file structures matter in professional development.
tags:
  - file-systems
  - organization
  - structure
  - beginner
  - fundamentals
  - infrastructure
draft: false
date: 2026-01-30
---
# Lecture C1S1: File Systems and Organization
In this section you'll learn why good organization matters, see examples of effective structures, understand how the organizational patterns used in this course help you (and others) find what you need quickly, and discover why developers need personal infrastructure that matches organizational standards.
## Getting Started
Many educational platforms strive to teach you "Everything you need to know" about the subject matter it explores, but I have found this endeavor is often fruitless and results in overwhelming the student.

There is a widely accepted way of viewing our level of competence in any given subject. It states there are [four levels of competence](https://en.wikipedia.org/wiki/Four_stages_of_competence).

The goal in this course is to take your from the first level of understanding:
1. Level 1: Unconscious Incompetence (I don't know what I don't know.) 
to
2. level 2: Conscious Incompetence (I know what I don't know.)

I will leave it to you to make the rest of the journey through level 4 by clicking on hyper links you find embedded within the course, and going down your own rabbit holes to find new an interesting ideas and concepts.

Don't try to memorize or learn all the concepts you see here.  Work through the entire course, and we will reinforce the important concepts multiple times. For now, it is enough to grasp the "why" behind our organizational choices, not a deep dive into every possible file structure pattern. By the end, you'll understand why we organize repositories the way we do, and you'll be able to navigate and contribute to well-organized projects.

---
## 1. Planning your Knowledge base
Why File Organization Matters

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
### The New Employee Test

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
- losing work in the mess of files and having to re-create it

---
### Industry Standard Project Structures

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
1. [Separates concerns](https://en.wikipedia.org/wiki/Separation_of_concerns): Code, tests, and documentation are clearly separated
2. [Language-agnostic:](https://en.wikipedia.org/wiki/Language-agnostic) Works for JavaScript, Python, Java, C#, and more
3. [Framework-agnostic:](https://gist.github.com/dragontheory/1277cbace48928eef5f7ab000ef3fe74) Used by React, Vue, Angular, Django, Flask, etc.
4. **Immediately understandable**: Any developer can navigate it without explanation
5. [Scales well:](https://en.wikipedia.org/wiki/Scalability) Works for small projects and large [codebases](https://en.wikipedia.org/wiki/Codebase)
6. **Tool compatibility**: [Build tools](https://dev.to/vaib/top-5-essential-build-tools-for-modern-development-5694), [IDEs](https://en.wikipedia.org/wiki/Integrated_development_environment), and [CI/CD systems](https://en.wikipedia.org/wiki/CI/CD) expect this structure

---
### Variations You'll See

While the core pattern is consistent, you'll see variations:

- [lib/](https://thisvsthat.io/dll-vs-lib) or `app/`** instead of [src/](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/src) (common in some frameworks)
- [`__tests__/` or `test/` or `spec/` instead of `tests/`](https://medium.com/@mohitkhubchandani88/understanding-web-project-folder-structure-6cc7ae62fb40) (depends on testing framework)
- [public/](https://medium.com/@mohitkhubchandani88/understanding-web-project-folder-structure-6cc7ae62fb40) or [static/](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes/static)** instead of `assets/` (common in web projects)
- [dist/ or build/](https://medium.com/@mohitkhubchandani88/understanding-web-project-folder-structure-6cc7ae62fb40) for compiled output (created by build tools, not manually organized)

The key is that the [separation of concerns](https://en.wikipedia.org/wiki/Separation_of_concerns) remains: code, tests, docs, and assets are always separated.

**This is what you'll use in your projects.** When you create repositories in this course, you'll follow this industry-standard structure. It's what employers expect, what tools are designed for, and what makes collaboration possible.

---
### Principles of Good Organization

While different projects use different structures, good organization follows these principles:
1. **Logical Grouping**
Files that belong together should be together. Authentication files go with authentication files, not scattered across the project.
2. **Consistent Naming**
Use consistent [naming conventions](https://en.wikipedia.org/wiki/Naming_convention). If you use [kebab-case](https://developer.mozilla.org/en-US/docs/Glossary/Kebab_case) for folders, use it everywhere. If you number things, be consistent with the numbering system.
 3. **Self-Explanatory Names**
Folder and file names should tell you what's inside. `user-authentication` is better than `auth` or `stuff`.
 4. **Shallow When Possible**
Avoid deeply [nested folders](https://www.glarysoft.com/how-to/are-you-making-these-common-mistakes-with-folder-structure-optimization-in-windows/) when you can. `src/components/auth/login.js` is better than `src/components/user/authentication/forms/login/login.js`.
 5. **Scalable Structure**
Organize for growth. A structure that works for 10 files should still make sense with 1000 files.

These principles apply whether you're organizing a single project or your entire development workspace.

---
### Understanding Git Repositories

When you initialize a [Git ](https://git-scm.com/video/what-is-git) Repository (using [git init](https://git-scm.com/docs/git-init) or through [GitHub](https://en.wikipedia.org/wiki/GitHub) Desktop), Git creates a hidden `.git` folder in that directory. **This `.git` folder is what makes a directory a [Git repository](https://github.com/resources/articles/what-are-code-repositories).
**Important: [Repositories should not be nested](https://www.google.com/search?q=why+not+nest+git+inside+git&sca_esv=4b271a6f1ec3bc04&sxsrf=ANbL-n6vK6tLYJfmBTipapjackZTF5s6Jg%3A1770977859354&source=hp&ei=Q_qOabaZE-LHi-gP87nnGQ&iflsig=AFdpzrgAAAAAaY8IU6eENM44jKc2Ui5FojS7UJwq3B_c&ved=0ahUKEwj2xtbRntaSAxXi4wIHHfPcOQMQ4dUDCDI&uact=5&oq=why+not+nest+git+inside+git&gs_lp=Egdnd3Mtd2l6Iht3aHkgbm90IG5lc3QgZ2l0IGluc2lkZSBnaXQyBRAhGKABMgUQIRigATIFECEYoAFIuS1QwwJYuCtwAngAkAEBmAGeAqAB5haqAQYxOS43LjK4AQPIAQD4AQGYAh2gAoIVqAIKwgIKECMY8AUYJxjqAsICBxAjGCcY6gLCAg0QIxjwBRgnGOoCGJ4GwgINECMY8AUYgAQYJxiKBcICBBAjGCfCAgUQABiABMICCxAuGIAEGNEDGMcBwgIFEC4YgATCAgsQLhiABBjHARivAcICBhAAGBYYHsICCBAAGKIEGIkFwgIFEAAY7wXCAgcQIRigARgKwgIEECEYFcICBhAhGBUYCsICBRAhGJ8FmAMH8QX3pKONZ9TJfZIHBjIxLjcuMaAH3tEBsgcGMTkuNy4xuAf5FMIHBzEzLjE1LjHIByOACAA&sclient=gws-wiz) inside each other.**

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

Now that you understand how repositories work and why they shouldn't be nested, you're ready to plan where yours will live. Complete:
- [Exercise 1: Planning Your Knowledge Base Structure](c01-found/c1s1-files/s1e1-plan-kbs) to get started.

---
## 2. Create Your Personal Knowledge Base Structure

Before you start creating repositories, you need a place to organize all your development work. This is your **knowledge base**—a well-organized folder structure that will hold your projects, learning materials, and notes.
### The Importance of Infrastructure

As a developer, you don't work in isolation. You're part of a team, an organization, and an industry. The tools and systems you use need to work with everyone else's tools and systems.

**This is why a having a [solid file infrastructure](https://mitcommlab.mit.edu/broad/commkit/file-structure/) matters.** When everyone uses similar tools and follows similar standards, collaboration becomes easier. Code flows smoothly between team members. Problems get solved faster. New team members can get up to speed quickly.
### The Organization Connection

Most developers work within organizations—companies, agencies, or teams. These organizations have policies and standards:
- **Communication tools** - Your company might use [Microsoft Teams](https://support.microsoft.com/en-us/topic/what-is-microsoft-teams-3de4d369-0167-8def-b93b-0eb5286d7a29), [Slack](https://slack.com/resources/why-use-slack/what-is-slack-and-how-does-it-work), or [Discord](https://support.discord.com/hc/en-us/articles/360045138571-Beginner-s-Guide-to-Discord)
- **Project management** - They might use [Jira](https://www.atlassian.com/software/jira), [Trello](https://trello.com/), or [Asana](https://asana.com/)
	- [Code hosting](https://en.wikipedia.org/wiki/Comparison_of_source-code-hosting_facilities) - They might use [GitHub](https://github.com/), [GitLab](https://gitlab.com/), or [Bitbucket](https://www.atlassian.com/software/bitbucket)
- [Code editors](https://www.geeksforgeeks.org/blogs/ide-vs-code-editor/) - They might standardize on [VS Code](https://code.visualstudio.com/), [IntelliJ](https://www.jetbrains.com/idea/), or [Vim](https://www.vim.org/)

If your organization uses Teams for communication, you need to be proficient in Teams. If they use GitHub for code, you need to understand GitHub. If they standardize on VS Code, you should use VS Code.

**Your personal infrastructure should mirror your organization's infrastructure.** This doesn't mean you can't have personal preferences, but it does mean you need to be comfortable with the tools your team uses.

---
### Organizational Structures in This Course

Throughout this course, you'll encounter several organizational patterns. Understanding these patterns helps you navigate the material and prepares you for real-world projects.  We will ask you to think of your own way of organizing things, but at the same time for continuity purposes, we will have you follow our set structure during the course.  Our file system is A WAY not THE Way, but it is the way we will do things during this course.
#### 1. Section-Based Organization

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
#### 2. Section Content Organization

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
#### Why this structure works:
1. It **Prevents nested repositories**: The **`projects/`** folder itself is NOT a repository. Each project inside it is its own separate repository.
2. **Clear separation**: Projects, learning materials, and notes are organized by purpose
3. **Scalable**: As you add more projects, the structure stays organized
4. **Self-documenting**: Anyone (including future you) can understand the organization

---
### Building Your Knowledge Base

By completing this section and its exercises, you will have:

- ✅ A well-organized knowledge base folder structure
- ✅ Clear separation between projects, learning materials, and notes
- ✅ Understanding of where future Git repositories will live
- ✅ A system that prevents nested repositories
- ✅ Documentation of your organizational structure
- ✅ (Optional) An Obsidian vault set up with proper structure for publishing

This foundation will support all your development work throughout this course and your career. Every project you create will have a clear place to live, and you'll never struggle with "where should I put this?" or accidentally create nested repositories.

**The knowledge base you build now will become the foundation for everything you create as a developer.**
#### Important points:
- The **knowledge-base** folder itself is **NOT** a Git repository
- Each project in `projects/` will be its own separate repository
- This structure prevents the nested repository problem we discussed earlier
- You'll create this structure in the exercises

With these organizational principles in mind, you're ready to create your own organized structure. Complete:
- [Exercise 2: Creating Your Project Organization Structure](c01-found/c1s1-files/s1e2-creat-kbs) to build your knowledge base.

---
## 3. Special Cases: Obsidian Knowledge Base Management

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

To learn more about Why you should consider using Obsidian check out [this ~30min video ](https://www.bing.com/videos/riverview/relatedvideo?q=why+use+obsidian+effectively&&mid=A9D3E4E06F582D97E5D1A9D3E4E06F582D97E5D1&churl=https%3a%2f%2fwww.youtube.com%2fchannel%2fUCQjBsscIa_mgEnSvWpm_9vw&FORM=VCGVRP) that explains everything you need to know to get started. 

or 

If you want to set up a Knowledge Base in Obsidian with the proper structure, complete:
- [Exercise 3: Setting Up Obsidian Knowledge Base](c01-found/c1s1-files/s1e3-obsid-kbs) (optional).
---
### 4. Apply this lesson to Your Learning Experience
As you work through this course:

1. **Notice the patterns** - Pay attention to how files are organized in each section
2. **Follow the structure** - When creating files, put them where the structure suggests they belong
3. **Ask why** - When you see a particular organization, think about why it was chosen
4. **Apply the principles** - Use these organizational principles in your own projects

OUTSTANDING WORK!!!   
The repository you'll build throughout this course will follow professional organizational standards. By the end of this course, you'll have a portfolio piece that demonstrates not just coding skills, but also professional organizational habits.

---
#### Next Steps: [C1S2: Version Control Foundations](c01-found/c1s2-vers-ctrl/index)
The Foundations of Git and Version Control

---
## Navigation
[Back to the Top](#Getting%20Started)
### Exercises in This Section
Complete these exercises to set up your knowledge base and understand file organization:

1. [Exercise 1: Planning Your Knowledge Base Structure](c01-found/c1s1-files/s1e1-plan-kbs)
   - Choose a location for your knowledge base
   - Understand the difference between a knowledge base folder and a Git repository
   - Create your top-level knowledge base folder
   - Plan your folder structure

1. [Exercise 2: Creating Your Project Organization Structure](c01-found/c1s1-files/s1e2-creat-kbs)
   - Create organized folders for projects, learning materials, and notes
   - Set up a structure that prevents nested repositories
   - Document your organization with README files
   - Understand where future Git repositories will be placed

1. [Exercise 3: Setting Up Obsidian Knowledge Base](c01-found/c1s1-files/s1e3-obsid-kbs) (Optional)
   - Set up Obsidian with the special `content/` folder structure for publishing
   - Understand how Obsidian's organization differs from standard repositories
   - Create your first notes in the proper structure
   - Document the Obsidian vault structure

---
### Global Navigation

- [HOME:](index) JASYTI's Full Stack Development Foundations Course -
- [Course 01:](c01-found/index) Foundations of Front End Development
- [Course 02:](c02-genai-fun/index.md) Fundamentals of Generative AI
- [Course 03:](c03-fe-react/index.md) Designing a Dynamic Frontend with React
- [Course 04:](c04-genai-design/index.md) Harnessing Gen AI: From Design to Code Optimization
- [Course 05:](c05-data/index) Understanding Data Structures and Algorithms
- [Course 06:](c06-mongol/index) Using MongoDB to Design and Manage Databases
- [Course 07:](c07-express/index) Developing a Reliable Back-end with Node and Express
- [Course:08](c08-ai-test/index) The Power of Generative AI Software Testing
- [Course 09:](c09-publish/index) Publishing your Website to the Live Internet
