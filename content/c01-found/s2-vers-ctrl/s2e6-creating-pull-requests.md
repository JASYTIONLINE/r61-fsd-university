---
title: "Exercise 6: Creating Pull Requests"
description: "Learn the fork workflow: fork a repository, clone your fork, add upstream remote, create a branch, push changes, and create a pull request."
tags: [git, github, pull-request, fork, upstream, collaboration, beginner, workbook]
draft: false
date: "2026-01-30"
---

# Exercise 6: Creating Pull Requests

**This exercise continues from Exercise 5. You must complete Exercises 1-5 first.**

**This exercise is a standalone technical manual. Follow each step exactly.**

**Time Required:** 30-40 minutes

---

## Prerequisites Check

Before starting, verify:

1. ✅ **Exercises 1-5 completed**
   - Repository `version-control-portfolio` exists and is working
   - You understand basic Git commands
   - You can create branches and make commits
   - VS Code terminal is configured with Git Bash

2. ✅ **Current Requirements**
   - VS Code open
   - Web browser open
   - Working internet connection
   - GitHub account logged in

**If any prerequisite is missing, complete it before proceeding.**

---

## What You Will Accomplish

By the end of this exercise, you will have:

- Forked a repository on GitHub
- Cloned your fork locally
- Added an upstream remote (connection to original repository)
- Created a branch on your fork
- Made changes and committed them
- Pushed your branch to your fork
- Created a pull request to the original repository
- Understood the difference between origin and upstream

---

## Understanding: Fork vs Clone

Before we start, understand the difference:

- **Clone**: Creates a local copy of a repository you have access to
- **Fork**: Creates your own copy of someone else's repository on GitHub

**Why fork?**
- You want to contribute to someone else's project
- You want to experiment without affecting the original
- You want to learn from others' code
- You want to build your portfolio through contributions

---

## Step 1: Fork a Repository on GitHub

### 1.1: Find a Repository to Fork

For this exercise, we'll use a test repository. You can:

1. **Option A (Recommended):** Create a test repository in your own GitHub account
   - Go to GitHub.com
   - Create a new repository named `test-repo-for-prs`
   - Add a README.md file
   - Make it public
   - This will be your "original" repository

2. **Option B:** Use an existing public repository
   - Find any public repository on GitHub
   - We'll use it for practice

**For this exercise, we'll assume you're using Option A (your own test repo).**

### 1.2: Fork the Repository

1. Navigate to your test repository on GitHub
2. Click the **Fork** button in the top right corner
3. If prompted, select your account as the destination
4. Wait for the fork to complete

**Expected Result:** You now have a copy of the repository in your account.

**Note:** If you're forking your own repository, GitHub will show a message. That's okay—you can still practice the workflow.

---

## Step 2: Clone Your Fork Locally

### 2.1: Get Your Fork's URL

1. On your fork's page on GitHub, click the green **Code** button
2. Make sure **HTTPS** is selected
3. Click the copy icon next to the URL
4. The URL should look like: `https://github.com/YOUR-USERNAME/test-repo-for-prs.git`

### 2.2: Navigate to Your Projects Folder

1. Open VS Code terminal (Ctrl + ~)
2. Navigate to your `knowledge-base/projects/` folder:
   ```bash
   cd ~/knowledge-base/projects
   ```
   Or on Windows:
   ```bash
   cd C:\Users\YourName\knowledge-base\projects
   ```

### 2.3: Clone Your Fork

1. In the terminal, type exactly (replace with your fork's URL):
   ```bash
   git clone https://github.com/YOUR-USERNAME/test-repo-for-prs.git
   ```
2. Press **Enter**
3. Wait for the clone to complete

**Expected Output:**
```
Cloning into 'test-repo-for-prs'...
remote: Enumerating objects: X, done.
remote: Counting objects: 100% (X/X), done.
remote: Compressing objects: 100% (X/X), done.
remote: Total X (delta X), reused X (delta X), pack-reused X
Receiving objects: 100% (X/X), done.
```

### 2.4: Enter the Repository Folder

1. In the terminal, type:
   ```bash
   cd test-repo-for-prs
   ```
2. Press **Enter**

### 2.5: Verify the Clone

1. In the terminal, type:
   ```bash
   git remote -v
   ```
2. Press **Enter**

**Expected Output:**
```
origin  https://github.com/YOUR-USERNAME/test-repo-for-prs.git (fetch)
origin  https://github.com/YOUR-USERNAME/test-repo-for-prs.git (push)
```

**This shows that `origin` points to your fork. This is correct.**

---

## Step 3: Add Upstream Remote

### 3.1: Understand Origin vs Upstream

- **Origin**: Your fork (where you push your changes)
- **Upstream**: The original repository (where you want to contribute)

**Why add upstream?**
- To pull the latest changes from the original repository
- To keep your fork up to date
- To understand where your contributions will go

### 3.2: Get the Original Repository URL

1. Navigate to the **original** repository on GitHub (not your fork)
2. Click the green **Code** button
3. Copy the HTTPS URL
4. The URL should look like: `https://github.com/ORIGINAL-OWNER/test-repo-for-prs.git`

**Note:** If you created the test repo yourself, the original and fork URLs are the same. That's fine for practice.

### 3.3: Add Upstream Remote

1. In the terminal (still in your cloned repository), type exactly (replace with the original repo URL):
   ```bash
   git remote add upstream https://github.com/ORIGINAL-OWNER/test-repo-for-prs.git
   ```
2. Press **Enter**

**Expected Result:** No error message, prompt returns.

### 3.4: Verify Both Remotes

1. In the terminal, type:
   ```bash
   git remote -v
   ```
2. Press **Enter**

**Expected Output:**
```
origin    https://github.com/YOUR-USERNAME/test-repo-for-prs.git (fetch)
origin    https://github.com/YOUR-USERNAME/test-repo-for-prs.git (push)
upstream  https://github.com/ORIGINAL-OWNER/test-repo-for-prs.git (fetch)
upstream  https://github.com/ORIGINAL-OWNER/test-repo-for-prs.git (push)
```

**You should see both `origin` (your fork) and `upstream` (original).**

---

## Step 4: Create a Branch for Your Changes

### 4.1: Check Current Branch

1. In the terminal, type:
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

### 4.2: Create a New Branch

1. In the terminal, type:
   ```bash
   git branch feature-add-contribution
   ```
2. Press **Enter**

### 4.3: Switch to the New Branch

1. In the terminal, type:
   ```bash
   git checkout feature-add-contribution
   ```
2. Press **Enter**

**Expected Output:**
```
Switched to branch 'feature-add-contribution'
```

### 4.4: Verify You're on the Branch

1. In the terminal, type:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch feature-add-contribution
nothing to commit, working tree clean
```

---

## Step 5: Make Changes and Commit

### 5.1: Create a New File

1. In VS Code, create a new file named `CONTRIBUTING.md`
2. Add the following content:
   ```markdown
   # Contributing

   This is a test contribution to demonstrate the pull request workflow.

   ## How to Contribute

   1. Fork this repository
   2. Create a branch for your changes
   3. Make your changes
   4. Create a pull request

   Thank you for contributing!
   ```
3. Save the file (Ctrl + S)

### 5.2: Stage the File

1. In the terminal, type:
   ```bash
   git add CONTRIBUTING.md
   ```
2. Press **Enter**

### 5.3: Commit the File

1. In the terminal, type:
   ```bash
   git commit -m "Add CONTRIBUTING.md file"
   ```
2. Press **Enter**

**Expected Output:**
```
[feature-add-contribution abc1234] Add CONTRIBUTING.md file
 1 file changed, 10 insertions(+)
 create mode 100644 CONTRIBUTING.md
```

### 5.4: Verify the Commit

1. In the terminal, type:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch feature-add-contribution
nothing to commit, working tree clean
```

---

## Step 6: Push Your Branch to Your Fork

### 6.1: Push the Branch

1. In the terminal, type:
   ```bash
   git push -u origin feature-add-contribution
   ```
2. Press **Enter**

**Expected Output:**
```
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to X threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), XXX bytes | XXX bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (0/0), done.
To https://github.com/YOUR-USERNAME/test-repo-for-prs.git
 * [new branch]      feature-add-contribution -> feature-add-contribution
Branch 'feature-add-contribution' set up to track remote branch 'feature-add-contribution' from 'origin'.
```

**The `-u` flag sets up tracking so future pushes are simpler.**

### 6.2: Verify on GitHub

1. Open your fork on GitHub in your browser
2. You should see a banner saying "feature-add-contribution had recent pushes"
3. Click the branch dropdown (it should say "main")
4. Select `feature-add-contribution`
5. You should see your `CONTRIBUTING.md` file

---

## Step 7: Create a Pull Request

### 7.1: Navigate to Pull Request Creation

1. On your fork's page on GitHub, click the **Contribute** button (or **Compare & pull request** banner)
2. You should see a page comparing your branch to the original repository's main branch

### 7.2: Fill Out the Pull Request

1. **Title:** 
   - Type: `Add CONTRIBUTING.md file`
   - This should be clear and descriptive

2. **Description:**
   - Type:
   ```markdown
   This PR adds a CONTRIBUTING.md file to help new contributors understand how to contribute to this project.
   
   ## Changes
   - Added CONTRIBUTING.md with basic contribution guidelines
   
   ## Testing
   - File created and committed on feature branch
   - Ready for review
   ```

3. **Review the changes:**
   - Scroll down to see the diff
   - Verify it shows your new file being added

### 7.3: Create the Pull Request

1. Click the green **Create pull request** button
2. Wait for the PR to be created

**Expected Result:** You see a new pull request page with your changes.

---

## Step 8: Understand the Pull Request

### 8.1: Review the PR Page

On the pull request page, you'll see:

- **Title and description** you wrote
- **Files changed** tab showing your diff
- **Conversation** tab for comments
- **Commits** tab showing your commit
- **Checks** tab (if CI/CD is set up)

### 8.2: Understand the Workflow

**What happens next in real projects:**

1. Repository maintainer reviews your PR
2. They may request changes
3. You make changes and push to the same branch
4. Maintainer approves and merges
5. Your changes become part of the original repository

**For this exercise:** Since it's your test repository, you can merge it yourself if you want.

---

## Step 9: Merge Your Own PR (Optional)

### 9.1: Merge the Pull Request

1. On the PR page, scroll down
2. Click the green **Merge pull request** button
3. Click **Confirm merge**
4. Optionally delete the branch after merging

**This completes the full workflow!**

---

## Key Concepts Demonstrated

### 9.1: What You Learned

1. **Forking**: Creating your own copy of someone else's repository
2. **Origin vs Upstream**: Understanding the difference between your fork and the original
3. **Branch-based contributions**: All changes go on a branch, not directly to main
4. **Pull Requests**: The professional way to contribute to projects
5. **Collaboration workflow**: How open-source and team projects work

### 9.2: Why This Matters

In professional development:
- You'll contribute to team repositories through PRs
- You'll review others' PRs
- You'll work with open-source projects
- PRs are the standard way to merge code in collaborative environments

---

## Expected Final State

After completing this exercise, you should have:

- ✅ Forked a repository on GitHub
- ✅ Cloned your fork locally
- ✅ Added upstream remote
- ✅ Created a branch for changes
- ✅ Made changes and committed them
- ✅ Pushed branch to your fork
- ✅ Created a pull request
- ✅ Understanding of origin vs upstream
- ✅ Understanding of the PR workflow

---

## Troubleshooting

### Problem: "fatal: remote upstream already exists"

**Solution:**
- The upstream remote is already added
- Check with `git remote -v`
- If you need to change it: `git remote set-url upstream NEW-URL`

### Problem: Can't push to fork

**Solution:**
- Verify you're pushing to `origin`, not `upstream`
- Check authentication: `gh auth status`
- Verify remote: `git remote -v`

### Problem: Can't see "Contribute" button

**Solution:**
- Make sure you've pushed your branch: `git push -u origin BRANCH-NAME`
- Refresh the GitHub page
- Check that you're on your fork, not the original repository

### Problem: PR shows wrong changes

**Solution:**
- Make sure you're comparing the right branches
- Verify your branch has the commits: `git log`
- Push again if needed: `git push`

---

## Navigation

**Previous Exercise:** [[s2-version-control/s2e5-switching-branches|Exercise 5: Switching Branches]]

**Next Exercise:** [[s2-version-control/s2e7-merging-branches|Exercise 7: Merging Branches]]

**Return to Section:** [[s2-version-control/index|Version Control Section]]
