---
title: "Exercise 3: Pushing Changes"
description: "Create files, stage them, commit them, and push to GitHub to synchronize local and remote repositories."
tags: [git, github, push, commits, beginner, workbook]
draft: false
date: "2026-01-30"
---

# Exercise 3: Pushing Changes

**This exercise continues from Exercise 2. You must complete Exercise 2 first.**

**This exercise is a standalone technical manual. Follow each step exactly.**

**Time Required:** 20-25 minutes

---

## Prerequisites Check

Before starting, verify:

1. ✅ **Exercise 2 completed**
   - Repository `version-control-portfolio` exists
   - Repository is open in VS Code
   - You're in the repository folder in terminal

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
**If not, complete Exercise 2 first.**

---

## What You Will Accomplish

By the end of this exercise, you will have:

- Created an `index.html` file
- Staged the file with Git
- Committed the file with a clear message
- Pushed the commit to GitHub
- Verified local and remote are synchronized

---

## Step 1: Create index.html File

### 1.1: Create New File in VS Code

1. In VS Code, look at the file explorer sidebar (left side)
2. Right-click in the empty space below `README.md`
3. Click **New File**
4. Type exactly: `index.html`
5. Press **Enter**

**Expected Result:** A new file `index.html` appears in the file explorer and opens in the editor.

### 1.2: Add HTML Content

1. In the `index.html` file (now open in the editor), type exactly:
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Version Control Portfolio</title>
   </head>
   <body>
       <h1>Welcome to My Portfolio</h1>
       <p>This repository demonstrates my version control skills.</p>
   </body>
   </html>
   ```

2. Press **Ctrl + S** to save the file

**Expected Result:** The file is saved. You may see a dot or indicator next to the filename showing it's been modified.

### 1.3: Verify File Creation

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html

nothing added to commit but untracked files present (use "git add" to track)
```

**If you see `index.html` listed under "Untracked files", proceed to Step 2.**
**If not, make sure the file is saved (Ctrl + S) and you're in the repository folder.**

---

## Step 2: Stage the File

### 2.1: Understand Staging

**What is staging?**
- Staging tells Git which files to include in the next commit
- Files must be staged before they can be committed
- You can stage multiple files at once

### 2.2: Stage index.html

1. In the VS Code terminal, type exactly:
   ```bash
   git add index.html
   ```
2. Press **Enter**

**Expected Result:** No error message, prompt returns.

### 2.3: Verify File is Staged

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
        new file:   index.html
```

**If you see `index.html` under "Changes to be committed", proceed to Step 3.**
**If not, repeat Step 2.2 and check for typos.**

---

## Step 3: Commit the File

### 3.1: Understand Commits

**What is a commit?**
- A commit is a snapshot of your project at a specific moment
- Each commit has a message explaining what changed
- Commits are saved locally first (not automatically sent to GitHub)

### 3.2: Create the Commit

1. In the terminal, type exactly:
   ```bash
   git commit -m "add index.html file"
   ```
2. Press **Enter**

**Expected Output:**
```
[main abc1234] add index.html file
 1 file changed, 10 insertions(+)
 create mode 100644 index.html
```

**The commit hash (abc1234) will be different - that's normal.**

### 3.3: Verify Commit Success

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

**Key indicators:**
- ✅ "Your branch is ahead of 'origin/main' by 1 commit" - This means you have a local commit not yet on GitHub
- ✅ "nothing to commit, working tree clean" - All changes are committed

**If you see this, proceed to Step 4.**
**If you see errors, check the commit message for typos.**

---

## Step 4: Understand Remotes

### 4.1: What is a Remote?

**Remote:** A saved connection to a GitHub repository.

- Your **local repository** lives on your computer
- Your **remote repository** lives on GitHub
- The default remote is named `origin`

### 4.2: Verify Remote Connection

1. In the terminal, type exactly:
   ```bash
   git remote -v
   ```
2. Press **Enter**

**Expected Output:**
```
origin  https://github.com/your-username/version-control-portfolio.git (fetch)
origin  https://github.com/your-username/version-control-portfolio.git (push)
```

**If you see both fetch and push URLs, the remote is configured correctly.**
**If not, you may need to re-clone the repository (see Exercise 2).**

---

## Step 5: Push to GitHub

### 5.1: Understand Pushing

**What is pushing?**
- Pushing sends your local commits to GitHub
- This synchronizes your local repository with the remote
- After pushing, your commits are visible on GitHub

### 5.2: Push Your Commit

1. In the terminal, type exactly:
   ```bash
   git push -u origin main
   ```
2. Press **Enter**

**Expected Output:**
```
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), XXX bytes | XXX.XX MiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/your-username/version-control-portfolio.git
   abc1234..def5678  main -> main
branch 'main' set up to track 'origin/main'.
```

**The `-u` flag sets up tracking so future pushes can use just `git push`.**

**If you see "main -> main" and no errors, proceed to Step 6.**
**If you see authentication errors, complete Exercise 1 first.**

### 5.3: Verify Push Success

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

**"Your branch is up to date with 'origin/main'" means local and remote are synchronized.**

---

## Step 6: Verify on GitHub

### 6.1: Open Repository on GitHub

1. Open your web browser
2. Navigate to: `https://github.com/your-username/version-control-portfolio`
   - Replace `your-username` with your actual GitHub username
3. Refresh the page (F5 or Ctrl + R)

### 6.2: Verify Files on GitHub

On the GitHub repository page, verify you see:

- ✅ `README.md` file listed
- ✅ `index.html` file listed
- ✅ Both files visible in the file list

### 6.3: Verify Commit on GitHub

1. On the GitHub repository page, look for the commit count or history
2. Click on the commit history (or the number of commits)
3. You should see your commit: "add index.html file"

**If you see the file and commit on GitHub, proceed to Step 7.**
**If not, wait a few seconds and refresh the page.**

---

## Step 7: Final Verification

### 7.1: View Commit History Locally

1. In the VS Code terminal, type exactly:
   ```bash
   git log --oneline
   ```
2. Press **Enter**

**Expected Output:**
```
def5678 (HEAD -> main, origin/main) add index.html file
abc1234 Initial commit
```

**You should see:**
- ✅ Your commit: "add index.html file"
- ✅ Initial commit
- ✅ `(HEAD -> main, origin/main)` showing both local and remote are on the same commit

### 7.2: List All Files

1. In the terminal, type exactly:
   ```bash
   ls
   ```
2. Press **Enter**

**Expected Output:**
```
index.html  README.md
```

**Both files should be listed.**

---

## Expected Final State

After completing this exercise, you should have:

- ✅ `index.html` file created locally
- ✅ File committed to local repository
- ✅ Commit pushed to GitHub
- ✅ Both `README.md` and `index.html` visible on GitHub
- ✅ Local and remote repositories synchronized
- ✅ Working tree clean

---

## Troubleshooting

### Problem: "fatal: not a git repository"

**Solution:**
- You're not in the repository folder
- Run `pwd` to check your location
- Run `cd version-control-portfolio` to navigate to the repository

### Problem: "nothing to commit, working tree clean" when trying to commit

**Solution:**
- The file may not be saved (press Ctrl + S)
- The file may not be staged (run `git add index.html` first)
- Check `git status` to see the current state

### Problem: "fatal: The current branch main has no upstream branch"

**Solution:**
- Use `git push -u origin main` (the `-u` flag sets up tracking)
- If that doesn't work, verify the remote exists: `git remote -v`

### Problem: Files don't appear on GitHub after push

**Solution:**
- Wait 10-15 seconds and refresh the GitHub page
- Check `git status` to verify the push completed
- Verify you're looking at the correct repository on GitHub

---

## Navigation

**Previous Exercise:** [[s2-vers-ctrl/s2e2-creating-repository|Exercise 2: Creating Repository]]

**Next Exercise:** [[s2-vers-ctrl/s2e4-creating-branches|Exercise 4: Creating Branches]]

**Home:** [[index 1|Main Course Page]]

**Return to Section:** [[s2-vers-ctrl/index|Version Control Section]]
