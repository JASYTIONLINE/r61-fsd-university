---
title: "C1S3E1: Creating Your First Webpage"
description: Create your first HTML webpage with proper document structure, title, headings, and paragraphs. Set up Live Server and preview your page in a browser.
tags:
  - html
  - css
  - vs-code
  - live-server
  - beginner
  - workbook
draft: false
date: 2026-01-30
---
# Getting Started:
Exercise 1: Creating Your First Webpage

**This exercise continues from Section 2. You must complete Section 2 first. Follow each step exactly.**

**Time Required:** 20-25 minutes

---

## Prerequisites Check

Before starting, verify:

1. ✅ **Section 2: Version Control Foundations completed**
   - You have a repository (containing: .git file) in your `knowledge-base/projects/` folder
   - Repository is open in VS Code
   - You're in the repository folder (i.e. ) in terminal
   ![[vsc-op-folder.png]]
(Note: Open the knowledge base folder in VS Code and navigate to Projects in vs Code)
![[vsc-openindex.png]]

- Repository should have `README.md` and `index.html` files

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
**If not, complete Section 2 first or resolve any uncommitted changes.**

---

## What You Will Accomplish

By the end of this exercise, you will have:

- Created a properly structured HTML document
- Added a page title and meta tags (including viewport for responsive design)
- Added headings and paragraphs to your page
- Set up Live Server extension in VS Code
- Previewed your page in a browser
- Committed your work with Git

---

## Step 1: Open index.html and Understand What You're Editing

### What This Step Does

`index.html` is the default homepage filename used by many web servers. When you open it in a browser, it becomes the first page a user sees. This file already exists in your repository from Section 2, and you're about to replace it with a properly structured HTML document.

### Instructions

1. In VS Code, look at the file explorer sidebar (left side)
2. Click on `index.html` to open it in the editor![[vsc-openindex.png]]

3. If the file already has content from Section 2, that's fine. You're about to replace it with a cleaner, properly structured HTML template.

---

## Step 2: Replace the File with Basic HTML Template

### What This Step Does

This creates the foundation of every HTML document. The structure you're creating tells the browser how to interpret and display your content. Every HTML document needs this basic structure to work properly.

### Instructions

1. In the `index.html` file (now open in the editor), select all the text (Ctrl + A)
2. Delete the selected text (Delete key)
3. Type or paste this exact code:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Webpage</title>
  </head>
  <body>
    <h1>Welcome to My First Webpage</h1>
    <p>This is my first paragraph. I'm learning HTML!</p>
    <p>This is my second paragraph. HTML is the structure of web pages.</p>
  </body>
</html>
```

4. Press **Ctrl + S** to save the file

### What to Notice

- **`<!DOCTYPE html>`** - This tells the browser to use modern HTML5 rules. It must be the very first line.
- **`<html lang="en">`** - This is the root element that wraps everything. The `lang="en"` attribute tells browsers and screen readers the page is in English.
- **`<head>`** - This section contains page settings and metadata. Nothing in `<head>` is visible to users, but it's important for browsers and search engines.
- **`<meta charset="UTF-8">`** - This tells the browser what character encoding to use. UTF-8 supports all characters and is the standard.
- **`<meta name="viewport" content="width=device-width, initial-scale=1.0">`** - This is essential for responsive design. It tells mobile browsers to use the device width instead of a desktop width, making your page work on phones and tablets.
- **`<title>`** - This appears in the browser tab. It's also what search engines use as the page title.
- **`<body>`** - This contains all the visible content that users see on the page.
- **`<h1>`** - This is a heading. Headings create hierarchy in your document. `<h1>` is the most important heading (largest).
- **`<p>`** - This is a paragraph. Paragraphs are for body text and automatically create spacing between blocks of text.

---

## Step 3: Verify File Was Saved

### What This Step Does

It's important to verify that your file was actually saved before moving forward. Sometimes files don't save automatically, and you want to catch that before trying to preview or commit.

### Visual Check

Look at the file tab in VS Code at the top of the editor:
- If you see a **white dot** next to `index.html`, the file is not saved yet
- Press **Ctrl + S** to save if you see the dot
- The dot should disappear when the file is saved
![[vsc-saved.png]]
### Git Check

1. In the VS Code terminal (Ctrl + ~), type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" or "git commit -a")
```

**If you see `index.html` listed under "Changes not staged for commit", your file was saved and Git detected the change. Proceed to Step 4.**

**If you don't see `index.html` listed:**
- Make sure you saved the file (Ctrl + S)
- Make sure you're in the repository folder in the terminal
- Check that you actually modified the file

---

## Step 4: Install Live Server Extension (One-Time Setup)

### What This Step Does

Live Server is a VS Code extension that creates a local web server for your HTML files. This allows you to preview your pages in a browser and see changes instantly when you save. This is much better than just opening the HTML file directly because it simulates how a real website works.

**Note:** You only need to install Live Server once. After this, you'll just use it.

### Instructions

1. In VS Code, click the **Extensions** icon in the left sidebar (or press Ctrl + Shift + X)![[vsc-ext.png]]
2. In the search box at the top, type: `live server`
3. Look for the extension named **Live Server** (published by Ritwick Dey)
4. Click the **Install** button (trust publisher)
5. Wait for installation to complete (may take 10-30 seconds)

### Verify Installation

After installation:
- VS Code may ask you to reload. If it does, click **Reload**
- The Extensions icon should show Live Server as installed
- You should see a "Go Live" button appear in the bottom-right corner of VS Code
![[vsc-golive.png]]
**If Live Server is installed, proceed to Step 5.**

---

## Step 5: Preview Your Page in the Browser

### What This Step Does

Previewing your page lets you see how it looks in a real browser. This is how you'll verify that your HTML is working correctly and see what users will see.

### Instructions

1. In VS Code file explorer (left sidebar), find `index.html`
2. **Right-click** on `index.html`
3. In the context menu, click **Open with Live Server**

**Expected Result:** Your default web browser should open automatically and display your page. You should see:
- "Welcome to My First Webpage" as a large heading
- Two paragraphs of text below it
- The browser tab should show "My First Webpage" (from the `<title>` tag)

### Verify What You See

You should see in the browser:
- ✅ A large heading: "Welcome to My First Webpage"
- ✅ First paragraph: "This is my first paragraph. I'm learning HTML!"
- ✅ Second paragraph: "This is my second paragraph. HTML is the structure of web pages."

**If you see your content correctly, proceed to Step 6.**

**If you don't see your content:**
- Make sure you saved the file (Ctrl + S)
- Make sure you opened it with Live Server (not by double-clicking the file in Windows File Explorer)
- Check that the browser tab shows "My First Webpage" - if it shows "file://" in the address bar, you didn't use Live Server
- Try closing the browser tab and opening with Live Server again
![[live-rightpng.png]]--

## Step 6: Commit Your Work

### What This Step Does

Committing your work saves this version of your file to Git history. This creates a snapshot you can return to later. Following the professional habits from Section 2, you'll check the status before committing to make sure everything is correct.

### Safety Check Before Committing

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" or "git commit -a")
```

**Verify:**
- ✅ You are on `main` branch
- ✅ Only `index.html` is modified
- ✅ No unexpected files are listed

**If everything looks correct, proceed to staging.**
**If you see unexpected files or are on a different branch, review your work before committing.**

### Stage the File

1. In the terminal, type exactly:
   ```bash
   git add index.html
   ```
2. Press **Enter**

**Expected Result:** No error message, prompt returns.

### Verify File is Staged

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
        modified:   index.html
```

**If you see `index.html` under "Changes to be committed", proceed to commit.**
**If not, repeat the `git add` command and check for typos.**

### Create the Commit

1. In the terminal, type exactly:
   ```bash
   git commit -m "s3: create first webpage with HTML structure"
   ```
2. Press **Enter**

**Expected Output:**
```
[main abc1234] s3: create first webpage with HTML structure
 1 file changed, 12 insertions(+), X deletions(-)
```

**The commit hash (abc1234) will be different - that's normal.**

### Verify Commit Success

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

**If you see this, your commit was successful. Proceed to final verification.**

---
## Expected Final State

After completing this exercise, you should have:

- ✅ `index.html` file with proper HTML structure
- ✅ Page title and viewport meta tag included
- ✅ Headings and paragraphs visible in the browser
- ✅ Live Server extension installed
- ✅ File committed to Git
- ✅ Working tree clean

### Final Verification

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 1 commit.

nothing to commit, working tree clean
```

**If you see "working tree clean", you're ready for the next exercise.**

---
## What This Sets Up for Exercise 2

You now have a properly structured HTML page that loads reliably in a browser. In the next exercise, you'll add more content elements like hyperlinks, lists, and images to make your page more interesting and functional.

---
#### Next Steps: [Return to the HTML-CSS Lecture](c01-found/c1s3-html-css/index#2.-HTML-Content-Elements)
2. HTML Content Elements

---
## Troubleshooting:
Things not working? Check out these common mistakes.
### Problem: "fatal: not a git repository"

**Solution:**
- You're not in the repository folder
- Run `pwd` to check your location
- Navigate to your repository folder: `cd path/to/your/repository`
### Problem: Live Server doesn't open browser

**Solution:**
- Make sure Live Server is installed (check Extensions)
- Try clicking the "Go Live" button in the bottom-right corner of VS Code
- Make sure you right-clicked on `index.html` and selected "Open with Live Server"
### Problem: Browser shows blank page or file:// in address bar

**Solution:**
- You didn't use Live Server - you opened the file directly
- Close the browser tab
- Right-click `index.html` in VS Code and select "Open with Live Server"
- The address bar should show `http://127.0.0.1:5500` or similar, not `file://`
### Problem: Changes don't appear in browser

**Solution:**
- Make sure you saved the file (Ctrl + S)
- Live Server should auto-refresh, but you can manually refresh the browser (F5)
- Check that you're editing the correct file

---
## Navigation
[Back to the Top](#Getting%20Started)
### Section 0 Map
- [C1S3E1:](c01-found/c1s3-html-css/s3e1-first-page) Exercise 1: Creating Your First Webpage
- [C1S3E2:](c01-found/c1s3-html-css/s3e2-elements) Exercise 2: Adding Rich Content Elements
- [C1S3E3:](c01-found/c1s3-html-css/s3e3-tables) Exercise 3: Creating Tables
- [C1S3E4:](c01-found/c1s3-html-css/s3e4-forms) Exercise 4: Creating Forms
- [C1S3E5:](c01-found/c1s3-html-css/s3e5-semantic) Exercise 5: Using Semantic HTML Structure
- [C1S3E6:](c01-found/c1s3-html-css/s3e6-css-intro) Exercise 6: Introduction to CSS
- [C1S3E7:](c01-found/c1s3-html-css/s3e7-css-selectors) Exercise 7: CSS Selectors
- [C1S3E8:](c01-found/c1s3-html-css/s3e8-css-styling) Exercise 8: CSS Styling Fundamentals
- [C1S3E9:](c01-found/c1s3-html-css/s3e9-css-layout) Exercise 9: CSS Layout with Float
- [C1S3E10:](c01-found/c1s3-html-css/s3e10-capstone) Exercise 10: Capstone Project - Client Meeting Scheduler

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