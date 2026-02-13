---
title: "C1S3E7: CSS Selectors"
description: Learn about CSS selectors, how to target elements, and understand CSS cascade and specificity. Practice with developer tools.
tags:
  - css
  - selectors
  - cascade
  - specificity
  - beginner
  - workbook
draft: false
date: 2026-01-30
---
# Exercise 7: CSS Selectors
**Time Required:** 30-35 minutes

---
## Getting Started
### Prerequisites Check
Before starting, verify:

1. ✅ **Exercise 6 completed**
   - `css/styles.css` file exists with CSS rules
   - CSS file is linked to HTML
   - All changes from Exercise 6 are committed

2. ✅ **Current State Verification**
   - Open VS Code terminal (Ctrl + ~)
   - Type: `git status`
   - Press Enter

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 6 commits.

nothing to commit, working tree clean
```

**If you see this, proceed.**
**If not, complete Exercise 6 first or resolve any uncommitted changes.**
### What to Expect
By the end of this exercise, you will have:

- Used various CSS selectors (element, ID, class, descendant)
- Grouped multiple selectors together
- Understood CSS cascade (how order matters)
- Understood CSS specificity (how browsers choose which styles apply)
- Practiced using developer tools to inspect selectors
- Committed your work with Git

---
## Step 1: Understand CSS Selectors

### What This Step Does

CSS selectors are patterns that tell the browser which HTML elements to style. Understanding selectors is essential for writing effective CSS. Different selectors have different levels of specificity, which determines which styles apply when multiple rules target the same element.

**Basic selector types:**
- **Element selectors** - Target elements by tag name (`p`, `h1`, `div`)
- **ID selectors** - Target elements by ID (`#header`, `#main-content`)
- **Class selectors** - Target elements by class (`.nav-link`, `.form-input`)
- **Descendant selectors** - Target elements inside other elements (`nav a`, `section p`)

**Why selectors matter:** The selector you choose determines which elements get styled and how specific your rule is. More specific selectors override less specific ones.

---
## Step 2: Use Element Selectors

### What This Step Does

Element selectors are the simplest type - they target all elements of a specific type. You'll add some element selector rules to see how they work.

### Instructions

1. Open `css/styles.css` in VS Code
2. Add these element selector rules at the end of the file:

```css
/* Element Selectors */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

h2 {
  color: #0066cc;
  border-bottom: 2px solid #0066cc;
  padding-bottom: 10px;
}

footer {
  background-color: #f5f5f5;
  padding: 20px;
  text-align: center;
  margin-top: 40px;
}
```

3. Press **Ctrl + S** to save the file

### What to Notice

- **`body { }`** - Targets the `<body>` element. This affects the entire page (font, default margins/padding).
- **`h2 { }`** - Targets all `<h2>` elements. Every `<h2>` on the page gets these styles.
- **`footer { }`** - Targets the `<footer>` element.

**Element selectors are broad:** They apply to ALL elements of that type on the page. Use them for base styles that should apply everywhere.

### Verify Changes

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 6 commits.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   css/styles.css
```

**If you see `css/styles.css` listed as modified, proceed to Step 3.**

---
## Step 3: Use ID Selectors

### What This Step Does

ID selectors target elements with a specific ID. IDs are unique (only one element per page can have a specific ID), so ID selectors are very specific. You'll style your header, main content, and footer using their IDs.

### Instructions

1. In `css/styles.css`, add these ID selector rules:

```css
/* ID Selectors */
#page-header {
  background-color: #0066cc;
  color: white;
  padding: 20px;
}

#main-content {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

#page-footer {
  border-top: 1px solid #ccc;
}
```

2. Press **Ctrl + S** to save the file

### What to Notice

- **`#page-header`** - The `#` symbol means "ID selector". This targets the element with `id="page-header"`.
- **ID selectors are specific** - Because IDs are unique, these rules only affect one element each.
- **Specificity** - ID selectors have higher specificity than element selectors, so they override element selector rules.

**Preview:** Refresh your browser and you should see the header has a blue background, the main content is centered with a max width, and the footer has a border.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see `css/styles.css` as modified. This is correct.**

---
## Step 4: Use Class Selectors

### What This Step Does

Class selectors target elements with a specific class. Classes are reusable (many elements can share the same class), so class selectors are great for styling groups of similar elements. You'll style your navigation links and form inputs using their classes.

### Instructions

1. In `css/styles.css`, update and expand the class selector rules:

```css
/* Class Selectors */
.nav-link {
  color: white;
  text-decoration: none;
  padding: 10px 15px;
  display: inline-block;
}

.nav-link:hover {
  background-color: #004499;
  text-decoration: underline;
}

.form-input {
  width: 100%;
  padding: 10px;
  margin: 5px 0;
  border: 1px solid #ccc;
  border-radius: 4px;
}
```

2. Press **Ctrl + S** to save the file

### What to Notice

- **`.nav-link`** - The `.` symbol means "class selector". This targets all elements with `class="nav-link"`.
- **Multiple elements** - All three navigation links share the `nav-link` class, so they all get the same styles.
- **Hover pseudo-class** - `.nav-link:hover` applies styles when users hover over the link.
- **Reusability** - Classes let you style multiple elements consistently.

**Preview:** Refresh your browser. Navigation links should be white with padding, and form inputs should have consistent styling.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see `css/styles.css` as modified. This is correct.**

---
## Step 5: Use Descendant Selectors

### What This Step Does

Descendant selectors target elements that are inside other elements. This lets you style elements based on their context (where they appear in the HTML structure). You'll style links and paragraphs differently depending on where they appear.

### Instructions

1. In `css/styles.css`, add these descendant selector rules:

```css
/* Descendant Selectors */
nav ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
}

nav li {
  margin-right: 20px;
}

section p {
  margin-bottom: 15px;
}

footer p {
  margin: 5px 0;
  font-size: 0.9em;
  color: #666;
}
```

2. Press **Ctrl + S** to save the file

### What to Notice

- **`nav ul`** - Targets `<ul>` elements that are inside `<nav>` elements. Other `<ul>` elements on the page aren't affected.
- **`nav li`** - Targets `<li>` elements inside `<nav>`. This only affects navigation list items.
- **`section p`** - Targets `<p>` elements inside `<section>` elements.
- **`footer p`** - Targets `<p>` elements inside `<footer>`. This is more specific than just `p`, so it overrides general paragraph styles for footer paragraphs.

**Context matters:** Descendant selectors let you style elements differently based on where they appear. A paragraph in the footer can look different from a paragraph in a section.

**Preview:** Refresh your browser. Navigation should be horizontal (flex), and footer paragraphs should be smaller and gray.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see `css/styles.css` as modified. This is correct.**

---
## Step 6: Group Multiple Selectors

### What This Step Does

You can apply the same styles to multiple selectors by grouping them with commas. This is efficient and helps keep your CSS organized. Instead of writing the same styles multiple times, you write them once and list all the selectors.

### Instructions

1. In `css/styles.css`, add these grouped selector rules:

```css
/* Grouping Selectors */
h1, h2, h3 {
  margin-top: 0;
}

section, article, aside {
  margin-bottom: 30px;
}

input[type="text"],
input[type="email"],
input[type="tel"],
textarea {
  font-family: Arial, sans-serif;
  font-size: 16px;
}
```

2. Press **Ctrl + S** to save the file

### What to Notice

- **Comma separation** - `h1, h2, h3` means "apply these styles to h1, h2, AND h3 elements"
- **Efficiency** - Instead of writing the same styles three times, you write them once
- **Attribute selectors** - `input[type="text"]` targets inputs with a specific type attribute
- **Multiple grouped selectors** - You can group as many selectors as you want

**Benefits of grouping:** Reduces code duplication, makes updates easier (change once, affects all), and keeps CSS organized.

**Preview:** Refresh your browser. Headings should have no top margin, and form inputs should have consistent font styling.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see `css/styles.css` as modified. This is correct.**

---
## Step 7: Understand CSS Cascade

### What This Step Does

The CSS cascade determines which styles apply when multiple rules target the same element. Understanding the cascade is essential for debugging CSS and knowing why certain styles aren't applying. The cascade has three main factors: source order, specificity, and importance.

**The Cascade Rules (in order of priority):**
1. **Source order** - Later rules override earlier ones (if specificity is equal)
2. **Specificity** - More specific selectors override less specific ones
3. **Importance** - `!important` declarations override others (use sparingly)

### Create a Cascade Example

1. In `css/styles.css`, add these rules to demonstrate cascade:

```css
/* Cascade Example - Source Order Matters */
p {
  color: black;
}

p {
  color: blue;  /* This wins because it comes later */
}

/* More specific selector wins */
section p {
  color: green;  /* This wins over just 'p' because it's more specific */
}
```

2. Press **Ctrl + S** to save

**What happens:**
- First `p { color: black; }` sets paragraphs to black
- Second `p { color: blue; }` overrides it to blue (same specificity, later in file)
- `section p { color: green; }` overrides to green (more specific selector)

**Preview:** Refresh your browser. Paragraphs in sections should be green, other paragraphs should be blue.

**Key takeaway:** When specificity is equal, the last rule wins. When specificity differs, the more specific rule wins.

---
## Step 8: Understand CSS Specificity

### What This Step Does

CSS specificity is a calculation that determines which selector is "stronger" when multiple rules target the same element. Understanding specificity helps you write CSS that works as expected and debug why styles aren't applying.

**Specificity Calculation:**
Browsers calculate specificity points:
- **Inline styles** - 1000 points
- **IDs** - 100 points each
- **Classes, attributes, pseudo-classes** - 10 points each
- **Elements, pseudo-elements** - 1 point each

**Higher specificity wins** when rules conflict.

### Create Specificity Examples

1. In `css/styles.css`, add these specificity examples:

```css
/* Specificity Examples */
/* This has 1 point (element) */
p {
  color: red;
}

/* This has 10 points (class) */
.intro {
  color: blue;
}

/* This has 100 points (ID) */
#main-content {
  color: green;
}

/* This has 11 points (element + class) */
p.intro {
  color: purple;
}

/* This has 101 points (ID + element) */
#main-content p {
  color: orange;
}
```

2. Press **Ctrl + S** to save

**What happens:**
- A paragraph with no class or ID: red (1 point)
- A paragraph with `class="intro"`: blue (10 points beats 1)
- A paragraph with `id="main-content"`: green (100 points beats 10)
- A paragraph with `class="intro"` AND `p.intro` selector: purple (11 points beats 10)
- A paragraph inside `#main-content` with `#main-content p`: orange (101 points beats all)

**Preview:** Refresh your browser. Different paragraphs should show different colors based on their specificity.

**Key takeaway:** More specific selectors (higher points) always win, regardless of source order.

---
## Step 9: Use Developer Tools to Inspect Specificity

### What This Step Does

Developer tools show you which CSS rules are active, their specificity, and which ones are being overridden. This is essential for debugging CSS and understanding why styles aren't applying as expected.

### Instructions

1. Open your page in the browser with Live Server
2. **Right-click** on a paragraph element
3. Click **Inspect** or **Inspect Element**
4. In the developer tools, look at the **Styles** panel (usually on the right)

### What You Can See

- **Active rules** - CSS rules that are currently applied to the element
- **Overridden rules** - CSS rules that are being overridden (usually shown with strikethrough)
- **Specificity** - Some developer tools show specificity values
- **Source** - Which CSS file and line number the rule comes from

### Try This

1. **Select different elements** - Click on various elements (paragraphs, headings, links)
2. **See which rules apply** - Look at the Styles panel to see active CSS rules
3. **See overridden rules** - Notice rules with strikethrough (these are overridden by more specific rules)
4. **Test specificity** - Select a paragraph with a class and see how class selector beats element selector

**This is how developers debug CSS:** When styles aren't working, developer tools show you exactly which rules are active and why others are being overridden.

---
## Step 10: Commit Your Work

### What This Step Does

You've added many CSS selectors and learned about cascade and specificity. Now you'll commit this change following professional habits.

### Safety Check Before Committing

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 6 commits.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   css/styles.css

no changes added to commit (use "git add" or "git commit -a")
```

**Verify:**
- ✅ You are on `main` branch
- ✅ Only `css/styles.css` is modified
- ✅ No unexpected files are listed

**If everything looks correct, proceed to staging.**
**If you see unexpected files, review your work before committing.**

### Stage the File

1. In the terminal, type exactly:
   ```bash
   git add css/styles.css
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
Your branch is ahead of 'origin/main' by 6 commits.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
        modified:   css/styles.css
```

**If you see `css/styles.css` under "Changes to be committed", proceed to commit.**

### Create the Commit

1. In the terminal, type exactly:
   ```bash
   git commit -m "s3: add CSS selectors and demonstrate cascade and specificity"
   ```
2. Press **Enter**

**Expected Output:**
```
[main stu4567] s3: add CSS selectors and demonstrate cascade and specificity
 1 file changed, XX insertions(+), X deletions(-)
```

**The commit hash (stu4567) will be different - that's normal.**

### Verify Commit Success

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 7 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

**Key indicators:**
- ✅ "Your branch is ahead of 'origin/main' by 7 commits" - You now have 7 local commits
- ✅ "nothing to commit, working tree clean" - All changes are committed

**If you see this, your commit was successful. Proceed to final verification.**

---
## Expected Final State

After completing this exercise, you should have:

- ✅ CSS rules using element, ID, class, and descendant selectors
- ✅ Grouped selectors for efficient styling
- ✅ Understanding of CSS cascade (source order matters)
- ✅ Understanding of CSS specificity (more specific wins)
- ✅ Experience using developer tools to inspect selectors
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
Your branch is ahead of 'origin/main' by 7 commits.

nothing to commit, working tree clean
```

**If you see "working tree clean", you're ready for the next exercise.**

---
## What This Sets Up for Exercise 8

You now understand how to target elements with CSS selectors and how the cascade and specificity work. In the next exercise, you'll learn more about CSS styling properties (text, borders, backgrounds) and practice the box model. You'll also organize your CSS with comments and sections.

---
#### Next Steps: Return to the [HTML-CSS Lecture](8. CSS Styling Fundamentals### 8.-CSS-Styling-Fundamentals)
8. CSS Styling Fundamentals

---
## Troubleshooting

### Problem: Styles aren't applying as expected

**Solution:**
- Check specificity - more specific selectors override less specific ones
- Check source order - later rules override earlier ones (if specificity is equal)
- Use developer tools to see which rules are active and which are overridden
- Verify selectors are spelled correctly (case-sensitive)

### Problem: Can't see specificity in developer tools

**Solution:**
- Different browsers show specificity differently
- Look for overridden rules (with strikethrough) - these show which rules lost
- Some browsers show specificity in computed styles or in a separate panel
- The important thing is understanding the concept, not seeing exact numbers

### Problem: Grouped selectors don't work

**Solution:**
- Make sure selectors are separated by commas: `h1, h2, h3`
- Don't put a comma after the last selector
- Verify all selectors in the group are valid
- Check for typos in selector names

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