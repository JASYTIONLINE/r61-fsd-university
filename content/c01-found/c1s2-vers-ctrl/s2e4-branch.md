---
title: "EC1S2E4: Creating Branches"
description: Learn to create, list, switch between, and delete Git branches while protecting main.
tags:
  - git
  - github
  - branching
  - beginner
  - workbook
draft: false
date: 2026-01-30
---

# Exercise 4: Creating Branches

**This exercise continues from Exercise 3. You must complete Exercises 1-3 first.**

**This exercise is a standalone technical manual. Follow each step exactly.**

**Time Required:** 15-20 minutes

---

## Prerequisites Check

Before starting, verify:

1. ✅ **Exercises 1-3 completed**
   - Repository `version-control-portfolio` exists
   - Repository is open in VS Code
   - You're in the repository folder in terminal
   - `index.html` file exists and is committed

2. ✅ **Current State Verification**
   - Open VS Code terminal (Ctrl + ~)
   - Type: `git status`
   - Press Enter

**Expected Output:**
```
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

**If you see this, proceed.**
**If not, complete Exercise 3 first.**

---

## What You Will Accomplish

By the end of this exercise, you will have:

- Learned what branches are
- Created a new branch
- Switched between branches
- Listed branches
- Deleted a branch
- Understood branch isolation

**Note:** This exercise creates and deletes a branch for learning purposes. No files will be permanently changed.

---

## Step 1: Understand Branches

### 1.1: What is a Branch?

**Branch:** A parallel version of your project that allows you to work on features without affecting the main code.

- `main` branch: The primary branch (your working code)
- Feature branches: Temporary branches for new work
- Branches are lightweight and safe to create

### 1.2: Why Use Branches?

- Protect `main` from breaking changes
- Work on multiple features simultaneously
- Experiment safely without consequences
- Collaborate without conflicts

---

## Step 2: List Existing Branches

### 2.1: View Current Branches

1. In the VS Code terminal, type exactly:
   ```bash
   git branch
   ```
2. Press **Enter**

**Expected Output:**
```
* main
```

**The asterisk (*) indicates which branch you're currently on.**
**At this point, only `main` exists.**

### 2.2: Verify Current Branch

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

**"On branch main" confirms you're on the main branch.**

---

## Step 3: Create a New Branch

### 3.1: Create Branch Named "feature-styling"

1. In the terminal, type exactly:
   ```bash
   git branch feature-styling
   ```
2. Press **Enter**

**Expected Result:** No error message, prompt returns.

**What happened:** A new branch was created, but you're still on `main`.

### 3.2: Verify Branch Was Created

1. In the terminal, type exactly:
   ```bash
   git branch
   ```
2. Press **Enter**

**Expected Output:**
```
* main
  feature-styling
```

**You should see:**
- ✅ `main` with asterisk (you're on this branch)
- ✅ `feature-styling` without asterisk (branch exists but you're not on it)

**If you see both branches, proceed to Step 4.**
**If not, check for typos in Step 3.1.**

---

## Step 4: Switch to the New Branch

### 4.1: Switch Using Checkout

1. In the terminal, type exactly:
   ```bash
   git checkout feature-styling
   ```
2. Press **Enter**

**Expected Output:**
```
Switched to branch 'feature-styling'
```

**What happened:** You switched from `main` to `feature-styling`.

### 4.2: Verify Branch Switch

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch feature-styling
Your branch is based on 'origin/main', but the upstream branch is missing.
nothing to commit, working tree clean
```

**"On branch feature-styling" confirms you're now on the new branch.**

### 4.3: List Branches Again

1. In the terminal, type exactly:
   ```bash
   git branch
   ```
2. Press **Enter**

**Expected Output:**
```
  main
* feature-styling
```

**The asterisk (*) is now on `feature-styling`, confirming you switched branches.**

---

## Step 5: Understand Branch Isolation

### 5.1: Verify Files Are the Same

1. In the terminal, type exactly:
   ```bash
   ls
   ```
2. Press **Enter**

**Expected Output:**
```
index.html  README.md
```

**Both files exist on this branch because the branch was created from `main`.**

### 5.2: View Commit History

1. In the terminal, type exactly:
   ```bash
   git log --oneline
   ```
2. Press **Enter**

**Expected Output:**
```
def5678 (HEAD -> feature-styling, origin/main) add index.html file
abc1234 Initial commit
```

**Key observation:**
- `HEAD -> feature-styling` shows you're on the feature branch
- Both branches point to the same commits right now
- Branches only diverge after you make commits

---

## Step 6: Switch Back to Main

### 6.1: Return to Main Branch

1. In the terminal, type exactly:
   ```bash
   git checkout main
   ```
2. Press **Enter**

**Expected Output:**
```
Switched to branch 'main'
```

### 6.2: Verify You're on Main

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

**"On branch main" confirms you're back on main.**

### 6.3: Verify Files Are Still There

1. In the terminal, type exactly:
   ```bash
   ls
   ```
2. Press **Enter**

**Expected Output:**
```
index.html  README.md
```

**Files are unchanged because no commits were made on the feature branch.**

---

## Step 7: Delete the Feature Branch

### 7.1: Understand Branch Deletion

**Why delete branches?**
- Keeps your repository clean
- Removes temporary work that's been merged
- Prevents branch clutter

**Important:** You can only delete a branch if you're not currently on it.

### 7.2: Delete the Feature Branch

1. Make sure you're on `main` (verify with `git status`)
2. In the terminal, type exactly:
   ```bash
   git branch -d feature-styling
   ```
3. Press **Enter**

**Expected Output:**
```
Deleted branch feature-styling (was def5678).
```

**The branch is deleted.**

### 7.3: Verify Branch Deletion

1. In the terminal, type exactly:
   ```bash
   git branch
   ```
2. Press **Enter**

**Expected Output:**
```
* main
```

**Only `main` remains. The feature branch is deleted.**

---

## Step 8: Understand What You Learned

### 8.1: Key Concepts

1. **Branches are lightweight:** Creating a branch doesn't copy files
2. **Branches start from current state:** New branches begin where you create them
3. **Switching is safe:** You can switch branches without losing work
4. **Branches isolate work:** Changes on one branch don't affect others until merged

### 8.2: Professional Workflow

**Standard workflow:**
1. Create a branch for new work
2. Make changes and commits on the branch
3. Merge the branch into `main` when complete
4. Delete the branch after merging

---

## Expected Final State

After completing this exercise, you should have:

- ✅ Only `main` branch exists
- ✅ All files unchanged (`README.md` and `index.html`)
- ✅ Working tree clean
- ✅ Understanding of how branches work

---

## Troubleshooting

### Problem: "error: cannot delete branch 'feature-styling'"

**Solution:**
- Make sure you're on `main` branch (`git checkout main`)
- If the branch has unmerged changes, use `git branch -D feature-styling` (capital D forces deletion)
- In this exercise, we didn't make commits, so `-d` should work

### Problem: "fatal: a branch named 'feature-styling' already exists"

**Solution:**
- The branch already exists
- List branches with `git branch` to see it
- Switch to it with `git checkout feature-styling` or delete it first

### Problem: Can't switch branches

**Solution:**
- Make sure you have no uncommitted changes (`git status` should show clean)
- Commit or stash any changes first
- Then switch branches

---
 #### Next Steps: - Return to the [Version Control Lecture](c01-found/c1s2-vers-ctrl/index#5.-Switching-Branches)
5. Switching Branches

---
## Navigation
[Back to the Top](#Getting%20Started)
### Section 0 Map
- [C1S2E1:](c01-found/c1s2-vers-ctrl/s2e1-auth-gh) Authenticating Git with GitHub
- [C1S2E2:](c01-found/c1s2-vers-ctrl/s2e2-creat-repo)  Creating a GitHub Repository
- [C1S2E3:](c01-found/c1s2-vers-ctrl/s2e3-push) Pushing Changes to your Remote Repository
- [C1S2E4:](c01-found/c1s2-vers-ctrl/s2e4-branch) Creating Branches in your Repository
- [C1S2E5:](c01-found/c1s2-vers-ctrl/s2e5-switch) Switching Between Branches
- [C1S2E6:](c01-found/c1s2-vers-ctrl/s2e6-pull) Creating Pull Requests
- [C1S2E7:](c01-found/c1s2-vers-ctrl/s2e7-merge) Merging Branches
- [C1S2E8:](c01-found/c1s2-vers-ctrl/s2e8-recap) Recap and Workflow Habits

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
