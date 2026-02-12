---
title: "Exercise 7: Merging Branches"
description: "Merge branch work into main, push to GitHub, and clean up temporary learning artifacts."
tags: [git, github, merge, branches, beginner, workbook]
draft: false
date: "2026-01-30"
---

# Exercise 7: Merging Branches

**This exercise continues from Exercise 6. You must complete Exercises 1-6 first.**

**This exercise is a standalone technical manual. Follow each step exactly.**

**Time Required:** 25-30 minutes

---

## Prerequisites Check

Before starting, verify:

1. ✅ **Exercises 1-6 completed**
   - Repository `version-control-portfolio` exists
   - Repository is open in VS Code
   - You're in the repository folder in terminal
   - `feature-about` branch exists with `about.html` file committed

2. ✅ **Current State Verification**
   - Open VS Code terminal (Ctrl + ~)
   - Type: `git branch`
   - Press Enter

**Expected Output:**
```
  feature-about
* main
```

**You should see both branches. The asterisk should be on `main`.**

**If you're on `feature-about`, switch to main:**
```bash
git checkout main
```

**If you see this, proceed.**
**If not, complete Exercise 6 first.**

---

## What You Will Accomplish

By the end of this exercise, you will have:

- Merged `feature-about` branch into `main`
- Verified the merge was successful
- Removed the temporary `about.html` file (cleanup)
- Pushed the final state to GitHub
- Deleted the feature branch
- Ended with a clean, professional repository

---

## Step 1: Verify Starting State

### 1.1: Confirm You're on Main

1. In the VS Code terminal, type exactly:
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

**"On branch main" confirms you're on the correct branch.**

### 1.2: Verify Feature Branch Exists

1. In the terminal, type exactly:
   ```bash
   git branch
   ```
2. Press **Enter**

**Expected Output:**
```
  feature-about
* main
```

**Both branches should be listed. Asterisk on `main`.**

### 1.3: Verify about.html Doesn't Exist on Main

1. In the terminal, type exactly:
   ```bash
   ls
   ```
2. Press **Enter**

**Expected Output:**
```
index.html  README.md
```

**`about.html` should NOT be listed (it only exists on `feature-about`).**

**Look at VS Code file explorer - `about.html` should NOT be visible.**

---

## Step 2: Verify Feature Branch Content

### 2.1: Switch to Feature Branch

1. In the terminal, type exactly:
   ```bash
   git checkout feature-about
   ```
2. Press **Enter**

**Expected Output:**
```
Switched to branch 'feature-about'
```

### 2.2: Verify about.html Exists

1. In the terminal, type exactly:
   ```bash
   ls
   ```
2. Press **Enter**

**Expected Output:**
```
about.html  index.html  README.md
```

**`about.html` should be listed.**

**Look at VS Code file explorer - `about.html` should be visible.**

### 2.3: View Commit on Feature Branch

1. In the terminal, type exactly:
   ```bash
   git log --oneline -1
   ```
2. Press **Enter**

**Expected Output:**
```
ghi7890 (HEAD -> feature-about) add about.html page
```

**This confirms the commit exists on the feature branch.**

### 2.4: Return to Main

1. In the terminal, type exactly:
   ```bash
   git checkout main
   ```
2. Press **Enter**

**Expected Output:**
```
Switched to branch 'main'
```

---

## Step 3: Merge Feature Branch into Main

### 3.1: Understand Merging

**What is merging?**
- Merging combines changes from one branch into another
- After merging, the feature branch's commits become part of `main`
- Files from the feature branch appear on `main`

### 3.2: Perform the Merge

1. Make sure you're on `main` (verify with `git status`)
2. In the terminal, type exactly:
   ```bash
   git merge feature-about
   ```
3. Press **Enter**

**Expected Output:**
```
Updating def5678..ghi7890
Fast-forward
 about.html | 10 ++++++++++
 1 file changed, 10 insertions(+)
 create mode 100644 about.html
```

**"Fast-forward" means Git simply moved `main` forward to include the feature branch's commits.**

### 3.3: Verify Merge Success

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

**"Your branch is ahead of 'origin/main' by 1 commit" means the merge created a new commit on `main`.**

### 3.4: Critical Visual Check - File Appears

**Look at the VS Code file explorer (left sidebar).**

**Expected Result:**
- ✅ `README.md` is visible
- ✅ `index.html` is visible
- ✅ `about.html` is **now visible**

**The file appeared because the branch was merged into `main`.**

### 3.5: Verify Files in Terminal

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

### 3.6: View Commit History

1. In the terminal, type exactly:
   ```bash
   git log --oneline
   ```
2. Press **Enter**

**Expected Output:**
```
ghi7890 (HEAD -> main) add about.html page
def5678 (origin/main) add index.html file
abc1234 Initial commit
```

**Key observations:**
- ✅ `HEAD -> main` shows you're on main
- ✅ The "add about.html page" commit is now part of `main`'s history
- ✅ `main` is ahead of `origin/main` (the merge hasn't been pushed yet)

---

## Step 4: Remove Temporary Learning File

### 4.1: Understand Cleanup

**Why remove `about.html`?**
- This file was created only to demonstrate branch isolation
- The goal is to end with a clean, professional repository
- Final repository should contain only: `README.md` and `index.html`

### 4.2: Delete the File

1. In the terminal, type exactly:
   ```bash
   rm about.html
   ```
2. Press **Enter**

**Expected Result:** No error message, prompt returns.

**Note:** On Windows with Git Bash, `rm` works. If it doesn't, use: `del about.html`

### 4.3: Verify File Deletion

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 1 commit.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    about.html

no changes added to commit (use "git add" or "git commit -a")
```

**"deleted: about.html" confirms the file deletion is detected by Git.**

### 4.4: Stage the Deletion

1. In the terminal, type exactly:
   ```bash
   git add about.html
   ```
2. Press **Enter**

**Expected Result:** No error message, prompt returns.

**Note:** Staging a deleted file tells Git to include the deletion in the next commit.

### 4.5: Verify Deletion is Staged

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 1 commit.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
        deleted:    about.html
```

**"deleted: about.html" under "Changes to be committed" confirms it's staged.**

### 4.6: Commit the Cleanup

1. In the terminal, type exactly:
   ```bash
   git commit -m "remove temporary about.html file"
   ```
2. Press **Enter**

**Expected Output:**
```
[main jkl0123] remove temporary about.html file
 1 file changed, 10 deletions(-)
 delete mode 100644 about.html
```

**The commit hash (jkl0123) will be different - that's normal.**

### 4.7: Verify Cleanup Commit

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

**"Your branch is ahead of 'origin/main' by 2 commits" means:**
- 1 commit from the merge
- 1 commit from the cleanup

### 4.8: Verify Files Are Clean

1. In the terminal, type exactly:
   ```bash
   ls
   ```
2. Press **Enter**

**Expected Output:**
```
index.html  README.md
```

**Only `README.md` and `index.html` should remain.**

**Look at VS Code file explorer - `about.html` should NOT be visible.**

---

## Step 5: Push to GitHub

### 5.1: Push Merged and Cleaned Main

1. In the terminal, type exactly:
   ```bash
   git push
   ```
2. Press **Enter**

**Expected Output:**
```
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), XXX bytes | XXX.XX MiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/your-username/version-control-portfolio.git
   def5678..jkl0123  main -> main
```

**"main -> main" confirms the push was successful.**

### 5.2: Verify Push Success

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

**"Your branch is up to date with 'origin/main'" confirms local and remote are synchronized.**

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
- ❌ `about.html` should NOT be listed

**Only two files should be visible.**

### 6.3: Verify Commits on GitHub

1. On the GitHub repository page, click on the commit count or history
2. You should see commits including:
   - "remove temporary about.html file" (most recent)
   - "add about.html page"
   - "add index.html file"
   - "Initial commit"

**The cleanup commit should be the most recent.**

---

## Step 7: Delete the Feature Branch

### 7.1: Understand Branch Cleanup

**Why delete the branch?**
- The work has been merged into `main`
- The branch is no longer needed
- Keeps the repository clean and professional

### 7.2: Delete the Feature Branch

1. Make sure you're on `main` (verify with `git status`)
2. In the terminal, type exactly:
   ```bash
   git branch -d feature-about
   ```
3. Press **Enter**

**Expected Output:**
```
Deleted branch feature-about (was ghi7890).
```

**The branch is deleted locally.**

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

**Only `main` should remain.**

---

## Step 8: Final Verification

### 8.1: View Final Commit History

1. In the terminal, type exactly:
   ```bash
   git log --oneline
   ```
2. Press **Enter**

**Expected Output:**
```
jkl0123 (HEAD -> main, origin/main) remove temporary about.html file
ghi7890 add about.html page
def5678 add index.html file
abc1234 Initial commit
```

**You should see:**
- ✅ All commits in order
- ✅ `(HEAD -> main, origin/main)` showing local and remote are synchronized

### 8.2: Verify Final File Structure

1. In the terminal, type exactly:
   ```bash
   ls
   ```
2. Press **Enter**

**Expected Output:**
```
index.html  README.md
```

**Only two files should remain.**

### 8.3: Verify Repository Status

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

**Everything should be clean and synchronized.**

---

## Expected Final State

After completing this exercise, you should have:

- ✅ Only `main` branch exists (feature branch deleted)
- ✅ Only two files: `README.md` and `index.html`
- ✅ All commits pushed to GitHub
- ✅ Local and remote repositories synchronized
- ✅ Clean, professional repository ready for portfolio

**This is the final state for Section 2.**

---

## Troubleshooting

### Problem: "error: The branch 'feature-about' is not fully merged"

**Solution:**
- This means the branch has commits not in `main`
- Use `git branch -D feature-about` (capital D) to force delete
- Or verify the merge completed successfully first

### Problem: Merge conflicts

**Solution:**
- In this exercise, conflicts shouldn't occur
- If they do, it means `main` was modified after creating the branch
- Complete the merge by resolving conflicts, then continue

### Problem: Can't push to GitHub

**Solution:**
- Verify authentication: `gh auth status`
- Check internet connection
- Verify remote exists: `git remote -v`
- Try pushing again: `git push`

---

## Navigation

**Previous Exercise:** [[s2-vers-ctrl/s2e6-creating-pull-requests|Exercise 6: Creating Pull Requests]]

**Next Exercise:** [[s2-vers-ctrl/s2e8-recap-and-workflow-habits|Exercise 8: Recap and Workflow Habits]]

**Home:** [[r61-fsd-university/content/c01-found/s2-vers-ctrl/index|Main Course Page]]

**Return to Section:** [[s2-vers-ctrl/index|Version Control Section]]
