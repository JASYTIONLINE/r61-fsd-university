---
title: "Exercise 1: Authenticating Git with GitHub"
description: "Install GitHub CLI, configure Git identity, authenticate with GitHub, and configure VS Code terminal for version control."
tags: [git, github, authentication, setup, beginner, workbook]
draft: false
date: "2026-01-30"
---

# Exercise 1: Authenticating Git with GitHub

**This exercise is a standalone technical manual. Follow each step exactly. No prior knowledge of Git commands is required.**

**Time Required:** 20-30 minutes

---

## Prerequisites Check

Before starting, verify you have completed:

1. ✅ **Section 0 (Orientation)**
   - Exercise 2: Git Bash installed
   - Exercise 3: VS Code installed
   - Exercise 4: GitHub account created

2. ✅ **Section 1 (File Systems)**
   - Exercise 2: Knowledge base folder structure created
   - You know the location of your `knowledge-base/projects/` folder

3. ✅ **Current Requirements**
   - Windows computer with administrator access
   - Working internet connection
   - GitHub account username and password
   - VS Code closed (we'll open it during this exercise)

**If any prerequisite is missing, complete it before proceeding.**

---

## What You Will Accomplish

By the end of this exercise, you will have:

- GitHub CLI (`gh`) installed on your computer
- Git configured with your name and email
- Git authenticated with GitHub using GitHub CLI
- VS Code terminal configured to use Git Bash
- Verified that authentication works

---

## Step 1: Install GitHub CLI

### 1.1: Download GitHub CLI

1. Open your web browser
2. Navigate to: `https://cli.github.com/`
3. Click the **Download for Windows** button
4. The download should start automatically
5. Wait for the download to complete

**Expected Result:** A file named `gh_x.x.x_windows_amd64.msi` appears in your Downloads folder (version numbers will vary).

### 1.2: Install GitHub CLI

1. Open your Downloads folder
2. Double-click the `gh_x.x.x_windows_amd64.msi` file
3. If Windows asks for permission, click **Yes**
4. The installation wizard opens
5. Click **Next** on the welcome screen
6. Accept the license agreement (check the box, then click **Next**)
7. Choose installation location (default is fine, click **Next**)
8. Click **Install**
9. Wait for installation to complete (may take 1-2 minutes)
10. Click **Finish**

### 1.3: Verify GitHub CLI Installation

1. Press the **Windows key**
2. Type: `git bash`
3. Press **Enter** (Git Bash opens)
4. In Git Bash, type exactly:
   ```bash
   gh --version
   ```
5. Press **Enter**

**Expected Output:**
```
gh version x.x.x (xxxx-xx-xx)
```

**If you see a version number, GitHub CLI is installed correctly.**
**If you see "command not found", restart your computer and try again.**

---

## Step 2: Configure Git with Your Identity

### 2.1: Open Git Bash

1. Press the **Windows key**
2. Type: `git bash`
3. Press **Enter**

**You should see a terminal window with a prompt ending in `$`**

### 2.2: Set Your Git Name

1. In Git Bash, type exactly (replace "Your Name" with your actual name):
   ```bash
   git config --global user.name "Your Name"
   ```
2. Press **Enter**
3. **Expected Result:** No error message, prompt returns

**Important:** Use your real name or professional name. This name will appear on all your commits.

### 2.3: Set Your Git Email

1. In Git Bash, type exactly (replace the email with the email address associated with your GitHub account):
   ```bash
   git config --global user.email "your.email@example.com"
   ```
2. Press **Enter**
3. **Expected Result:** No error message, prompt returns

**Important:** Use the same email address you used to create your GitHub account.

### 2.4: Verify Git Configuration

1. In Git Bash, type exactly:
   ```bash
   git config --global --list
   ```
2. Press **Enter**

**Expected Output:**
```
user.name=Your Name
user.email=your.email@example.com
[additional configuration lines]
```

**Verify:**
- ✅ Your name appears after `user.name=`
- ✅ Your email appears after `user.email=`

**If your name and email are correct, proceed to Step 3.**
**If they are incorrect, repeat Steps 2.2 and 2.3 with the correct information.**

---

## Step 3: Authenticate with GitHub Using GitHub CLI

### 3.1: Start Authentication

1. In Git Bash (still open from Step 2), type exactly:
   ```bash
   gh auth login
   ```
2. Press **Enter**

**Expected Output:**
```
? What account do you want to log into? GitHub.com
```

### 3.2: Select GitHub.com

1. The prompt shows: `? What account do you want to log into?`
2. Press **Enter** (GitHub.com is the default)

**Expected Output:**
```
? What is your preferred protocol for Git operations? HTTPS
```

### 3.3: Select HTTPS Protocol

1. The prompt shows: `? What is your preferred protocol for Git operations?`
2. Press **Enter** (HTTPS is the default)

**Expected Output:**
```
? Authenticate Git with your GitHub credentials? Yes
```

### 3.4: Enable Git Credential Helper

1. The prompt shows: `? Authenticate Git with your GitHub credentials?`
2. Press **Enter** (Yes is the default)

**Expected Output:**
```
? How would you like to authenticate GitHub CLI? Login with a web browser
```

### 3.5: Choose Web Browser Authentication

1. The prompt shows: `? How would you like to authenticate GitHub CLI?`
2. Press **Enter** (Login with a web browser is the default)

**Expected Output:**
```
! First copy your one-time code: XXXX-XXXX
Press Enter to open github.com in your browser...
```

### 3.6: Copy One-Time Code

1. **Copy the one-time code** shown (format: XXXX-XXXX)
   - Click and drag to select the code
   - Press **Ctrl + C** to copy
2. Press **Enter** in Git Bash

**Expected Result:** Your web browser opens to GitHub's device authorization page.

### 3.7: Authorize on GitHub Website

1. In your web browser, you should see a GitHub page asking you to authorize GitHub CLI
2. Paste the one-time code you copied (Ctrl + V) into the code field
3. Click **Continue**
4. If prompted to sign in, enter your GitHub username and password
5. Click **Authorize github** (or similar button)
6. You should see a success message: "You have successfully authorized GitHub CLI"

### 3.8: Return to Git Bash

1. Return to the Git Bash window
2. You should see:
   ```
   ✓ Authentication complete.
   ✓ Logged in as [your-username]
   ```

**If you see "Authentication complete" and your username, proceed to Step 4.**
**If you see an error, repeat Step 3 from the beginning.**

---

## Step 4: Verify Authentication

### 4.1: Test GitHub CLI Authentication

1. In Git Bash, type exactly:
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

**If you see all three checkmarks, authentication is successful.**

### 4.2: Test Git Authentication

1. In Git Bash, type exactly:
   ```bash
   git config --global credential.helper
   ```
2. Press **Enter**

**Expected Output:**
```
!gh auth git-credential
```

**If you see this output, Git is configured to use GitHub CLI for authentication.**

---

## Step 5: Configure VS Code Terminal to Use Git Bash

### 5.1: Open VS Code

1. Press the **Windows key**
2. Type: `visual studio code`
3. Press **Enter**

**VS Code opens.**

### 5.2: Open VS Code Settings

1. In VS Code, press **Ctrl + ,** (Control key + comma)
   - This opens Settings
2. In the search box at the top, type: `terminal integrated default profile windows`
3. Click on **Terminal > Integrated > Default Profile: Windows**

### 5.3: Set Git Bash as Default Terminal

1. Click the dropdown that says **PowerShell** (or **Command Prompt**)
2. Select **Git Bash** from the list
3. Close the Settings tab (click the X or press **Ctrl + ,** again)

### 5.4: Verify Terminal Configuration

1. In VS Code, press **Ctrl + ~** (Control key + tilde key)
   - This opens the integrated terminal
2. Look at the terminal prompt

**Expected Result:**
- The prompt should end with `$` (not `>` or `PS`)
- The prompt should show something like: `username@computername MINGW64 ~ $`

**If you see a `$` prompt, VS Code terminal is configured correctly.**
**If you see `>` or `PS`, repeat Step 5.3.**

### 5.5: Test Git in VS Code Terminal

1. In the VS Code terminal (still open), type exactly:
   ```bash
   git --version
   ```
2. Press **Enter**

**Expected Output:**
```
git version x.x.x
```

**If you see a version number, Git works in VS Code terminal.**

3. Type exactly:
   ```bash
   gh --version
   ```
4. Press **Enter**

**Expected Output:**
```
gh version x.x.x (xxxx-xx-xx)
```

**If you see a version number, GitHub CLI works in VS Code terminal.**

---

## Step 6: Final Verification

### 6.1: Verify All Components

In the VS Code terminal, run these commands one at a time and verify each output:

1. **Check Git identity:**
   ```bash
   git config --global user.name
   ```
   **Expected:** Your name

2. **Check Git email:**
   ```bash
   git config --global user.email
   ```
   **Expected:** Your email

3. **Check GitHub CLI authentication:**
   ```bash
   gh auth status
   ```
   **Expected:** Three checkmarks showing you're logged in

4. **Check terminal type:**
   ```bash
   echo $SHELL
   ```
   **Expected:** Path containing `bash` or `git-bash`

**If all four checks pass, you have successfully completed Exercise 1.**

---

## Expected Final State

After completing this exercise, you should have:

- ✅ GitHub CLI installed and working
- ✅ Git configured with your name and email
- ✅ Git authenticated with GitHub via GitHub CLI
- ✅ VS Code terminal configured to use Git Bash
- ✅ All commands working in VS Code terminal

---

## Troubleshooting

### Problem: "gh: command not found" after installation

**Solution:**
1. Close all terminal windows
2. Restart your computer
3. Open Git Bash again
4. Try `gh --version` again

### Problem: Authentication fails during `gh auth login`

**Solution:**
1. Make sure you're using the correct GitHub username and password
2. Make sure you copy the one-time code exactly (including dashes)
3. Make sure you paste it into the GitHub website (not back into Git Bash)
4. Try the authentication process again from Step 3.1

### Problem: VS Code terminal still shows PowerShell

**Solution:**
1. Close VS Code completely
2. Reopen VS Code
3. Open terminal (Ctrl + ~)
4. If still PowerShell, repeat Step 5.3 and restart VS Code again

### Problem: Git config shows wrong name or email

**Solution:**
1. Run the `git config --global user.name` and `user.email` commands again with correct values
2. Verify with `git config --global --list`

---

## Next Steps

- [[c01-found/s2-vers-ctrl/index#Authentication: Connecting Git to GitHub|Return to Lecture]] - Review the authentication concepts in the lecture before continuing.

---

## Navigation

**Next Exercise:** [[s2-vers-ctrl/s2e2-creating-repository|Exercise 2: Creating Repository]]

**Home:** [[index|Main Course Page]]

**Return to Section:** [[s2-vers-ctrl/index|Version Control Section]]
