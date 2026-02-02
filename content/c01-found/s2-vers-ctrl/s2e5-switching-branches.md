---
title: "Exercise 5: Switching Branches"
description: "Make real file changes on a branch and observe branch isolation in action."
tags: [git, github, branches, checkout, beginner, workbook]
draft: false
date: "2026-01-30"
---

# Exercise 5: Switching Branches

**This exercise continues from Exercise 4. You must complete Exercises 1-4 first.**

**This exercise is a standalone technical manual. Follow each step exactly.**

**Time Required:** 20-25 minutes

---

## Prerequisites Check

Before starting, verify:

1. ✅ **Exercises 1-4 completed**
   - Repository `version-control-portfolio` exists
   - Repository is open in VS Code
   - You're in the repository folder in terminal
   - Only `main` branch exists

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
**If not, complete Exercise 4 first.**

---

## What You Will Accomplish

By the end of this exercise, you will have:

- Created a branch for new work
- Created a file on the branch
- Committed the file to the branch
- Switched back to `main` and seen the file disappear
- Switched back to the branch and seen the file return
- Understood that commits belong to branches

---

## Step 1: Create and Switch to a New Branch

### 1.1: Create Branch Named "feature-about"

1. In the VS Code terminal, type exactly:
   ```bash
   git branch feature-about
   ```
2. Press **Enter**

**Expected Result:** No error message, prompt returns.

### 1.2: Switch to the New Branch

1. In the terminal, type exactly:
   ```bash
   git checkout feature-about
   ```
2. Press **Enter**

**Expected Output:**
```
Switched to branch 'feature-about'
```

### 1.3: Verify You're on the Branch

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch feature-about
Your branch is based on 'origin/main', but the upstream branch is missing.
nothing to commit, working tree clean
```

**"On branch feature-about" confirms you're on the new branch.**

---

## Step 2: Create a File on the Branch

### 2.1: Create about.html File

1. In VS Code, look at the file explorer sidebar (left side)
2. Right-click in the empty space below `index.html`
3. Click **New File**
4. Type exactly: `about.html`
5. Press **Enter**

**Expected Result:** A new file `about.html` appears in the file explorer and opens in the editor.

### 2.2: Add HTML Content

1. In the `about.html` file (now open in the editor), type exactly:
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>About - Version Control Portfolio</title>
   </head>
   <body>
       <h1>About This Project</h1>
       <p>This page demonstrates branch isolation in Git.</p>
       <p>This file exists only on the feature-about branch.</p>
   </body>
   </html>
   ```

2. Press **Ctrl + S** to save the file

**Expected Result:** The file is saved.

### 2.3: Verify File Creation

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch feature-about
Your branch is based on 'origin/main', but the upstream branch is missing.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)
```

**If you see `about.html` listed under "Untracked files", proceed to Step 3.**
**If not, make sure the file is saved (Ctrl + S).**

---

## Step 3: Stage and Commit the File

### 3.1: Stage the File

1. In the terminal, type exactly:
   ```bash
   git add about.html
   ```
2. Press **Enter**

**Expected Result:** No error message, prompt returns.

### 3.2: Verify File is Staged

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch feature-about
Your branch is based on 'origin/main', but the upstream branch is missing.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
        new file:   about.html
```

**If you see `about.html` under "Changes to be committed", proceed to Step 3.3.**

### 3.3: Commit the File

1. In the terminal, type exactly:
   ```bash
   git commit -m "add about.html page"
   ```
2. Press **Enter**

**Expected Output:**
```
[feature-about ghi7890] add about.html page
 1 file changed, 10 insertions(+)
 create mode 100644 about.html
```

**The commit hash (ghi7890) will be different - that's normal.**

### 3.4: Verify Commit Success

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch feature-about
Your branch is based on 'origin/main', but the upstream branch is missing.
nothing to commit, working tree clean
```

**"nothing to commit, working tree clean" confirms the commit was successful.**

---

## Step 4: Verify File Exists on Branch

### 4.1: List Files

1. In the terminal, type exactly:
   ```bash
   ls
   ```
2. Press **Enter**

**Expected Output:**
```
about.html  index.html  README.md
```

**All three files should be listed, including `about.html`.**

### 4.2: View Commit History

1. In the terminal, type exactly:
   ```bash
   git log --oneline
   ```
2. Press **Enter**

**Expected Output:**
```
ghi7890 (HEAD -> feature-about) add about.html page
def5678 (origin/main) add index.html file
abc1234 Initial commit
```

**Key observations:**
- ✅ `HEAD -> feature-about` shows you're on the feature branch
- ✅ Your commit "add about.html page" is at the top
- ✅ This commit exists only on `feature-about`, not on `main`

---

## Step 5: Switch Back to Main

### 5.1: Switch to Main Branch

1. In the terminal, type exactly:
   ```bash
   git checkout main
   ```
2. Press **Enter**

**Expected Output:**
```
Switched to branch 'main'
```

### 5.2: Verify You're on Main

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

**"On branch main" confirms you're on main.**

### 5.3: Critical Visual Check - File Disappears

**Look at the VS Code file explorer (left sidebar).**

**Expected Result:**
- ✅ `README.md` is visible
- ✅ `index.html` is visible
- ❌ `about.html` is **NOT visible**

**This is correct and expected!**
**The file exists on `feature-about` but not on `main`.**

### 5.4: Verify Files in Terminal

1. In the terminal, type exactly:
   ```bash
   ls
   ```
2. Press **Enter**

**Expected Output:**
```
index.html  README.md
```

**`about.html` is not listed because it doesn't exist on `main`.**

### 5.5: View Commit History on Main

1. In the terminal, type exactly:
   ```bash
   git log --oneline
   ```
2. Press **Enter**

**Expected Output:**
```
def5678 (HEAD -> main, origin/main) add index.html file
abc1234 Initial commit
```

**Key observations:**
- ✅ `HEAD -> main` shows you're on main
- ✅ The "add about.html page" commit is **not** in this history
- ✅ Only commits that exist on `main` are shown

**This demonstrates branch isolation - commits belong to specific branches.**

---

## Step 6: Switch Back to Feature Branch

### 6.1: Switch to Feature Branch

1. In the terminal, type exactly:
   ```bash
   git checkout feature-about
   ```
2. Press **Enter**

**Expected Output:**
```
Switched to branch 'feature-about'
```

### 6.2: Critical Visual Check - File Returns

**Look at the VS Code file explorer (left sidebar).**

**Expected Result:**
- ✅ `README.md` is visible
- ✅ `index.html` is visible
- ✅ `about.html` is **visible again**

**The file reappeared because you're back on the branch where it exists.**

### 6.3: Verify Files in Terminal

1. In the terminal, type exactly:
   ```bash
   ls
   ```
2. Press **Enter**

**Expected Output:**
```
about.html  index.html  README.md
```

**All three files are listed again.**

---

## Step 7: Understand What Happened

### 7.1: Key Concepts Demonstrated

1. **Files belong to branches:** When you commit a file on a branch, it exists only on that branch
2. **Switching branches changes your view:** Files appear and disappear based on which branch you're on
3. **No data is lost:** The file still exists in Git's history, just not visible on `main`
4. **Commits are branch-specific:** Commits made on a branch don't exist on other branches until merged

### 7.2: This is Branch Isolation

**Branch isolation means:**
- Work on `feature-about` doesn't affect `main`
- You can experiment safely
- Multiple people can work on different branches
- `main` stays stable and working

---

## Expected Final State

After completing this exercise, you should have:

- ✅ `main` branch: Contains `README.md` and `index.html` only
- ✅ `feature-about` branch: Contains `README.md`, `index.html`, and `about.html`
- ✅ One commit on `feature-about` that doesn't exist on `main`
- ✅ Understanding that files and commits belong to branches

**Important:** Do not delete the `feature-about` branch yet. You'll use it in Exercise 6.

---

## Troubleshooting

### Problem: File doesn't disappear when switching to main

**Solution:**
- Make sure you committed the file on the branch (`git commit`)
- Check that you're actually on `main` (`git status`)
- Try closing and reopening VS Code

### Problem: "error: pathspec 'feature-about' did not match any file(s)"

**Solution:**
- The branch doesn't exist
- Create it first: `git branch feature-about`
- Then switch: `git checkout feature-about`

### Problem: Can't switch branches

**Solution:**
- Make sure all changes are committed (`git status` should show clean)
- If you have uncommitted changes, commit them first or use `git stash`

---

## Next Steps

- [[c01-found/s2-vers-ctrl/index#Branching: Working Safely|Return to Lecture]] - Revisit the branching and branch isolation concepts in the lecture before continuing.

---

## Navigation

**Previous Exercise:** [[s2-vers-ctrl/s2e4-creating-branches|Exercise 4: Creating Branches]]

**Next Exercise:** [[s2-vers-ctrl/s2e6-creating-pull-requests|Exercise 6: Creating Pull Requests]]

**Home:** [[index|Main Course Page]]

**Return to Section:** [[s2-vers-ctrl/index|Version Control Section]]
