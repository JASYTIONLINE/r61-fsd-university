---
title: "C1S1E1: Planning Your Knowledge Base Structure"
description: Plan and create the foundational folder structure for your development knowledge base that will hold all your projects, repositories, and learning materials.
tags:
  - file-systems
  - organization
  - knowledge-base
  - structure
  - beginner
  - workbook
draft: false
date: 2026-01-30
---
# What Are We Doing?
Exercise 1: Planning Your Knowledge Base Structure

This exercise is written so you can complete it **without an instructor present**.
Read each section fully before performing the steps.

This exercise is part of the [[c01-found/c1s1-files/index|File Systems and Organization section]]. You'll create a well-organized knowledge base that will hold all your development projects, repositories, and learning materials.

---

## What You Are Building

By the end of this exercise, you will have:
- A clear plan for where your knowledge base will live
- An understanding of the difference between a knowledge base folder and a Git repository
- A top-level knowledge base folder created
- A documented structure plan for your projects

---

## Before You Start

Make sure you have:
- A Windows computer
- Basic understanding of File Explorer
- About 10-15 minutes
- A location in mind for your knowledge base (Documents folder, Desktop, or a dedicated drive)

**Important concepts to remember:**
- A knowledge base is just a regular folder—it's NOT a Git repository
- This folder will contain multiple separate Git repositories later
- Each repository will have its own `.git` folder, but they won't be nested inside each other

---

## Step 1: Choose Your Knowledge Base Location

### What This Step Does
You need to decide where your knowledge base will live on your computer. This is where all your development projects, learning materials, and repositories will be organized.

### Instructions
1. Think about where you want your development work to live:
   - **Documents folder**: `C:\Users\YourName\Documents\knowledge-base` (common choice)
   - **Desktop**: `C:\Users\YourName\Desktop\knowledge-base` (easy to find)
   - **Dedicated location**: `C:\dev\knowledge-base` or `D:\development\knowledge-base` (if you have a separate drive)
   - **OneDrive/Cloud**: If you use OneDrive, you can put it there, but be aware that syncing many files can be slow (i don't recommend this as one drive sync can interfere with .git.)

2. **Recommended location**: `Documents\knowledge-base` or `Documents\dev-knowledge-base`
   - Easy to find
   - Professional organization

3. Write down or remember your chosen location—you'll need it in the next step.

### Verify
You should have:
- ✅ A location chosen for your knowledge base
- ✅ An understanding of why you chose that location
- ✅ The full path written down (e.g., `C:\Users\YourName\Documents\knowledge-base`)

---

## Step 2: Create Your Knowledge Base Folder

### What This Step Does
This creates the top-level folder that will contain all your development work. This is just a regular folder—not a Git repository.

### Instructions
1. Open **File Explorer** (Windows key + E)
2. Navigate to your chosen location (e.g., Documents folder)
3. Right-click in an empty area
4. Select **New** → **Folder**
5. Name the folder: `knowledge-base` or `dev-knowledge-base` or `my-development`
   - Use a name that makes sense to you
   - Avoid spaces if possible (use hyphens or underscores instead)
   - Example: `knowledge-base`, `dev-knowledge-base`, `my-dev-work`
6. Press Enter to create the folder

### Verify
You should see:
- ✅ A new folder created in your chosen location
- ✅ The folder is empty (this is correct—we'll add structure in the next exercise)
- ✅ You can open the folder and see it's empty

---

## Step 3: Plan Your Folder Structure

### What This Step Does
Before creating subfolders, you'll plan out how you want to organize your projects. This prevents confusion and nested repositories later.

### Instructions
1. Open your knowledge base folder (the one you just created)
2. Think about how you want to organize your work. I recommend using the following structure during this course. It will help keep you grounded and be easy to follow through the course:
---
#### Figure 1
```
knowledge-base/
├── projects/          # Your actual coding projects (each will be a separate repo)
├── learning/          # Course materials, tutorials, practice code
├── notes/             # Personal notes, documentation, ideas
└── archive/           # Old projects or completed work
```
---
3. **Important considerations:**
   - **projects/**: This is where you'll create Git repositories. Each project will be its own folder with its own `.git` folder
   - **learning/**: Course materials, tutorials, practice exercises (may or may not be repos)
   - **notes/**: Personal documentation, ideas, planning documents
   - **archive/**: Completed projects or old work

4. **Key principle**: No repository should be nested inside another repository. Each project in `projects/` will be a separate, independent repository.

5. Create a markdown file in your knowledge base folder called `structure-plan.md:
   - Right-click in the folder
   - Select **New** → **Text Document**
   - Name it `structure-plan.md'
   - Open it and write down your planned structure or copy and past the file structure in [[#Figure 1|Figure 1]]
---
### Verify
You should have:
- ✅ A plan for your folder structure
- ✅ A `structure-plan.md` file with your structure documented
- ✅ An understanding that each project will be a separate repository (not nested)

---

## Expected State at the End of This Exercise

You should now have:
- **Knowledge base folder**: Created in your chosen location
- **Structure plan**: Documented in `structure-plan.md
- **Understanding**: Clear idea of where your development work will live

Your knowledge base folder should look like:
![[ss-kb-start.png]]
```
knowledge-base/
└── structure-plan.md
```

---

## Why This Matters

A well-planned knowledge base:
- **Prevents confusion**: You always know where to find your projects
- **Avoids nested repositories**: By planning ahead, you won't accidentally create repos inside repos
- **Scales well**: As you add more projects, the structure stays organized
- **Professional**: Shows good organizational habits from the start

Congratulations": You have Just taken the firs steps to managing all your future files in a professional knowledge base with version control. This foundation will support all your development work throughout this course and your career.

Next Steps: [[c01-found/c1s1-files/index#Your Personal Knowledge Base Structure|Return to Lecture]]
---
[Back to the Top](#What%20are%20we%20doing?)
## Navigation
### Section 0 Map
- [C1S1E1:](c01-found/c1s1-files/s1e2-creat-kbs) Planning Your Knowledge Base Structure
- [C1S1E2:](c01-found/c1s1-files/s1e2-creat-kbs) Creating Your Project Organization Structure
- [C1S1E3:](c01-found/c1s1-files/s1e3-obsid-kbs) Setting Up Obsidian Knowledge Base (Optional)

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
