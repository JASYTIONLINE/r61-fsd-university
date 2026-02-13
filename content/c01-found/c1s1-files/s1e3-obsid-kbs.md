---
title: "C1S1E3: Setting Up Obsidian Knowledge Base (Optional)"
description: Set up Obsidian as a knowledge management tool with the special folder structure required for publishing, understanding how it differs from standard repository organization.
tags:
  - obsidian
  - knowledge-base
  - note-taking
  - organization
  - optional
  - beginner
  - workbook
draft: false
date: 2026-01-30
---

# What Are We Doing?
Exercise 3: Setting Up Obsidian Knowledge Base (Optional)

This exercise is written so you can complete it **without an instructor present**.
Read each section fully before performing the steps.

This exercise is part of the [[c01-found/c1s1-files/index|File Systems and Organization section]]. You'll set up Obsidian as a note-taking and knowledge management tool, with special attention to its unique folder structure requirements for publishing.

**Note:** This exercise is **optional**. Only complete it if you want to use Obsidian for note-taking and knowledge management. If you're just using Obsidian for personal notes (not publishing), you can skip the special folder structure setup.

---

## What You Are Building

By the end of this exercise, you will have:
- Obsidian installed (if not already installed)
- An Obsidian vault created with the correct structure for publishing
- Understanding of how Obsidian's folder structure differs from standard repositories
- Basic Obsidian configuration

---

## Before You Start

Make sure you have:
- Completed [[s1e1-plan-kbs|Exercise 1: Planning Your Knowledge Base Structure]]
- Obsidian installed (from [[s0e6-opts|Orientation Exercise 6]] or install it now)
- About 15-20 minutes
- Understanding that Obsidian uses a special structure for publishing

**Important:** If you're using Obsidian just for personal notes (not publishing), you can create a simpler structure. This exercise focuses on the publishing structure because this course uses it.

---

## Step 1: Understand Obsidian's Special Structure

### What This Step Does
Obsidian has a unique requirement: when publishing, the published content lives in a `content/` folder, not at the root. This is different from standard Git repositories.

### Instructions
1. **Standard Git repository structure:**
   ```
   my-repo/
   ├── .git/
   ├── src/
   ├── README.md
   └── index.html
   ```
   Everything is at the root level.

2. **Obsidian publishing structure:**
   ```
   obsidian-vault/
   ├── .obsidian/          # Obsidian config (not published)
   ├── content/             # This is what gets published!
   │   ├── index.md
   │   ├── section-1/
   │   └── section-2/
   └── README.md            # At root, but content/ is what matters
   ```

3. **Key difference:** 
   - In a standard repo, your main content is at the root
   - In Obsidian for publishing, your main content goes in `content/`
   - The Obsidian configuration stays at the root level

4. This is why you need to plan your Obsidian vault structure differently if you plan to publish.

### Verify
You should understand:
- ✅ Obsidian uses a `content/` folder for published material
- ✅ This is different from standard repository structure
- ✅ Configuration files stay at the root, content goes in `content/`

---

## Step 2: Decide Where Your Obsidian Vault Will Live

### What This Step Does
You need to decide if your Obsidian vault will be part of your knowledge base or separate. Both approaches work.

### Instructions
1. **Option A: Obsidian vault inside knowledge base**
   ```
   knowledge-base/
   ├── projects/
   ├── learning/
   ├── notes/
   └── obsidian-vault/      # Obsidian vault here
       ├── .obsidian/
       └── content/
   ```
   - Pros: Everything in one place
   - Cons: Obsidian vault structure is different from other folders

2. **Option B: Obsidian vault separate from knowledge base**
   ```
   Documents/
   ├── knowledge-base/      # Your dev work
   └── obsidian-vault/      # Obsidian separate
       ├── .obsidian/
       └── content/
   ```
   - Pros: Clear separation, easier to manage
   - Cons: Two locations to remember

3. **Recommendation:** If you're publishing (like this course), keep it separate. If just for personal notes, either works.

4. Choose your approach and remember where you'll create it.

### Verify
You should have:
- ✅ Decided where your Obsidian vault will live
- ✅ Understanding of the two approaches
- ✅ A location chosen

---

## Step 3: Create Your Obsidian Vault Structure

### What This Step Does
This creates the Obsidian vault with the correct folder structure for publishing.

### Instructions
1. Navigate to your chosen location (separate from knowledge base, or inside it if you prefer)

2. Create a new folder named `obsidian-vault` or `my-notes` or similar

3. Inside that folder, create a `content` folder:
   - This is where all your published notes will go
   - Right-click in the vault folder → **New** → **Folder**
   - Name it `content`

4. Your structure should look like:
   ```
   obsidian-vault/
   └── content/
   ```

5. **Important:** Don't create a `.git` folder here yet. If you plan to version control this vault, you'll do that later, and you'll need to understand that the `content/` folder is what matters for the repository structure.

### Verify
You should see:
- ✅ An Obsidian vault folder created
- ✅ A `content/` folder inside it
- ✅ The vault folder is ready for Obsidian

---

## Step 4: Open Vault in Obsidian

### What This Step Does
This opens your vault in Obsidian so Obsidian can initialize its configuration files.

### Instructions
1. Open **Obsidian** (Windows key → type "obsidian")

2. If this is your first time:
   - Click **Open folder as vault**
   - Navigate to your `obsidian-vault` folder
   - Click **Select Folder**

3. If you already have Obsidian open:
   - Click the vault switcher (folder icon, bottom left)
   - Click **Open another vault** → **Open folder as vault**
   - Navigate to your `obsidian-vault` folder
   - Click **Select Folder**

4. Obsidian will create a `.obsidian` folder automatically (this contains settings)

5. Your vault should now be open in Obsidian

### Verify
You should see:
- ✅ Obsidian is open with your vault loaded
- ✅ You can see the file explorer on the left
- ✅ The `content/` folder is visible in Obsidian

---

## Step 5: Create Your First Note in Content Folder

### What This Step Does
This creates your first note in the `content/` folder to establish the pattern.

### Instructions
1. In Obsidian's file explorer, click on the `content` folder

2. Click the **New note** button (or press Ctrl+N)

3. Name it `index` (this will create `index.md`)

4. Add some content:
   ```markdown
   # My Knowledge Base
   
   Welcome to my Obsidian knowledge base!
   
   This vault uses a special structure where published content lives in the `content/` folder.
   ```

5. Save the file (Ctrl+S)

6. Create a subfolder in `content/` for organization:
   - Right-click on `content` in the file explorer
   - Select **New folder**
   - Name it `notes` or `learning` or similar

### Verify
You should have:
- ✅ An `index.md` file in the `content/` folder
- ✅ At least one subfolder in `content/` for organization
- ✅ Understanding that all your notes go in `content/`, not at the root

---

## Step 6: Document the Structure

### What This Step Does
Create a README at the root of your vault to document the special structure.

### Instructions
1. In Obsidian, create a new note at the root level (not in `content/`)
   - Click the root folder in the file explorer
   - Click **New note**
   - Name it `README`

2. Add this content:
   ```markdown
   # Obsidian Vault Structure
   
   This vault uses a special structure for publishing:
   
   - **content/** - All published notes and materials go here
   - **.obsidian/** - Obsidian configuration (auto-created, don't edit manually)
   - **README.md** - This file (at root for documentation)
   
   ## Important Notes
   
   - All your notes should be created in the `content/` folder
   - The `content/` folder is what gets published
   - This structure is different from standard Git repositories
   - If version controlling this vault, the `content/` folder structure needs to be considered
   ```

3. Save the file

### Verify
You should have:
- ✅ A README.md at the root of your vault
- ✅ Documentation explaining the special structure
- ✅ Clear notes about where content goes

---

## Expected State at the End of This Exercise

You should now have:

```
obsidian-vault/
├── .obsidian/          # Auto-created by Obsidian
├── content/            # Your published content
│   ├── index.md
│   └── notes/          # (or whatever subfolder you created)
└── README.md           # Documentation
```

**In Obsidian:**
- ✅ Vault is open and working
- ✅ You can create notes in the `content/` folder
- ✅ You understand the special structure

---

## Why This Matters

Understanding Obsidian's structure:
- **Prevents confusion**: You know where to put notes (in `content/`)
- **Enables publishing**: If you want to publish your vault, the structure is already correct
- **Shows flexibility**: Different tools have different organizational needs
- **Professional practice**: Understanding tool-specific requirements is important

**Key takeaway:** Not all tools use standard repository structures. Obsidian is a special case where the published content lives in a `content/` subfolder. If you plan to use Obsidian for publishing (like this course does), you need this structure. If you're just using it for personal notes, you can use a simpler structure, but understanding this pattern helps you adapt to different tools.

---

## Next Steps

- [[c01-found/c1s1-files/index#Special Cases: Obsidian Knowledge Management|Return to Lecture]] - Go back to the lecture section that introduced Obsidian as a special case.
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
