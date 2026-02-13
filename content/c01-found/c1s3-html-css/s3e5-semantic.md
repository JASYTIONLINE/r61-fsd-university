---
title: "C1S3E5: Using Semantic HTML Structure"
description: Improve your HTML structure using semantic elements, ID and class attributes. Learn about header, footer, nav, section, and other semantic elements.
tags:
  - html
  - semantic-html
  - accessibility
  - structure
  - beginner
  - workbook
draft: false
date: 2026-01-30
---
# Exercise 5: Using Semantic HTML Structure
**Time Required:** 25-30 minutes

---
## Getting Started
### Prerequisites Check
Before starting, verify:

1. ✅ **Exercise 4 completed**
   - `index.html` file has a contact form
   - All changes from Exercise 4 are committed
   - You can preview your page in a browser

2. ✅ **Current State Verification**
   - Open VS Code terminal (Ctrl + ~)
   - Type: `git status`
   - Press Enter

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 4 commits.

nothing to commit, working tree clean
```

**If you see this, proceed.**
**If not, complete Exercise 4 first or resolve any uncommitted changes.**
### What to Expect
By the end of this exercise, you will have:

- Used ID and class attributes to identify and group elements
- Added semantic HTML elements (header, footer, nav, section)
- Used time and abbreviation elements
- Improved your page structure for accessibility and maintainability
- Committed your work with Git

---
## Step 1: Understand ID and Class Attributes

### What This Step Does

ID and class attributes help you identify and organize HTML elements. They're essential for styling with CSS (which you'll learn in the next exercises) and for creating semantic, accessible HTML. Understanding when to use IDs versus classes is important for good HTML structure.

**ID attributes:**
- **Unique** - Only one element per page can have a specific ID
- **Use for:** Unique page elements like header, main content, footer
- **Example:** `id="header"`, `id="main-content"`, `id="contact-form"`

**Class attributes:**
- **Reusable** - Multiple elements can share the same class
- **Use for:** Groups of similar elements (buttons, cards, navigation items)
- **Example:** `class="button"`, `class="card"`, `class="nav-item"`

**Best practices:**
- Use IDs for unique, one-of-a-kind elements
- Use classes for repeated patterns or groups of elements
- Use meaningful names that describe purpose, not appearance
- Use kebab-case (lowercase with hyphens) for names: `main-content`, not `mainContent` or `MainContent`

---
## Step 2: Add Semantic Structure to Your Page

### What This Step Does

You'll wrap your existing content in semantic HTML elements. This improves accessibility (screen readers understand the page structure), SEO (search engines understand content hierarchy), and maintainability (code is easier to read and modify). You'll add a header, nav, main content sections, and a footer.

### Instructions

1. Open `index.html` in VS Code
2. Find the opening `<body>` tag
3. Add a header section **immediately after** `<body>`:

```html
  <header id="page-header">
    <h1>Welcome to My First Webpage</h1>
    <nav>
      <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#schedule">Schedule</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>
```

4. Find your existing `<h1>` tag (the one that says "Welcome to My First Webpage")
5. **Delete** that `<h1>` tag and its content (it's now in the header)
6. Find the paragraph that comes right after where the `<h1>` was
7. Wrap all your main content (from the first paragraph through the form) in a `<main>` tag:

```html
  <main id="main-content">
    <!-- All your existing content goes here -->
  </main>
```

8. Add a footer **before** the closing `</body>` tag:

```html
  <footer id="page-footer">
    <p>&copy; 2026 My Learning Journey. All rights reserved.</p>
    <p>Last updated: <time datetime="2026-01-30">January 30, 2026</time></p>
  </footer>
```

9. Press **Ctrl + S** to save the file

### What to Notice

- **`<header>`** - This semantic element represents the introductory content of a page or section. It typically contains the site title, logo, and navigation.
- **`id="page-header"`** - This ID uniquely identifies the header. You can reference it in CSS or JavaScript later.
- **`<nav>`** - This semantic element represents navigation links. Screen readers use this to identify navigation sections.
- **`<main>`** - This semantic element represents the main content of the page. There should be only one `<main>` per page.
- **`id="main-content"`** - This ID uniquely identifies the main content area.
- **`<footer>`** - This semantic element represents footer content (copyright, contact info, etc.).
- **`id="page-footer"`** - This ID uniquely identifies the footer.
- **`<time>`** - This semantic element represents dates and times. The `datetime` attribute provides a machine-readable format, while the text between tags is human-readable.
- **`&copy;`** - This is an HTML entity that displays the copyright symbol (©).

**Semantic Benefits:** Using semantic elements helps screen readers navigate your page, helps search engines understand your content, and makes your code more maintainable.

### Verify Changes

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 4 commits.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   index.html
```

**If you see `index.html` listed as modified, proceed to Step 3.**

---
## Step 3: Add Section Elements and IDs

### What This Step Does

You'll organize your content into logical sections using the `<section>` element. Each section will have an ID that matches the navigation links you created. This creates a clear page structure and makes anchor links work properly.

### Instructions

1. In `index.html`, find your main content (inside the `<main>` tag)
2. Wrap your content in sections with IDs:

```html
    <section id="about">
      <h2>About This Page</h2>
      <p>This is my first paragraph. I'm learning HTML!</p>
      <p>This is my second paragraph. HTML is the structure of web pages.</p>
      <!-- Keep your image, links, and lists here -->
    </section>

    <section id="schedule">
      <h2>Weekly Schedule</h2>
      <!-- Keep your table here -->
    </section>

    <section id="contact">
      <h2>Contact Me</h2>
      <!-- Keep your form here -->
    </section>
```

3. **Important:** Make sure the section IDs match the navigation links:
   - `id="about"` matches `href="#about"` in nav
   - `id="schedule"` matches `href="#schedule"` in nav
   - `id="contact"` matches `href="#contact"` in nav (you already have this from Exercise 2)

4. Press **Ctrl + S** to save the file

### What to Notice

- **`<section>`** - This semantic element represents a thematic grouping of content. Each section should have a heading.
- **Section IDs** - These IDs allow navigation links to jump to specific sections. They also provide unique identifiers for styling.
- **Matching IDs and links** - The `href="#about"` in the navigation matches `id="about"` in the section. This is how anchor links work.

**Note:** You may need to remove the old `<h2>` tags that are now redundant (like "Weekly Schedule" and "Contact Me" if they're already in sections). Keep the structure clean.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see `index.html` as modified. This is correct.**

---
## Step 4: Add Class Attributes to Similar Elements

### What This Step Does

You'll add class attributes to groups of similar elements. This demonstrates how classes work for reusable patterns. In this case, you'll add classes to navigation items and form inputs to show how classes group related elements.

### Instructions

1. In `index.html`, find the navigation list items
2. Add a class to each navigation link:

```html
        <li><a href="#about" class="nav-link">About</a></li>
        <li><a href="#schedule" class="nav-link">Schedule</a></li>
        <li><a href="#contact" class="nav-link">Contact</a></li>
```

3. Find your form inputs
4. Add a class to the text inputs:

```html
  <input type="text" id="name" name="name" class="form-input" required>
  <input type="email" id="email" name="email" class="form-input" required>
  <input type="tel" id="phone" name="phone" class="form-input">
```

5. Press **Ctrl + S** to save the file

### What to Notice

- **`class="nav-link"`** - All three navigation links share this class. This allows you to style all navigation links the same way (which you'll do with CSS later).
- **`class="form-input"`** - All text inputs share this class. This allows you to style all form inputs consistently.
- **Multiple classes** - Elements can have multiple classes: `class="form-input required"` (separated by spaces).
- **Reusability** - Classes are reusable. Many elements can share the same class, making it easy to apply consistent styling.

**Class vs ID:** Remember, IDs are unique (one per page), classes are reusable (many per page). Use IDs for unique elements, classes for groups of similar elements.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see `index.html` as modified. This is correct.**

---
## Step 5: Add Abbreviation Element

### What This Step Does

The `<abbr>` element is a semantic way to mark abbreviations and acronyms. When users hover over an abbreviation, browsers can show the full text. This improves accessibility and helps users understand abbreviations they might not know.

### Instructions

1. In `index.html`, find a place where you might use an abbreviation (like in your paragraphs or footer)
2. For example, in your footer or about section, add:

```html
    <p>I'm learning <abbr title="HyperText Markup Language">HTML</abbr> and <abbr title="Cascading Style Sheets">CSS</abbr>.</p>
```

3. Press **Ctrl + S** to save the file

### What to Notice

- **`<abbr>`** - This semantic element marks abbreviations and acronyms.
- **`title` attribute** - This provides the full text of the abbreviation. When users hover over "HTML", they'll see "HyperText Markup Language".
- **Accessibility** - Screen readers can announce the full text, helping users understand abbreviations.

**Best Practice:** Use `<abbr>` for any abbreviation that might not be universally understood. Common examples: HTML, CSS, API, URL, etc.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see `index.html` as modified. This is correct.**

---
## Step 6: Test Navigation Links

### What This Step Does

You'll test that the navigation links you created actually work. Clicking "About", "Schedule", or "Contact" in the navigation should jump to the corresponding section on the page.

### Instructions

1. In VS Code file explorer, right-click on `index.html`
2. Click **Open with Live Server** (or refresh if already open)

**Expected Result:** Your browser should show the updated page with a header containing navigation.

### Test the Navigation

1. Click "About" in the navigation - page should scroll to the about section
2. Click "Schedule" in the navigation - page should scroll to the schedule section
3. Click "Contact" in the navigation - page should scroll to the contact section

**If the navigation links work, proceed to Step 7.**
**If links don't work, check that section IDs match the href values in navigation (case-sensitive).**

---
## Step 7: Commit Your Work

### What This Step Does

You've restructured your page with semantic HTML elements and proper IDs and classes. Now you'll commit this change following professional habits.

### Safety Check Before Committing

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 4 commits.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   index.html

no changes added to commit (use "git add" or "git commit -a")
```

**Verify:**
- ✅ You are on `main` branch
- ✅ Only `index.html` is modified
- ✅ No unexpected files are listed

**If everything looks correct, proceed to staging.**
**If you see unexpected files, review your work before committing.**

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
Your branch is ahead of 'origin/main' by 4 commits.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
        modified:   index.html
```

**If you see `index.html` under "Changes to be committed", proceed to commit.**

### Create the Commit

1. In the terminal, type exactly:
   ```bash
   git commit -m "s3: add semantic HTML structure with header, nav, sections, footer"
   ```
2. Press **Enter**

**Expected Output:**
```
[main mno3456] s3: add semantic HTML structure with header, nav, sections, footer
 1 file changed, XX insertions(+), X deletions(-)
```

**The commit hash (mno3456) will be different - that's normal.**

### Verify Commit Success

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 5 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

**Key indicators:**
- ✅ "Your branch is ahead of 'origin/main' by 5 commits" - You now have 5 local commits
- ✅ "nothing to commit, working tree clean" - All changes are committed

**If you see this, your commit was successful. Proceed to final verification.**

---
## Expected Final State

After completing this exercise, you should have:

- ✅ Semantic HTML structure with header, nav, main, sections, and footer
- ✅ ID attributes on unique elements (header, main, footer, sections)
- ✅ Class attributes on groups of similar elements (nav-link, form-input)
- ✅ Working navigation with anchor links
- ✅ Time and abbreviation elements used appropriately
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
Your branch is ahead of 'origin/main' by 5 commits.

nothing to commit, working tree clean
```

**If you see "working tree clean", you're ready for the next exercise.**

---
## What This Sets Up for Exercise 6

You now have a well-structured HTML page with semantic elements and proper IDs and classes. In the next exercise, you'll learn about CSS and how to style your page. The IDs and classes you just added will be essential for targeting elements with CSS selectors.

---
#### Next Steps: Return to the [HTML-CSS Lecture](6. Introduction to CSS#6.-Introduction-to-CSS)
6. Introduction to CSS

---
## Troubleshooting

### Problem: Navigation links don't jump to sections

**Solution:**
- Check that section IDs match the href values exactly (case-sensitive)
- Verify IDs use the same text: `id="about"` matches `href="#about"`
- Make sure you added the `#` symbol in href (like `href="#about"`, not `href="about"`)

### Problem: Page structure looks broken

**Solution:**
- Check that all opening tags have matching closing tags
- Verify semantic elements are properly nested (header, nav, main, section, footer)
- Make sure you didn't accidentally delete important content when restructuring

### Problem: Abbreviation doesn't show tooltip

**Solution:**
- Make sure you included the `title` attribute: `<abbr title="Full Text">ABBR</abbr>`
- Hover over the abbreviation (don't just click it)
- Some browsers show tooltips on hover, others show them in different ways

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