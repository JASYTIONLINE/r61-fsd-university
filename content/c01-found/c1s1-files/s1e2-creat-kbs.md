---
title: "C1S1E2: Creating Your Project Organization Structure"
description: Create the folder structure within your knowledge base that will hold your projects, learning materials, and notes while preventing nested repositories.
tags:
  - file-systems
  - organization
  - folder-structure
  - projects
  - beginner
  - workbook
draft: false
date: 2026-01-30
---

# What Are We Doing?
Exercise 2: Creating Your Project Organization Structure

This exercise is written so you can complete it **without an instructor present**.
Read each section fully before performing the steps.

This exercise is part of the [[c01-found/c1s1-files/index|File Systems and Organization section]]. You'll create the organized folder structure within your knowledge base that will hold all your development work.

---

## What You Are Building

By the end of this exercise, you will have:
- A complete folder structure within your knowledge base
- Subfolders for projects, learning materials, and notes
- An understanding of how to prevent nested repositories
- A README file documenting your structure

---

## Before You Start

Make sure you have:
- Completed [[s1e1-plan-kbs|Exercise 1: Planning Your Knowledge Base Structure]]
- Your knowledge base folder created
- Your structure plan from Exercise 1
- About 10 minutes

**Remember:**
- These are just regular folders—NOT Git repositories yet
- Each project folder will become a separate repository later
- No `.git` folders should exist at this point

---

## Step 1: Create Main Category Folders

### What This Step Does
This creates the main organizational folders that will hold different types of work. This structure prevents confusion and makes it easy to find what you need.
### Instructions
1. Open your **knowledge base folder** (created in Exercise 1)
2. Create the following folders by right-clicking → **New** → **Folder**:

   - **projects** - This will hold your actual coding projects (each will be a separate Git repository)
   - **learning** - Course materials, tutorials, practice exercises
   - **notes** - Personal notes, documentation, ideas
   - **archive** - Completed projects or old work (optional but recommended)

3. Your folder structure should now look like:
   ```
   knowledge-base/
   ├── projects/
   ├── learning/
   ├── notes/
   ├── archive/
   └── structure-plan.md
   ```

### Verify
You should see:
- ✅ Four main folders created (projects, learning, notes, archive)
- ✅ All folders are empty (this is correct)
- ✅ Your structure-plan.md file is still there

---

## Step 2: Create Learning Subfolders

### What This Step Does
The learning folder will hold course materials and practice work. Creating subfolders now helps you organize from the start.

### Instructions
1. Open the **learning** folder
2. Create these subfolders:
   - **courses** - Materials from courses you're taking
   - **practice** - Practice exercises and experiments
   - **tutorials** - Tutorials you're following
   - **resources** - Reference materials, cheat sheets, etc.

1. Your learning folder should now look like:![[ss-learn.png]]
   ```
   learning/
   ├── courses/
   ├── practice/
   ├── tutorials/
   └── resources/
   ```

### Verify
You should see:
- ✅ Four subfolders created in the learning folder
- ✅ All subfolders are empty

---
NEXT STEP
## Step 3: Create a README File

### What This Step Does
A README file documents your folder structure so you (and others) understand the organization. This is a professional practice.

### Instructions
1. Go back to your **knowledge base** root folder **(the main folder)**
2. Right-click → **New** → **Text Document**
3. Name it `README.md` (README files are in Markdown language so they display properly online)
4. Open the file and add this content (customize as needed):

   ```
   # My Development Knowledge Base
   
   This folder contains all my development projects, learning materials, and notes.
   
   ## Folder Structure
   
   - **projects/** - Active coding projects (each is a separate Git repository)
   - **learning/** - Course materials, tutorials, and practice work
     - **courses/** - Materials from courses
     - **practice/** - Practice exercises
     - **tutorials/** - Tutorials I'm following
     - **resources/** - Reference materials
   - **notes/** - Personal notes and documentation
   - **archive/** - Completed or old projects
   
   ## Important Notes
   
   - Each project in the projects/ folder will be its own Git repository
   - No repositories should be nested inside each other

   ```

5. Save the file

### Verify
You should have:
- ✅ A README file in your knowledge base root
- ✅ The README documents your folder structure
- ✅ Clear notes about repository organization

---

## Step 4: Understand Repository Placement

### What This Step Does
This step helps you understand where Git repositories will go inside your structure and why they should not be nested. 

### Instructions
1. Open the **projects** folder
2. Think about future projects:
   - When you create a project (in later exercises), you'll create a folder here
   - Each project folder will become its own Git repository
   - Example structure (for future reference):
     ```
     projects/
     ├── my-first-website/     # This will be a repo (has .git folder)
     ├── portfolio-project/    # This will be a repo (has .git folder)
     └── practice-app/         # This will be a repo (has .git folder)
     ```

1. 

2. Create a README.md file in the projects folder:
   - Right-click in **projects** folder
   - **New** → **Text Document**
   - Name it `README.md` (in a repository, it is customary to have a README file in every section folder to other developers know the purpose of the folder and how it should be used)
   - Add this text:
```
  This is my Projects folder. All repositories created during this course in this folder.  Each folder in Projects will be its own Git repository. Each repository will have its own `.git` folder.
  
  The `projects/` folder itself will NOT have a `.git` folder. This prevents nesting. Nesting in Git means putting one Git repository inside another, which happens when a folder inside your main project also contains its own .git directory. 
  
  When you do this, the outer repo does not properly track the inner repo’s files; it only sees that folder as a separate repository boundary. That creates confusion with commits, pushes, cloning, and history because there is now two independent version histories sitting inside each other. 
  
  Unless you intentionally use submodules (not covered in this course), nesting repos is a mistake: it breaks clean tracking, causes missing files in remote pushes, and makes collaboration messy.
```
     
### Verify
You should understand:
- ✅ Where and why future repositories will be created (in projects/ subfolders)
- ✅ Why the projects/ folder itself won't be a repository 
- ✅ How this prevents nested repositories

---

## Expected State at the End of This Exercise

You should now have:

```
knowledge-base/
├── projects/
│   └── README.md
├── learning/
│   ├── courses/
│   ├── practice/
│   ├── tutorials/
│   └── resources/
├── notes/
├── archive/
├── README.md
└── structure-plan.txt
```

**Important**: No `.git` folders should exist anywhere yet. These are all regular folders.

---

## Why Did You Make ME DO This?

This organized structure:
- **Prevents nested repositories**: By planning where repos go, you avoid accidentally nesting them
- **Makes finding things easy**: Clear categories help you locate projects quickly
- **Scales well**: As you add more projects, the structure stays organized
- **Shows professionalism**: Well-organized folders demonstrate good development habits
- **Self-documenting**: The README explains the structure to you and others

GREAT JOB!!: When you start creating Git repositories in the next section, you'll create them as separate folders inside `projects/`, each with its own `.git` folder. This structure ensures they're never nested.

[[c01-found/c1s1-files/index#Special Cases: Obsidian Knowledge Management|Return to Lecture]]
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
