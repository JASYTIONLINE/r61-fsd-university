---
title: "Exercise 6: Introduction to CSS"
description: "Learn how to add CSS to your webpage. Create organized file structure, understand the box model, and use browser developer tools."
tags: [css, styling, box-model, developer-tools, file-organization, beginner, workbook]
draft: false
date: "2026-01-30"
---

# Exercise 6: Introduction to CSS

**This exercise continues from Exercise 5. You must complete Exercise 5 first.**

**This exercise is a standalone technical manual. Follow each step exactly.**

**Time Required:** 30-35 minutes

---

## Prerequisites Check

Before starting, verify:

1. ✅ **Exercise 5 completed**
   - `index.html` file has semantic HTML structure with IDs and classes
   - All changes from Exercise 5 are committed
   - You can preview your page in a browser

2. ✅ **Current State Verification**
   - Open VS Code terminal (Ctrl + ~)
   - Type: `git status`
   - Press Enter

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 5 commits.

nothing to commit, working tree clean
```

**If you see this, proceed.**
**If not, complete Exercise 5 first or resolve any uncommitted changes.**

---

## What You Will Accomplish

By the end of this exercise, you will have:

- Added inline CSS styles to understand how CSS works
- Created a CSS file and linked it to your HTML
- Set up proper file organization (css/ folder)
- Learned about the CSS box model
- Used browser developer tools to inspect elements
- Committed your work with Git

---

## Step 1: Understand How HTML and CSS Work Together

### What This Step Does

Before adding CSS, it's important to understand how HTML and CSS work together. HTML provides the structure and content (what's on the page), while CSS provides the presentation (how it looks). CSS uses selectors to target HTML elements and applies styles to them.

**The relationship:**
- HTML elements are styled by CSS rules
- CSS selectors target HTML elements (by element name, ID, or class)
- CSS properties change how elements look (color, size, spacing, etc.)
- The browser combines HTML structure with CSS styles to render the final page

**Three ways to add CSS:**
1. **Inline styles** - CSS written directly in the HTML using the `style` attribute
2. **Internal styles** - CSS written in a `<style>` tag in the HTML `<head>`
3. **External stylesheets** - CSS written in a separate `.css` file, linked in the HTML

For this exercise, you'll try inline styles first (to see how CSS works), then move to external stylesheets (the best practice).

---

## Step 2: Add Inline CSS to Understand How It Works

### What This Step Does

You'll add inline CSS to see how CSS works in action. Inline styles are written directly on HTML elements using the `style` attribute. This is quick for testing, but not ideal for larger projects. You'll use it here just to see CSS in action, then move to better methods.

### Instructions

1. Open `index.html` in VS Code
2. Find the `<h1>` tag in your header (the one that says "Welcome to My First Webpage")
3. Add a `style` attribute to it:

```html
    <h1 style="color: blue; font-size: 2.5em;">Welcome to My First Webpage</h1>
```

4. Find a paragraph in your about section
5. Add a `style` attribute to it:

```html
    <p style="color: #333; line-height: 1.6;">This is my first paragraph. I'm learning HTML!</p>
```

6. Press **Ctrl + S** to save the file

### What to Notice

- **`style` attribute** - This is where you write CSS directly on an element
- **CSS syntax** - `property: value;` - Each style rule has a property (like `color`) and a value (like `blue`), separated by a colon, ending with a semicolon
- **Multiple properties** - You can add multiple properties separated by semicolons
- **Color values** - Colors can be names (`blue`) or hex codes (`#333` is dark gray)
- **Size values** - `2.5em` means 2.5 times the default size, `1.6` for line-height is a multiplier

**Preview the changes:** Open your page with Live Server and you should see the heading is blue and larger, and the paragraph has different styling.

### Verify Changes

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 5 commits.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   index.html
```

**If you see `index.html` listed as modified, proceed to Step 3.**

---

## Step 3: Create CSS Folder Structure (File Organization)

### What This Step Does

Following the file organization principles from Section 1, you'll create a proper folder structure for your CSS files. This implements logical grouping (CSS files together), scalable structure (easy to add more CSS files later), and self-explanatory organization. This is professional file organization that employers expect.

**Why organize files:**
- **Logical grouping** - CSS files belong together, not scattered
- **Scalable structure** - Easy to add more CSS files (like `reset.css`, `components.css`) later
- **Self-explanatory** - Anyone looking at your project knows where CSS files are
- **Professional** - This is how real projects are organized

### Instructions

1. In VS Code file explorer, look at your repository root (where `index.html` is)
2. **Right-click** in the empty space in the file explorer (not on any file)
3. Click **New Folder**
4. Type exactly: `css`
5. Press **Enter**

**Expected Result:** A new folder named `css` appears in your file explorer.

### Verify Folder Creation

1. In the VS Code terminal, type exactly:
   ```bash
   ls
   ```
2. Press **Enter**

**Expected Output:**
```
css  index.html  README.md
```

**You should see `css` listed as a folder/directory.**

**If you see the `css` folder, proceed to Step 4.**
**If not, make sure you created it in the repository root (same level as index.html).**

---

## Step 4: Create CSS File with Proper Naming

### What This Step Does

You'll create your first CSS file with a clear, self-explanatory name. Following naming conventions from Section 1, you'll use kebab-case (lowercase with hyphens) and a descriptive name. This file will contain all your CSS styles.

### Instructions

1. In VS Code file explorer, click on the `css` folder you just created
2. **Right-click** inside the `css` folder
3. Click **New File**
4. Type exactly: `styles.css`
5. Press **Enter**

**Expected Result:** A new file `styles.css` opens in the editor, and it appears in the `css` folder in file explorer.

### What to Notice

- **File name** - `styles.css` is clear and self-explanatory (it contains styles)
- **File extension** - `.css` tells the system this is a CSS file
- **Location** - The file is in the `css/` folder, following file organization principles
- **Naming convention** - Using kebab-case (`styles.css`, not `Styles.css` or `styles.CSS`)

**This implements file organization principles from Section 1:**
- Logical grouping (CSS files in css/ folder)
- Consistent naming (kebab-case)
- Self-explanatory names (styles.css clearly contains styles)
- Scalable structure (easy to add more CSS files to this folder)

### Verify File Creation

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 5 commits.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        css/

no changes added to commit (use "git add" or "git commit -a")
```

**You should see `css/` listed as an untracked directory. This is correct - Git detects the new folder.**

---

## Step 5: Add CSS to Your Stylesheet

### What This Step Does

You'll write CSS rules in your external stylesheet. This is the professional way to add CSS - all styles in one organized file, linked to your HTML. You'll add some basic styles to see how external CSS works.

### Instructions

1. In `css/styles.css` (the file you just created), type this CSS:

```css
/* Basic Typography */
h1 {
  color: blue;
  font-size: 2.5em;
}

p {
  color: #333;
  line-height: 1.6;
}

/* Navigation Styles */
.nav-link {
  color: #0066cc;
  text-decoration: none;
}

.nav-link:hover {
  color: #004499;
  text-decoration: underline;
}
```

2. Press **Ctrl + S** to save the file

### What to Notice

- **CSS comments** - `/* comment */` - Comments help organize and document your CSS
- **Element selectors** - `h1 { }` targets all `<h1>` elements
- **Class selectors** - `.nav-link { }` targets elements with `class="nav-link"` (the `.` means class)
- **Properties** - `color`, `font-size`, `line-height`, `text-decoration` are CSS properties
- **Values** - `blue`, `2.5em`, `1.6`, `#0066cc` are values
- **Hover pseudo-class** - `.nav-link:hover` applies styles when users hover over the link

**CSS Organization:** Notice the comments (`/* Basic Typography */`, `/* Navigation Styles */`). This is the beginning of organizing your CSS into logical sections.

### Verify File Was Saved

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should see both `index.html` and `css/` listed. This is correct.**

---

## Step 6: Link CSS File to HTML

### What This Step Does

External CSS files don't automatically apply to your HTML - you need to link them. You'll add a `<link>` tag in the `<head>` section of your HTML that tells the browser to load and apply your CSS file.

### Instructions

1. Open `index.html` in VS Code
2. Find the `<head>` section
3. Add this line **before** the closing `</head>` tag:

```html
    <link rel="stylesheet" href="css/styles.css">
```

4. **Remove the inline styles** you added in Step 2 (the `style` attributes from the `<h1>` and `<p>` tags)
5. Press **Ctrl + S** to save the file

### What to Notice

- **`<link>`** - This tag links external resources to your HTML
- **`rel="stylesheet"`** - This tells the browser this is a CSS stylesheet
- **`href="css/styles.css"`** - This is the path to your CSS file. It's a relative path (relative to the HTML file location)
- **Path structure** - `css/styles.css` means "go into the css folder, then find styles.css"

**Why remove inline styles:** Now that you have external CSS, the inline styles are redundant. External CSS is better because it's reusable, maintainable, and organized.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 5 commits.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        css/
```

**You should see both `index.html` modified and `css/` as untracked. This is correct.**

---

## Step 7: Preview Your Styled Page

### What This Step Does

Previewing lets you see how your CSS styles look in the browser. You'll verify that the external CSS file is loading correctly and applying styles to your page.

### Instructions

1. In VS Code file explorer, right-click on `index.html`
2. Click **Open with Live Server** (or refresh if already open)

**Expected Result:** Your browser should show the page with styles applied.

### Verify What You See

You should see:
- ✅ Heading is blue and larger (from CSS, not inline styles)
- ✅ Paragraphs have improved spacing and color
- ✅ Navigation links are styled (blue color, underline on hover)

**If styles are applied, proceed to Step 8.**
**If styles don't appear, check that:**
- The CSS file path in the `<link>` tag is correct: `css/styles.css`
- The CSS file is saved
- You're viewing the page with Live Server (not by opening the file directly)

---

## Step 8: Understand the CSS Box Model

### What This Step Does

The CSS box model is a fundamental concept that explains how spacing works in CSS. Every HTML element is a box with four areas: content, padding, border, and margin. Understanding this is essential for controlling spacing and layout.

**The Box Model:**
```
┌─────────────────────────┐
│      Margin             │  (space outside the border)
│  ┌───────────────────┐  │
│  │     Border         │  │  (border around the element)
│  │  ┌─────────────┐  │  │
│  │  │   Padding    │  │  │  (space inside the border)
│  │  │  ┌─────────┐ │  │  │
│  │  │  │ Content │ │  │  │  (the actual element content)
│  │  │  └─────────┘ │  │  │
│  │  └─────────────┘  │  │
│  └───────────────────┘  │
└─────────────────────────┘
```

**The four areas:**
- **Content** - The actual element content (text, images, etc.)
- **Padding** - Space inside the border, between content and border
- **Border** - The border around the element
- **Margin** - Space outside the border, between this element and other elements

**Why it matters:** When you set `width: 200px`, that's just the content width. The total space the element takes up includes padding, border, and margin. This affects layout and spacing.

### Add Box Model Example to CSS

1. In `css/styles.css`, add this at the end:

```css
/* Box Model Example */
section {
  padding: 20px;
  border: 2px solid #ccc;
  margin: 20px 0;
}
```

2. Press **Ctrl + S** to save

**What this does:**
- `padding: 20px` - Adds 20 pixels of space inside the border
- `border: 2px solid #ccc` - Adds a 2-pixel solid gray border
- `margin: 20px 0` - Adds 20 pixels of space above and below (0 on left/right)

**Preview:** Refresh your browser and you should see sections have spacing and borders around them.

---

## Step 9: Use Browser Developer Tools

### What This Step Does

Browser developer tools let you inspect your HTML and CSS, see which styles are applied, and understand the box model visually. This is an essential skill for debugging and learning how CSS works.

### Instructions

1. In your browser (with your page open), **right-click** on any element (like a heading or paragraph)
2. Click **Inspect** or **Inspect Element** (exact wording varies by browser)

**Expected Result:** Developer tools open, showing the HTML structure and CSS styles.

### What You Can See

- **Elements panel** - Shows the HTML structure
- **Styles panel** - Shows CSS rules applied to the selected element
- **Box model visualization** - Shows content, padding, border, and margin (if available)
- **Computed styles** - Shows final calculated styles after all CSS rules are applied

### Try This

1. **Select different elements** - Click on various elements in the HTML panel
2. **See applied styles** - Look at the Styles panel to see which CSS rules are active
3. **Modify styles** - Try changing values in the Styles panel (changes are temporary, just for learning)
4. **See box model** - Look for a box model diagram showing padding, border, margin

**This is how developers debug CSS:** Developer tools are essential for understanding why styles aren't applying, seeing the box model in action, and testing changes before committing them.

---

## Step 10: Commit Your Work

### What This Step Does

You've created a CSS file, set up proper file organization, and added styles to your page. Now you'll commit both the HTML changes and the new CSS file following professional habits.

### Safety Check Before Committing

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 5 commits.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        css/
```

**Verify:**
- ✅ You are on `main` branch
- ✅ `index.html` is modified (CSS link added, inline styles removed)
- ✅ `css/` folder is untracked (new CSS file)
- ✅ No unexpected files are listed

**If everything looks correct, proceed to staging.**
**If you see unexpected files, review your work before committing.**

### Stage Both Files

1. In the terminal, type exactly:
   ```bash
   git add index.html css/
   ```
2. Press **Enter**

**Expected Result:** No error message, prompt returns.

**Note:** `css/` stages the entire folder and all files in it. This is correct for adding new folders.

### Verify Files are Staged

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 5 commits.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
        new file:   css/styles.css
        modified:   index.html
```

**If you see both files under "Changes to be committed", proceed to commit.**

### Create the Commit

1. In the terminal, type exactly:
   ```bash
   git commit -m "s3: add CSS with organized file structure and box model"
   ```
2. Press **Enter**

**Expected Output:**
```
[main pqr7890] s3: add CSS with organized file structure and box model
 2 files changed, XX insertions(+), X deletions(-)
 create mode 100644 css/styles.css
```

**The commit hash (pqr7890) will be different - that's normal.**

### Verify Commit Success

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 6 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

**Key indicators:**
- ✅ "Your branch is ahead of 'origin/main' by 6 commits" - You now have 6 local commits
- ✅ "nothing to commit, working tree clean" - All changes are committed

**If you see this, your commit was successful. Proceed to final verification.**

---

## Expected Final State

After completing this exercise, you should have:

- ✅ `css/` folder created (proper file organization)
- ✅ `css/styles.css` file with CSS rules
- ✅ HTML file linked to CSS stylesheet
- ✅ Inline styles removed (using external CSS instead)
- ✅ Basic understanding of box model
- ✅ Experience with browser developer tools
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
Your branch is ahead of 'origin/main' by 6 commits.

nothing to commit, working tree clean
```

**If you see "working tree clean", you're ready for the next exercise.**

---

## What This Sets Up for Exercise 7

You now have CSS set up with proper file organization. In the next exercise, you'll learn more about CSS selectors (how to target elements) and understand CSS cascade and specificity (how browsers decide which styles to apply when multiple rules conflict).

---

## Troubleshooting

### Problem: CSS styles don't appear

**Solution:**
- Check the file path in the `<link>` tag: `href="css/styles.css"` (relative to HTML file location)
- Make sure the CSS file is saved (Ctrl + S)
- Verify the CSS file is in the `css/` folder, not the root
- Check browser console for errors (F12, then Console tab)
- Make sure you're viewing with Live Server, not opening file directly

### Problem: Can't create css folder

**Solution:**
- Make sure you're in the repository root (same level as index.html)
- Right-click in empty space in file explorer, not on a file
- Try creating it via terminal: `mkdir css` then `cd css` and create the file

### Problem: Developer tools don't open

**Solution:**
- Try different methods: Right-click → Inspect, or press F12, or Ctrl+Shift+I
- Different browsers have different shortcuts
- Make sure you're clicking on the webpage, not the browser chrome

---

## Next Steps

- [[c01-found/s3-html-css/index#Introduction to CSS|Return to Lecture]] - Go back to the Introduction to CSS section of the lecture before diving deeper into selectors.

---

## Navigation

**Previous Exercise:** [[s3-html-css/s3e5-using-semantic-html-structure|Exercise 5: Using Semantic HTML Structure]]

**Next Exercise:** [[s3-html-css/s3e7-css-selectors|Exercise 7: CSS Selectors]]

**Home:** [[index|Main Course Page]]

**Return to Section:** [[s3-html-css/index|HTML & CSS Section]]
