---
title: "Exercise 8: Recap and Workflow Habits"
description: "Recap that ties together all exercises, reinforces good habits, and prepares for HTML and CSS."
tags: [git, github, recap, habits, beginner, workbook]
draft: false
date: "2026-01-30"
---

# Exercise 8: Recap and Workflow Habits

**This exercise is a recap and reflection. No new commands are introduced.**

**This exercise is a standalone technical manual. Follow each step exactly.**

**Time Required:** 15-20 minutes

---

## Prerequisites Check

Before starting, verify:

1. ✅ **Exercises 1-7 completed**
   - Repository `version-control-portfolio` exists
   - Repository is open in VS Code
   - You're in the repository folder in terminal
   - Only `main` branch exists
   - Only `README.md` and `index.html` files exist
   - All commits pushed to GitHub

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
**If not, complete Exercise 7 first.**

---

## What You Will Accomplish

By the end of this exercise, you will have:

- Reviewed all concepts learned in Exercises 1-6
- Understood the "why" behind each action
- Reinforced professional workflow habits
- Verified your repository is portfolio-ready
- Prepared for the next section (HTML & CSS)

---

## Step 1: Verify Your Repository State

### 1.1: Check Branch Structure

1. In the VS Code terminal, type exactly:
   ```bash
   git branch -a
   ```
2. Press **Enter**

**Expected Output:**
```
* main
  remotes/origin/main
```

**You should see:**
- ✅ Only `main` branch locally
- ✅ `remotes/origin/main` showing the remote branch
- ✅ No feature branches remaining

### 1.2: Check File Structure

1. In the terminal, type exactly:
   ```bash
   ls -la
   ```
2. Press **Enter**

**Expected Output:**
```
total X
drwxr-xr-x 1 user user  X date .git
drwxr-xr-x 1 user user  X date .
drwxr-xr-x 1 user user  X date ..
-rw-r--r-- 1 user user  X date README.md
-rw-r--r-- 1 user user  X date index.html
```

**You should see:**
- ✅ `.git` folder (hidden)
- ✅ `README.md` file
- ✅ `index.html` file
- ✅ No other files

### 1.3: Check Commit History

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
- ✅ All commits in chronological order
- ✅ `(HEAD -> main, origin/main)` showing synchronization
- ✅ Clear commit messages

### 1.4: Verify Remote Connection

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

**Both fetch and push URLs should point to your GitHub repository.**

---

## Step 2: Review Exercise 1 - Authentication

### 2.1: What You Did

1. Installed GitHub CLI (`gh`)
2. Configured Git with your name and email
3. Authenticated with GitHub using `gh auth login`
4. Configured VS Code terminal to use Git Bash

### 2.2: Why It Matters

**Authentication is the foundation:**
- Without it, you can't push code to GitHub
- GitHub CLI provides modern, secure authentication
- Git identity appears on every commit
- VS Code terminal integration makes workflow smooth

### 2.3: Verify Authentication Still Works

1. In the terminal, type exactly:
   ```bash
   gh auth status
   ```
2. Press **Enter**

**Expected Output:**
```
github.com
  ✓ Logged in to github.com as [your-username]
  ✓ Git operations for github.com configured to use HTTPS
  ✓ Credential helper is configured
```

**All three checkmarks confirm authentication is working.**

---

## Step 3: Review Exercise 2 - Repository Creation

### 3.1: What You Did

1. Created a GitHub repository
2. Cloned it to your `knowledge-base/projects/` folder
3. Opened it in VS Code
4. Connected local and remote repositories

### 3.2: Why It Matters

**Repository structure:**
- One repository per project (professional standard)
- Located in your knowledge base (organized)
- Local and remote stay synchronized
- Foundation for all future work

### 3.3: Verify Repository Location

1. In the terminal, type exactly:
   ```bash
   pwd
   ```
2. Press **Enter**

**Expected Output:**
```
/c/Users/YourName/knowledge-base/projects/version-control-portfolio
```

**This confirms your repository is in the correct location.**

---

## Step 4: Review Exercise 3 - Tracking and Committing

### 4.1: What You Did

1. Created `index.html` file
2. Staged it with `git add`
3. Committed it with `git commit`
4. Pushed it to GitHub with `git push`

### 4.2: Why It Matters

**The Git workflow:**
- **Untracked → Staged → Committed → Pushed**
- Each step has a purpose
- `git status` shows you where you are
- Commits are local until pushed

### 4.3: Key Concepts

1. **Staging:** Choosing what to commit
2. **Committing:** Saving a snapshot locally
3. **Pushing:** Sending commits to GitHub
4. **Status checking:** Always know your state

---

## Step 5: Review Exercise 4 - Branch Creation

### 5.1: What You Did

1. Created a branch
2. Switched between branches
3. Listed branches
4. Deleted a branch

### 5.2: Why It Matters

**Branching protects main:**
- `main` stays stable and working
- Feature branches isolate new work
- Safe to experiment
- Professional workflow standard

### 5.3: Key Concepts

1. **Branches are lightweight:** Don't copy files
2. **Switching is safe:** No data loss
3. **Isolation:** Changes don't affect other branches
4. **Cleanup:** Delete branches after merging

---

## Step 6: Review Exercise 5 - Branch Isolation

### 6.1: What You Did

1. Created a file on a branch
2. Committed it to the branch
3. Switched to `main` and saw the file disappear
4. Switched back and saw the file return

### 6.2: Why It Matters

**Branch isolation in action:**
- Files belong to branches
- Commits belong to branches
- Switching branches changes your view
- `main` stays untouched

### 6.3: Key Concepts

1. **Files are branch-specific:** Until merged
2. **Commits are branch-specific:** Until merged
3. **Visual confirmation:** Files appear/disappear
4. **Safety:** `main` protected from experiments

---

## Step 7: Review Exercise 6 - Pull Requests

### 7.1: What You Did

1. Forked a repository on GitHub
2. Cloned your fork locally
3. Added upstream remote
4. Created a branch for changes
5. Made changes and committed them
6. Pushed branch to your fork
7. Created a pull request

### 7.2: Why It Matters

**Collaboration workflow:**
- Forking enables contributing to others' projects
- Pull requests are the professional way to merge code
- Origin vs upstream understanding is essential
- This is how open-source and team projects work

### 7.3: Key Concepts

1. **Forking:** Creating your own copy of someone else's repository
2. **Origin vs Upstream:** Your fork vs the original repository
3. **Pull Requests:** Request to merge your changes into the original
4. **Collaboration:** Professional way to contribute code

---

## Step 8: Review Exercise 7 - Merging and Cleanup

### 8.1: What You Did

1. Merged feature branch into `main`
2. Removed temporary learning files
3. Pushed final state to GitHub
4. Deleted the feature branch

### 8.2: Why It Matters

**Professional workflow:**
- Merge when work is complete
- Clean up temporary files
- Keep repository professional
- Push final state to GitHub

### 8.3: Key Concepts

1. **Merging:** Combines branch work into `main`
2. **Cleanup:** Remove temporary files
3. **Pushing:** Share final state
4. **Branch deletion:** Keep repository clean

---

## Step 9: Professional Workflow Habits

### 9.1: The Habits You Practiced

Throughout all exercises, you repeatedly used:

1. **`git status`** - Check state before actions
2. **Clear commit messages** - Explain what changed
3. **Branch protection** - Never commit directly to `main` for new work
4. **Regular pushing** - Keep local and remote in sync
5. **Cleanup** - Remove temporary files and branches

### 9.2: Why These Habits Matter

**Professional development:**
- Prevents mistakes
- Makes collaboration easier
- Creates professional-looking repositories
- Builds skills employers expect

### 9.3: Practice These Habits

1. **Always check status:**
   ```bash
   git status
   ```
   Run this before risky operations.

2. **Commit often with clear messages:**
   ```bash
   git commit -m "descriptive message"
   ```
   Small, focused commits are better than large ones.

3. **Use branches for new work:**
   ```bash
   git branch feature-name
   git checkout feature-name
   ```
   Protect `main` by working on branches.

4. **Push regularly:**
   ```bash
   git push
   ```
   Keep your work backed up on GitHub.

5. **Clean up after yourself:**
   ```bash
   git branch -d feature-name
   ```
   Delete branches and remove temporary files.

---

## Step 10: Verify Portfolio Readiness

### 10.1: Check Repository on GitHub

1. Open your web browser
2. Navigate to: `https://github.com/your-username/version-control-portfolio`
3. Review the repository page

**Verify:**
- ✅ Repository is public (or private if you prefer)
- ✅ Only `README.md` and `index.html` files visible
- ✅ Commit history shows professional messages
- ✅ No temporary or test files
- ✅ Clean, organized appearance

### 10.2: Check Local Repository

1. In VS Code terminal, type exactly:
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

### 10.3: Final File Check

1. In VS Code, look at the file explorer
2. Verify you see only:
   - ✅ `README.md`
   - ✅ `index.html`

**No other files should be visible.**

---

## Step 11: Prepare for Next Section

### 11.1: What's Next?

**Section 3: HTML & CSS**
- You'll start writing real code
- You'll build web pages
- You'll use version control for every change
- Your repository will grow

### 11.2: How Version Control Helps

**As your project grows:**
- Mistakes become easier to make
- Changes become harder to track
- Recovery becomes more important

**Version control:**
- Lets you experiment safely
- Shows you what changed
- Lets you revert mistakes
- Keeps your work organized

### 11.3: Your Workflow Going Forward

**For every change:**
1. Check status: `git status`
2. Create a branch: `git branch feature-name`
3. Switch to branch: `git checkout feature-name`
4. Make changes
5. Stage changes: `git add .`
6. Commit changes: `git commit -m "message"`
7. Push to GitHub: `git push`
8. Merge to main when complete
9. Delete branch after merging

**This workflow will become second nature.**

---

## Expected Final State

After completing this exercise, you should have:

- ✅ Complete understanding of all concepts
- ✅ Professional workflow habits established
- ✅ Clean, portfolio-ready repository
- ✅ Ready to start building with HTML & CSS
- ✅ Confidence in using version control

---

## Summary: What You've Accomplished

**You started with:**
- No version control knowledge
- No repository
- No understanding of Git

**You now have:**
- ✅ Git and GitHub CLI installed and configured
- ✅ A professional repository structure
- ✅ Understanding of version control concepts
- ✅ Experience with Git commands
- ✅ Professional workflow habits
- ✅ A portfolio-ready repository

**This foundation will support all your development work.**

---

## Navigation

**Previous Exercise:** [[s2-vers-ctrl/s2e7-merging-branches|Exercise 7: Merging Branches]]

**Next Section:** [[s3-html-css/index|Section 3: HTML & CSS]]

**Home:** [[r61-fsd-university/content/c01-found/s2-vers-ctrl/index|Main Course Page]]

**Return to Section:** [[s2-vers-ctrl/index|Version Control Section]]
