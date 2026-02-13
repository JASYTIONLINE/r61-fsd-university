---
title: "C1S2E2: Creating Your First Repository"
description: Create a GitHub repository and clone it to your knowledge-base/projects/ folder to begin version control work.
tags:
  - git
  - github
  - repository
  - beginner
  - workbook
draft: false
date: 2026-01-30
---
# Exercise 2: Creating Repository
**Time Required:** 15-20 minutes

---
## Getting Started
### Prerequisites Check
Before starting, verify you have completed:
1. ✅ **Exercise 1: Authenticating Git with GitHub**
   - GitHub CLI installed
   - Git configured with your name and email
   - Git authenticated with GitHub
   - VS Code terminal configured to use Git Bash

2. ✅ **Section 1: File Systems**
   - Knowledge base folder structure created
   - You know the exact path to your `knowledge-base/projects/` folder
   - Example: `C:\Users\YourName\knowledge-base\projects\`

3. ✅ **Current Requirements**
   - VS Code installed (closed-we'll open it during this exercise)
   - Working internet connection
   - Web browser open

**If any prerequisite is missing, complete it before proceeding.**

### What You Will Accomplish
By the end of this exercise, you will have:
- A GitHub repository created on GitHub.com
- The repository cloned to your `knowledge-base/projects/` folder
- The repository open in VS Code
- A [README.md](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes) file in the repository
- [Local](https://docs.github.com/en/desktop/adding-and-cloning-repositories/adding-a-repository-from-your-local-computer-to-github-desktop) and [remote](https://docs.github.com/en/get-started/git-basics/about-remote-repositories) repositories connected

---
## Step 1: Create Repository on GitHub

### 1.1: Navigate to GitHub
1. Open your web browser
2. Navigate to:  [GithHub](https://github.com/login)
3. If not already logged in, click **Sign in** and enter your credentials
4. You will need to setup [2-factor authentication](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa/about-two-factor-authentication)
5. After logging in, you should see your GitHub dashboard

### 1.2: Start Repository Creation
1. In the top right corner of GitHub, locate the **+** icon (plus sign)
2. Click the **+** icon
3. A dropdown menu appears
4. Click **New repository**
![[ss-new-repo.png]]
**Expected Result:** You are taken to the "Create a new repository" page.

### 1.3: Configure Repository Settings
Fill out the form exactly as follows:
1. **Repository name:**
   - Type: `version-control-portfolio`
   - Use all lowercase letters
   - Use hyphens instead of spaces
   - **Do not** use underscores or special characters

2. **Description (optional):**
   - Leave blank or type: `My version control learning portfolio`

3. **Visibility:**
   - Select **Public** (radio button)

4. **Initialize this repository with:**
   - ✅ Check the box: **Add a README file**
   - ❌ Leave unchecked: **Add .gitignore**
   - ❌ Leave unchecked: **Choose a license**

5. **Do not change any other settings**
![[ss-create-repo.png]]
### 1.4: Create the Repository
1. Scroll down to the bottom of the page
2. Click the green button: **Create repository**

**Expected Result:** You are taken to your new repository page on GitHub.

### 1.5: Verify Repository Creation
On the repository page, verify you see:
- ✅ Repository name: `version-control-portfolio` (or your username/version-control-portfolio)
- ✅ One file listed: `README.md`
- ✅ Text showing "1 commit" or similar
- ✅ A green **Code** button visible

**If you see all of these, proceed to Step 2.**
**If anything is missing, go back and check Step 1.3.**
![[ss-verify.png]]
---
## Step 2: Get Repository URL

### 2.1: Copy Repository URL
1. On your GitHub repository page, locate the green **Code** button
2. Click the **Code** button
3. A dropdown menu appears
4. Make sure [HTTPS](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa/about-two-factor-authentication) is selected (it should be by default)
5. Click the **copy icon** (two overlapping squares) next to the URL

**Expected Result:** The URL is copied to your clipboard. It should look like: 
```
https://github.com/your-username/version-control-portfolio.git
```

**Important:** Keep this URL copied. You'll need it in Step 3.
![[ss-copy.png]]
---

## Step 3: Navigate to Your Projects Folder

### 3.1: Open VS Code
- Choose the file drop down and choose e Open Folder
- Navigate to your projects folder
- Open the folder in VS Code

![[ss-open-local.png]]

### 3.2: Open VS Code Terminal
![[ss-vs-term.png]]
1. In VS Code, press **Ctrl + ~** (Control key + tilde key)
   - This opens the integrated terminal at the bottom
2. Verify the terminal prompt ends with `$` (Git Bash)

**If you see `$`, proceed.**
**If you see `>` or `PS`, you need to configure VS Code terminal [[#Step 5 Open Repository in VS Code|see Section 2 Exercise 1, Step 5.]]

### 3.3: OPEN Projects Folder
1. In the VS Code terminal, type your path (replace with your actual path):
   ```bash
   cd /c/Users/YourName/knowledge-base/projects
   ```
   **Important:** 
   - Replace `YourName` with your Windows username
   - Use forward slashes `/` not backslashes `\`
   - Use `/c/` instead of `C:\`
   - The path is case-sensitive

2. Press **Enter**

**Expected Output:**
```
username@computername MINGW64 /c/Users/YourName/knowledge-base/projects
```

**If you see your path in the prompt, you're in the right location.**
**If you get an error, check:**
- Your username is correct
- The folder path exists (create it if needed)
- You're using forward slashes and `/c/` format

### 3.4: Verify You're in the Right Location
1. In the terminal, type exactly:
   ```bash
   pwd
   ```
2. Press **Enter**

**Expected Output:**
```
/c/Users/YourName/knowledge-base/projects
```

**If the path matches your knowledge-base/projects folder, proceed to Step 4.**
**If not, repeat Step 3.3 with the correct path.**

---
## Step 4: Clone the Repository
### 4.1: Clone Using Git
1. In the VS Code terminal (still in your projects folder), type exactly:
   ```bash
   git clone https://github.com/your-username/version-control-portfolio.git
   ```
   **Important:** Replace `your-username` with your actual GitHub username.

2. Press **Enter**

**Expected Output:**
```
Cloning into 'version-control-portfolio'...
remote: Enumerating objects: X, done.
remote: Counting objects: 100% (X/X), done.
remote: Compressing objects: 100% (X/X), done.
remote: Total X (delta X), reused X (delta X), pack-reused 0 (from 0)
Receiving objects: 100% (X/X), done.
Resolving deltas: 100% (X/X), done.
```

**If you see "Cloning into..." and no errors, proceed to Step 4.2.**
**If you see an authentication error, you need to complete Exercise 1 first.**

### 4.2: Verify Clone Success
1. In the terminal, type exactly:
   ```bash
   ls
   ```
2. Press **Enter**

**Expected Output:**
```
version-control-portfolio
```

**If you see the folder name, the clone was successful.**
**If you don't see it, check for error messages in Step 4.1.**

---

## Step 5: Open Repository in VS Code

### 5.1: Navigate into Repository Folder
1. In the terminal, type exactly:
   ```bash
   cd version-control-portfolio
   ```
2. Press **Enter**

**Expected Result:** The prompt should now show the repository path.

### 5.2: Open Folder in VS Code
1. In VS Code, click **File** in the menu bar
2. Click **Open Folder...**
3. Navigate to: `C:\Users\YourName\knowledge-base\projects\version-control-portfolio`
   - Use Windows File Explorer format (backslashes, `C:\`)
4. Click **Select Folder** (or **OK**)

**Expected Result:** VS Code opens the repository folder. You should see:
- A file explorer sidebar on the left
- `README.md` file listed
- The terminal still open at the bottom

### 5.3: Verify Git Repository Status
1. In the VS Code terminal (still open), type exactly:
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

**If you see "On branch main" and "working tree clean", proceed to Step 6.**
**If you see an error, make sure you're in the repository folder (Step 5.1).**

---

## Step 6: Verify Repository Structure
### 6.1: List Files

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
```

**You should see:**
- ✅ `.git` folder (hidden, starts with a dot)
- ✅ `README.md` file

### 6.2: Verify Remote Connection
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

**If you see both fetch and push URLs pointing to your GitHub repository, proceed to Step 7.**
**If not, the clone may have failed. Repeat Step 4.**

---
## Step 7: Verify Connection to GitHub

### 7.1: Check Branch Information
1. In the terminal, type exactly:
   ```bash
   git branch -a
   ```
2. Press **Enter**

**Expected Output:**
```
* main
  remotes/origin/main
```

**The asterisk (*) shows you're on the `main` branch.**
**`remotes/origin/main` shows the remote branch exists.**

### 7.2: View Commit History
1. In the terminal, type exactly:
   ```bash
   git log --oneline
   ```
2. Press **Enter**

**Expected Output:**
```
[commit-hash] Initial commit
```

**You should see at least one commit (the initial commit from GitHub).**

---
## Expected Final State

After completing this exercise, you should have:

- ✅ A GitHub repository named `version-control-portfolio`
- ✅ The repository cloned to `knowledge-base/projects/version-control-portfolio/`
- ✅ The repository open in VS Code
- ✅ One file: `README.md`
- ✅ Local repository connected to GitHub (remote: origin)
- ✅ Working tree clean, on branch `main`

---
#### Next Steps: - Return to the [Version Control Lecture](c01-found/c1s2-vers-ctrl/index#3.-Pushing-Changes-to-Your-Remote)
3. Pushing Changes to Your Remote

---
## Troubleshooting

### Problem: "fatal: could not read Username"

**Solution:**
- You need to complete Exercise 1 first (GitHub CLI authentication)
- Run `gh auth status` to verify authentication
- If not authenticated, run `gh auth login` again
### Problem: "fatal: destination path already exists"

**Solution:**
- The folder already exists
- Either delete the existing folder, or
- Use a different repository name in Step 1.3
### Problem: Can't find knowledge-base/projects folder

**Solution:**
- Complete Section 1, Exercise 2 first
- Or create the folder manually:
  ```bash
  mkdir -p /c/Users/YourName/knowledge-base/projects
  ```
### Problem: VS Code doesn't show files

**Solution:**
- Make sure you opened the correct folder (Step 5.2)
- Check that you're in the repository folder in terminal (`pwd`)
- Try closing and reopening VS Code

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
- [Course 03:](c03-fe-react/index.md) Designing a Dynamic Frontend with React
- [Course 04:](c04-genai-design/index.md) Harnessing Gen AI: From Design to Code Optimization
- [Course 05:](c05-data/index) Understanding Data Structures and Algorithms
- [Course 06:](c06-mongol/index) Using MongoDB to Design and Manage Databases
- [Course 07:](c07-express/index) Developing a Reliable Back-end with Node and Express
- [Course:08](c08-ai-test/index) The Power of Generative AI Software Testing
- [Course 09:](c09-publish/index) Publishing your Website to the Live Internet
