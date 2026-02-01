---
title: "Exercise 2: Creating Your Project Organization Structure"
description: "Create the folder structure within your knowledge base that will hold your projects, learning materials, and notes while preventing nested repositories."
tags: [file-systems, organization, folder-structure, projects, beginner, workbook]
draft: false
date: "2026-01-30"
---

# Exercise 2: Creating Your Project Organization Structure

This exercise is written so you can complete it **without an instructor present**.
Read each section fully before performing the steps.

This exercise is part of the [[s1-files/index|File Systems and Organization section]]. You'll create the organized folder structure within your knowledge base that will hold all your development work.

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
- Completed [[s1-files/s1e1-planning-knowledge-base-structure|Exercise 1: Planning Your Knowledge Base Structure]]
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
   └── structure-plan.txt
   ```

### Verify
You should see:
- ✅ Four main folders created (projects, learning, notes, archive)
- ✅ All folders are empty (this is correct)
- ✅ Your structure-plan.txt file is still there

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

3. Your learning folder should now look like:
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

## Step 3: Create a README File

### What This Step Does
A README file documents your folder structure so you (and others) understand the organization. This is a professional practice.

### Instructions
1. Go back to your **knowledge base** root folder (the main folder)
2. Right-click → **New** → **Text Document**
3. Name it `README.txt` (or `README.md` if you prefer Markdown)
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
   - This knowledge base folder itself is NOT a Git repository
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
This step helps you understand where Git repositories will go and why they won't be nested.

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

3. **Key point**: Each project folder will have its own `.git` folder, but the `projects/` folder itself will NOT have a `.git` folder. This prevents nesting.

4. Create a placeholder file in the projects folder to remind yourself:
   - Right-click in **projects** folder
   - **New** → **Text Document**
   - Name it `README.txt`
   - Add this text: "Each project folder here will be its own Git repository. This folder itself is NOT a repository."

### Verify
You should understand:
- ✅ Where future repositories will be created (in projects/ subfolders)
- ✅ Why the projects/ folder itself won't be a repository
- ✅ How this prevents nested repositories

---

## Expected State at the End of This Exercise

You should now have:

```
knowledge-base/
├── projects/
│   └── README.txt
├── learning/
│   ├── courses/
│   ├── practice/
│   ├── tutorials/
│   └── resources/
├── notes/
├── archive/
├── README.txt (or README.md)
└── structure-plan.txt
```

**Important**: No `.git` folders should exist anywhere yet. These are all regular folders.

---

## Why This Matters

This organized structure:
- **Prevents nested repositories**: By planning where repos go, you avoid accidentally nesting them
- **Makes finding things easy**: Clear categories help you locate projects quickly
- **Scales well**: As you add more projects, the structure stays organized
- **Shows professionalism**: Well-organized folders demonstrate good development habits
- **Self-documenting**: The README explains the structure to you and others

When you start creating Git repositories in the next section, you'll create them as separate folders inside `projects/`, each with its own `.git` folder. This structure ensures they're never nested.

---

## Navigation

### Section Navigation
- [[index 1|Home]] - Return to main course page
- [[s1-files/index|File Systems Index]] - Return to file systems overview
- [[s1-files/s1e1-planning-knowledge-base-structure|Exercise 1: Planning Knowledge Base Structure]] - Previous exercise
- [[s1-files/s1e2-creating-project-organization-structure|Exercise 2: Creating Project Organization Structure]] - This page
- [[s1-files/s1e3-setting-up-obsidian-knowledge-base|Exercise 3: Setting Up Obsidian Knowledge Base]] - Next exercise (Optional)

### Related Materials
- [[s1-files/index|File Systems Lecture]] - Review the concepts
