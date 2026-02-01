---
title: "Exercise 10: Capstone Project - Client Meeting Scheduler"
description: "Build a complete Client Meeting Scheduler web application combining all HTML and CSS concepts. Create a portfolio-ready project with proper file organization and best practices."
tags: [html, css, capstone, project, portfolio, beginner, workbook]
draft: false
date: "2026-01-30"
---

# Exercise 10: Capstone Project - Client Meeting Scheduler

**This exercise continues from Exercise 9. You must complete Exercise 9 first.**

**This exercise is a standalone technical manual. Follow each step exactly.**

**Time Required:** 60-90 minutes

---

## Prerequisites Check

Before starting, verify:

1. ✅ **Exercise 9 completed**
   - Page has layout with float and responsive design
   - All changes from Exercise 9 are committed
   - You understand all HTML and CSS concepts covered so far

2. ✅ **Current State Verification**
   - Open VS Code terminal (Ctrl + ~)
   - Type: `git status`
   - Press Enter

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 9 commits.

nothing to commit, working tree clean
```

**If you see this, proceed.**
**If not, complete Exercise 9 first or resolve any uncommitted changes.**

---

## What You Will Accomplish

By the end of this exercise, you will have:

- Built a complete Client Meeting Scheduler web application
- Combined all HTML and CSS concepts you've learned
- Implemented proper file organization (css/, images/ folders)
- Used semantic HTML throughout
- Applied accessibility best practices
- Created responsive design
- Organized CSS with comments and sections
- Created a portfolio-ready project
- Committed your work with Git

---

## Step 1: Understand the Project Requirements

### What This Step Does

You're building a Client Meeting Scheduler - a web application that allows clients to schedule meetings. This project combines everything you've learned: HTML structure, forms, tables, CSS styling, layout, and responsive design. This will be a complete, professional project you can show to employers.

**Project requirements:**
- **Semantic HTML** - Use proper HTML5 semantic elements
- **Organized file structure** - CSS in `css/` folder, images in `images/` folder
- **Complete form** - Meeting scheduling form with all necessary fields
- **Table display** - Show scheduled meetings in a table
- **Responsive design** - Works on all screen sizes
- **Accessibility** - Proper labels, alt text, semantic elements
- **Professional CSS** - Organized with comments and sections
- **Clean code** - Well-commented, maintainable structure

**This is your portfolio piece:** This project demonstrates your ability to build a complete web application from scratch.

---

## Step 2: Set Up Project File Structure

### What This Step Does

Following file organization principles from Section 1, you'll create a proper folder structure for your project. This implements logical grouping (CSS files together, images together), scalable structure (easy to add more files), and self-explanatory organization.

**Why proper structure matters:**
- **Logical grouping** - Related files are together
- **Scalable** - Easy to add more files as project grows
- **Professional** - This is what employers expect
- **Maintainable** - Easy to find and update files

### Instructions

1. In VS Code file explorer, look at your repository root
2. **Right-click** in empty space
3. Click **New Folder**
4. Type exactly: `images`
5. Press **Enter**

**Expected Result:** A new folder named `images` appears in your file explorer.

**Note:** You already have a `css/` folder from Exercise 6. If you don't, create it now following the same steps.

### Verify Folder Structure

1. In the terminal, type exactly:
   ```bash
   ls
   ```
2. Press **Enter**

**Expected Output:**
```
css  images  index.html  README.md
```

**You should see:**
- ✅ `css/` folder (for CSS files)
- ✅ `images/` folder (for image files)
- ✅ `index.html` (your main HTML file)
- ✅ `README.md` (project documentation)

**If you see this structure, proceed to Step 3.**
**If folders are missing, create them now.**

### Verify with Git Status

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 9 commits.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        images/

nothing to commit, working tree clean
```

**You should see `images/` as an untracked directory. This is correct - you'll commit it after adding content.**

---

## Step 3: Create the HTML Structure

### What This Step Does

You'll create the complete HTML structure for the Client Meeting Scheduler. This includes a header with navigation, a main content area with a scheduling form and meetings table, and a footer. You'll use semantic HTML elements throughout.

### Instructions

1. Open `index.html` in VS Code
2. Replace the entire content with this complete structure:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Client Meeting Scheduler</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <header id="page-header">
      <h1>Client Meeting Scheduler</h1>
      <nav>
        <ul>
          <li><a href="#schedule" class="nav-link">Schedule Meeting</a></li>
          <li><a href="#meetings" class="nav-link">View Meetings</a></li>
          <li><a href="#about" class="nav-link">About</a></li>
        </ul>
      </nav>
    </header>

    <main id="main-content">
      <section id="schedule" class="content-section">
        <h2>Schedule a New Meeting</h2>
        <form id="meeting-form">
          <label for="client-name">Client Name:</label>
          <input type="text" id="client-name" name="client-name" class="form-input" required>

          <label for="client-email">Client Email:</label>
          <input type="email" id="client-email" name="client-email" class="form-input" required>

          <label for="meeting-date">Meeting Date:</label>
          <input type="date" id="meeting-date" name="meeting-date" class="form-input" required>

          <label for="meeting-time">Meeting Time:</label>
          <input type="time" id="meeting-time" name="meeting-time" class="form-input" required>

          <label for="meeting-type">Meeting Type:</label>
          <select id="meeting-type" name="meeting-type" class="form-input" required>
            <option value="">Select meeting type...</option>
            <option value="consultation">Consultation</option>
            <option value="follow-up">Follow-up</option>
            <option value="project-review">Project Review</option>
            <option value="other">Other</option>
          </select>

          <label for="meeting-notes">Additional Notes:</label>
          <textarea id="meeting-notes" name="meeting-notes" class="form-input" rows="4"></textarea>

          <button type="submit" class="submit-button">Schedule Meeting</button>
        </form>
      </section>

      <section id="meetings" class="content-section">
        <h2>Scheduled Meetings</h2>
        <table id="meetings-table">
          <caption>Upcoming client meetings</caption>
          <thead>
            <tr>
              <th>Date</th>
              <th>Time</th>
              <th>Client Name</th>
              <th>Email</th>
              <th>Type</th>
              <th>Notes</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>2026-02-05</td>
              <td>10:00 AM</td>
              <td>John Smith</td>
              <td>john@example.com</td>
              <td>Consultation</td>
              <td>Initial project discussion</td>
            </tr>
            <tr>
              <td>2026-02-07</td>
              <td>2:00 PM</td>
              <td>Sarah Johnson</td>
              <td>sarah@example.com</td>
              <td>Follow-up</td>
              <td>Review proposal</td>
            </tr>
            <tr>
              <td>2026-02-10</td>
              <td>11:00 AM</td>
              <td>Mike Davis</td>
              <td>mike@example.com</td>
              <td>Project Review</td>
              <td>Milestone check-in</td>
            </tr>
          </tbody>
        </table>
      </section>

      <section id="about" class="content-section">
        <h2>About This Scheduler</h2>
        <p>This <abbr title="Client Meeting Scheduler">CMS</abbr> helps you manage client meetings efficiently. Schedule new meetings, view upcoming appointments, and keep track of all your client interactions in one place.</p>
        <p>Built with semantic <abbr title="HyperText Markup Language">HTML</abbr> and <abbr title="Cascading Style Sheets">CSS</abbr> for a professional, accessible experience.</p>
      </section>
    </main>

    <footer id="page-footer">
      <p>&copy; <time datetime="2026">2026</time> Client Meeting Scheduler. All rights reserved.</p>
      <p>Last updated: <time datetime="2026-01-30">January 30, 2026</time></p>
    </footer>
  </body>
</html>
```

3. Press **Ctrl + S** to save the file

### What to Notice

- **Semantic structure** - Uses `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`
- **Proper form** - All inputs have labels with `for` and `id` attributes
- **Accessibility** - Alt text ready (when you add images), semantic elements, proper labels
- **Table structure** - Semantic table with `<caption>`, `<thead>`, `<tbody>`
- **Time elements** - Uses `<time>` with `datetime` attribute
- **Abbreviations** - Uses `<abbr>` with `title` attributes

**This implements all HTML concepts:** Structure, forms, tables, semantic elements, accessibility.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 9 commits.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        images/
```

**You should see `index.html` modified and `images/` untracked. This is correct.**

---

## Step 4: Create Complete CSS Stylesheet

### What This Step Does

You'll create a complete, professional CSS stylesheet that styles the entire Client Meeting Scheduler application. This will be well-organized with comments and sections, implementing all CSS concepts you've learned.

### Instructions

1. Open `css/styles.css` in VS Code
2. Replace the entire content with this complete, organized stylesheet:

```css
/* ========================================
   CLIENT MEETING SCHEDULER - STYLESHEET
   ======================================== */

/* ========================================
   RESET & BASE STYLES
   ======================================== */
* {
  box-sizing: border-box;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f5f5f5;
  color: #333;
  line-height: 1.6;
}

/* ========================================
   TYPOGRAPHY
   ======================================== */
h1 {
  font-size: 2.5em;
  font-weight: 700;
  margin: 0;
  text-align: center;
}

h2 {
  font-size: 2em;
  font-weight: 600;
  color: #0066cc;
  border-bottom: 3px solid #0066cc;
  padding-bottom: 10px;
  margin-top: 0;
}

h3 {
  font-size: 1.5em;
  font-weight: 600;
  color: #333;
  margin-top: 0;
}

p {
  margin-bottom: 15px;
  color: #555;
}

/* ========================================
   LAYOUT & STRUCTURE
   ======================================== */
#page-header {
  background: linear-gradient(to bottom, #0066cc, #004499);
  color: white;
  padding: 30px 20px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

#main-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 30px 20px;
}

.content-section {
  background-color: white;
  padding: 30px;
  margin: 30px 0;
  border-radius: 8px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

#page-footer {
  background-color: #333;
  color: white;
  padding: 20px;
  text-align: center;
  margin-top: 40px;
}

#page-footer p {
  margin: 5px 0;
  font-size: 0.9em;
}

/* ========================================
   NAVIGATION
   ======================================== */
nav ul {
  list-style: none;
  padding: 0;
  margin: 20px 0 0 0;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

nav li {
  margin: 0 15px;
}

.nav-link {
  color: white;
  text-decoration: none;
  padding: 10px 20px;
  display: inline-block;
  border-radius: 4px;
  transition: background-color 0.3s;
}

.nav-link:hover {
  background-color: rgba(255, 255, 255, 0.2);
  text-decoration: none;
}

/* ========================================
   FORMS
   ======================================== */
form {
  max-width: 600px;
  margin: 0 auto;
}

label {
  display: block;
  margin-top: 20px;
  margin-bottom: 8px;
  font-weight: 600;
  color: #333;
}

.form-input,
input[type="text"],
input[type="email"],
input[type="date"],
input[type="time"],
select,
textarea {
  width: 100%;
  padding: 12px;
  margin-bottom: 15px;
  border: 2px solid #ddd;
  border-radius: 4px;
  font-family: inherit;
  font-size: 16px;
  transition: border-color 0.3s;
  box-sizing: border-box;
}

.form-input:focus,
input:focus,
select:focus,
textarea:focus {
  outline: none;
  border-color: #0066cc;
  box-shadow: 0 0 5px rgba(0, 102, 204, 0.3);
}

.submit-button {
  background-color: #0066cc;
  color: white;
  border: none;
  border-radius: 4px;
  padding: 15px 30px;
  font-size: 18px;
  font-weight: 600;
  cursor: pointer;
  margin-top: 20px;
  width: 100%;
  transition: background-color 0.3s;
}

.submit-button:hover {
  background-color: #004499;
}

.submit-button:active {
  background-color: #003366;
}

/* ========================================
   TABLES
   ======================================== */
table {
  width: 100%;
  border-collapse: collapse;
  margin: 20px 0;
  background-color: white;
}

caption {
  font-weight: 600;
  font-size: 1.2em;
  margin-bottom: 15px;
  text-align: left;
  color: #333;
}

thead {
  background-color: #0066cc;
  color: white;
}

th {
  padding: 15px;
  text-align: left;
  font-weight: 600;
}

td {
  padding: 12px 15px;
  border-bottom: 1px solid #ddd;
}

tbody tr:hover {
  background-color: #f0f7ff;
}

tbody tr:last-child td {
  border-bottom: none;
}

/* ========================================
   UTILITY CLASSES
   ======================================== */
.content-section {
  clear: both;
}

abbr {
  text-decoration: underline;
  text-decoration-style: dotted;
  cursor: help;
}

/* ========================================
   RESPONSIVE DESIGN
   ======================================== */
/* For tablets and smaller screens */
@media (max-width: 768px) {
  h1 {
    font-size: 2em;
  }

  h2 {
    font-size: 1.5em;
  }

  #main-content {
    padding: 15px;
  }

  .content-section {
    padding: 20px;
    margin: 20px 0;
  }

  nav ul {
    flex-direction: column;
    align-items: center;
  }

  nav li {
    margin: 5px 0;
  }

  .nav-link {
    width: 100%;
    text-align: center;
  }

  table {
    font-size: 0.9em;
  }

  th, td {
    padding: 8px;
  }
}

/* For mobile phones */
@media (max-width: 480px) {
  h1 {
    font-size: 1.5em;
  }

  h2 {
    font-size: 1.3em;
  }

  #page-header {
    padding: 20px 15px;
  }

  .content-section {
    padding: 15px;
  }

  table {
    display: block;
    overflow-x: auto;
  }

  thead, tbody, tr, td, th {
    display: block;
  }

  thead {
    display: none;
  }

  tr {
    border: 1px solid #ddd;
    margin-bottom: 10px;
    padding: 10px;
  }

  td {
    border: none;
    padding: 5px 0;
    text-align: right;
    position: relative;
    padding-left: 50%;
  }

  td::before {
    content: attr(data-label);
    position: absolute;
    left: 0;
    width: 45%;
    text-align: left;
    font-weight: 600;
    color: #0066cc;
  }
}
```

3. Press **Ctrl + S** to save the file

### What to Notice

- **Complete organization** - Sections clearly separated with comments
- **Professional styling** - Colors, spacing, typography all work together
- **Form styling** - Focus states, transitions, professional appearance
- **Table styling** - Hover effects, proper spacing, readable layout
- **Responsive design** - Media queries for tablets and mobile
- **Mobile table** - Special mobile layout for tables (stacks vertically)

**This implements all CSS concepts:** Selectors, styling, box model, layout, responsive design, organization.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should see both `index.html` and `css/styles.css` as modified. This is correct.**

---

## Step 5: Preview Your Complete Application

### What This Step Does

Previewing lets you see your complete Client Meeting Scheduler application. You'll verify that all elements display correctly, forms work, tables look good, and the responsive design functions properly.

### Instructions

1. In VS Code file explorer, right-click on `index.html`
2. Click **Open with Live Server**

**Expected Result:** Your browser should show the complete Client Meeting Scheduler application.

### Verify What You See

You should see:
- ✅ Professional header with navigation
- ✅ Schedule Meeting form with all fields
- ✅ Scheduled Meetings table with sample data
- ✅ About section with information
- ✅ Footer with copyright and date
- ✅ Consistent styling throughout
- ✅ Responsive design (test by resizing window)

### Test Responsive Design

1. **Resize browser window** to test responsive design
2. **At 768px and below** - Layout should adapt for tablets
3. **At 480px and below** - Layout should adapt for mobile (table stacks vertically)
4. **Navigation** - Should stack vertically on mobile

**If everything looks good, proceed to Step 6.**
**If something doesn't look right, check that both files are saved and refresh the browser.**

---

## Step 6: Add Data Labels for Mobile Table (Optional Enhancement)

### What This Step Does

For the mobile table layout to work properly with the CSS you added, you need to add `data-label` attributes to table cells. This makes the mobile table more readable.

### Instructions

1. In `index.html`, find the table body rows
2. Add `data-label` attributes to each `<td>`:

```html
            <tr>
              <td data-label="Date">2026-02-05</td>
              <td data-label="Time">10:00 AM</td>
              <td data-label="Client Name">John Smith</td>
              <td data-label="Email">john@example.com</td>
              <td data-label="Type">Consultation</td>
              <td data-label="Notes">Initial project discussion</td>
            </tr>
```

3. Repeat for all table rows
4. Press **Ctrl + S** to save

**This enhances mobile experience:** On mobile, each cell shows its label, making the table readable even on small screens.

---

## Step 7: Commit Your Work

### What This Step Does

You've built a complete Client Meeting Scheduler application. Now you'll commit all your work following professional habits. This is a significant milestone - you've created a portfolio-ready project!

### Safety Check Before Committing

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 9 commits.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   css/styles.css
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        images/

no changes added to commit (use "git add" or "git commit -a")
```

**Verify:**
- ✅ You are on `main` branch
- ✅ `index.html` and `css/styles.css` are modified
- ✅ `images/` folder exists (even if empty)
- ✅ No unexpected files are listed

**If everything looks correct, proceed to staging.**
**If you see unexpected files, review your work before committing.**

### Stage All Files

1. In the terminal, type exactly:
   ```bash
   git add index.html css/styles.css images/
   ```
2. Press **Enter**

**Expected Result:** No error message, prompt returns.

**Note:** Staging `images/` adds the folder. Even if it's empty now, it's part of your organized structure.

### Verify Files are Staged

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 9 commits.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
        new file:   images/
        modified:   css/styles.css
        modified:   index.html
```

**If you see all files under "Changes to be committed", proceed to commit.**

### Create the Commit

1. In the terminal, type exactly:
   ```bash
   git commit -m "s3: complete Client Meeting Scheduler capstone project"
   ```
2. Press **Enter**

**Expected Output:**
```
[main bcd5678] s3: complete Client Meeting Scheduler capstone project
 3 files changed, XX insertions(+), X deletions(-)
 create mode 100644 images/
```

**The commit hash (bcd5678) will be different - that's normal.**

### Verify Commit Success

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 10 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

**Key indicators:**
- ✅ "Your branch is ahead of 'origin/main' by 10 commits" - You now have 10 local commits
- ✅ "nothing to commit, working tree clean" - All changes are committed

**If you see this, your commit was successful. Proceed to final verification.**

---

## Expected Final State

After completing this exercise, you should have:

- ✅ Complete Client Meeting Scheduler application
- ✅ Proper file organization (css/, images/ folders)
- ✅ Semantic HTML throughout
- ✅ Accessible forms with proper labels
- ✅ Styled table with sample data
- ✅ Responsive design (works on all screen sizes)
- ✅ Organized CSS with comments and sections
- ✅ Professional, portfolio-ready project
- ✅ All changes committed to Git
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
Your branch is ahead of 'origin/main' by 10 commits.

nothing to commit, working tree clean
```

**If you see "working tree clean", congratulations! You've completed the capstone project!**

---

## What You've Accomplished

You've successfully completed Section 3: HTML & CSS Foundations! You've learned:

- ✅ HTML document structure and semantic elements
- ✅ HTML content elements (links, lists, images, tables, forms)
- ✅ CSS styling (selectors, properties, box model)
- ✅ CSS layout (float, display, responsive design)
- ✅ File organization (proper folder structure)
- ✅ Professional workflow (Git, organized code)
- ✅ Built a complete, portfolio-ready project

**This is a significant achievement!** You now have the skills to build web pages from scratch and a project you can show to employers.

---

## Next Steps

After completing this section, you can:

- **Push to GitHub** - Share your work: `git push`
- **Continue to Section 4** - Learn JavaScript Fundamentals
- **Enhance this project** - Add more features, improve styling
- **Build more projects** - Practice your HTML and CSS skills

---

## Troubleshooting

### Problem: Layout doesn't look right

**Solution:**
- Check that CSS file is linked: `<link rel="stylesheet" href="css/styles.css">`
- Verify file paths are correct (css/styles.css, not styles.css)
- Make sure both files are saved
- Check browser console for errors (F12)

### Problem: Form doesn't submit

**Solution:**
- This is expected - forms need backend code to actually submit
- The HTML structure is correct
- In real projects, you'd add `action` and `method` attributes and backend code
- For now, focus on the HTML and CSS structure

### Problem: Mobile table doesn't show labels

**Solution:**
- Make sure you added `data-label` attributes to table cells
- Verify CSS media query is correct for mobile
- Check that you're testing at 480px or smaller width

### Problem: Images folder is empty

**Solution:**
- This is fine! The folder is part of your organized structure
- You can add images later if needed
- The important thing is having the proper folder structure

---

## Navigation

**Previous Exercise:** [[s3-html-css/s3e9-css-layout-with-float|Exercise 9: CSS Layout with Float]]

**Next Section:** [[s4-js/index|Section 4: JavaScript Basics]]

**Home:** [[index|Main Course Page]]

**Return to Section:** [[s3-html-css/index|HTML & CSS Section]]

**Congratulations on completing the HTML & CSS section!**
