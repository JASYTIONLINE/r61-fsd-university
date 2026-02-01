---
title: "Exercise 8: CSS Styling Fundamentals"
description: "Learn CSS styling properties for text, borders, and backgrounds. Practice the box model and organize CSS with comments and sections."
tags: [css, styling, box-model, organization, beginner, workbook]
draft: false
date: "2026-01-30"
---

# Exercise 8: CSS Styling Fundamentals

**This exercise continues from Exercise 7. You must complete Exercise 7 first.**

**This exercise is a standalone technical manual. Follow each step exactly.**

**Time Required:** 30-35 minutes

---

## Prerequisites Check

Before starting, verify:

1. ✅ **Exercise 7 completed**
   - CSS file has various selectors
   - You understand cascade and specificity
   - All changes from Exercise 7 are committed

2. ✅ **Current State Verification**
   - Open VS Code terminal (Ctrl + ~)
   - Type: `git status`
   - Press Enter

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 7 commits.

nothing to commit, working tree clean
```

**If you see this, proceed.**
**If not, complete Exercise 7 first or resolve any uncommitted changes.**

---

## What You Will Accomplish

By the end of this exercise, you will have:

- Styled text with font properties, colors, and alignment
- Added borders and backgrounds to elements
- Practiced the box model with padding, margin, and border
- Styled form elements for better user experience
- Organized CSS with comments and logical sections
- Committed your work with Git

---

## Step 1: Organize CSS with Comments and Sections

### What This Step Does

Before adding more styles, you'll organize your existing CSS with comments and logical sections. This implements file organization principles from Section 1: logical grouping, maintainability, and self-documenting code. Well-organized CSS is easier to read, maintain, and update.

**Why organize CSS:**
- **Logical grouping** - Related styles are together
- **Easy to find** - Comments help locate specific styles
- **Maintainable** - Clear structure makes updates easier
- **Professional** - This is how real projects are organized

### Instructions

1. Open `css/styles.css` in VS Code
2. Reorganize your CSS with section comments. Structure it like this:

```css
/* ========================================
   RESET & BASE STYLES
   ======================================== */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

/* ========================================
   TYPOGRAPHY
   ======================================== */
h1 {
  color: blue;
  font-size: 2.5em;
}

h2 {
  color: #0066cc;
  border-bottom: 2px solid #0066cc;
  padding-bottom: 10px;
}

h1, h2, h3 {
  margin-top: 0;
}

p {
  color: #333;
  line-height: 1.6;
}

section p {
  margin-bottom: 15px;
}

/* ========================================
   LAYOUT & STRUCTURE
   ======================================== */
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

section {
  padding: 20px;
  border: 2px solid #ccc;
  margin: 20px 0;
}

footer {
  background-color: #f5f5f5;
  padding: 20px;
  text-align: center;
  margin-top: 40px;
}

#page-footer {
  border-top: 1px solid #ccc;
}

/* ========================================
   NAVIGATION
   ======================================== */
nav ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
}

nav li {
  margin-right: 20px;
}

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

/* ========================================
   FORMS
   ======================================== */
.form-input {
  width: 100%;
  padding: 10px;
  margin: 5px 0;
  border: 1px solid #ccc;
  border-radius: 4px;
  font-family: Arial, sans-serif;
  font-size: 16px;
}

input[type="text"],
input[type="email"],
input[type="tel"],
textarea {
  font-family: Arial, sans-serif;
  font-size: 16px;
}

/* ========================================
   FOOTER
   ======================================== */
footer p {
  margin: 5px 0;
  font-size: 0.9em;
  color: #666;
}
```

3. Press **Ctrl + S** to save the file

### What to Notice

- **Section comments** - `/* ======================================== */` creates clear visual separators
- **Logical grouping** - Related styles are grouped together (Typography, Layout, Navigation, Forms)
- **Easy navigation** - You can quickly find styles by looking for section comments
- **Maintainable** - When you need to update navigation styles, you know exactly where to look

**This implements file organization principles:**
- Logical grouping (related styles together)
- Self-documenting (comments explain what each section does)
- Scalable (easy to add new sections as project grows)

### Verify Changes

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 7 commits.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   css/styles.css
```

**If you see `css/styles.css` listed as modified, proceed to Step 2.**

---

## Step 2: Add Advanced Text Styling

### What This Step Does

You'll add more text styling properties to make your typography more polished. This includes font weight, text alignment, text decoration, and text transformation. These properties give you fine control over how text appears.

### Instructions

1. In `css/styles.css`, find the TYPOGRAPHY section
2. Add these advanced text styling rules:

```css
/* Advanced Text Styling */
h1 {
  font-weight: bold;
  text-align: center;
  letter-spacing: 2px;
}

h2 {
  font-weight: 600;
  text-transform: uppercase;
}

p {
  text-align: left;
  word-spacing: 1px;
}

.intro {
  font-size: 1.1em;
  font-style: italic;
  color: #555;
}

strong {
  font-weight: bold;
  color: #0066cc;
}

em {
  font-style: italic;
}
```

3. Press **Ctrl + S** to save the file

### What to Notice

- **`font-weight`** - Controls how bold text is (`normal`, `bold`, or numbers like `400`, `600`, `700`)
- **`text-align`** - Controls horizontal alignment (`left`, `center`, `right`, `justify`)
- **`text-transform`** - Changes text case (`uppercase`, `lowercase`, `capitalize`)
- **`letter-spacing`** - Space between individual letters
- **`word-spacing`** - Space between words
- **`font-style`** - `italic` or `normal`
- **`font-size`** - Size of text (can use `em`, `px`, `rem`, `%`)

**Preview:** Refresh your browser. Headings should be more styled, and text should have better typography.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see `css/styles.css` as modified. This is correct.**

---

## Step 3: Add Borders and Backgrounds

### What This Step Does

Borders and backgrounds add visual interest and help separate content areas. You'll add various border styles and background colors/images to see how they work. Understanding borders is also important for the box model.

### Instructions

1. In `css/styles.css`, add a new section for borders and backgrounds:

```css
/* ========================================
   BORDERS & BACKGROUNDS
   ======================================== */
section {
  background-color: #fafafa;
  border-left: 4px solid #0066cc;
  border-radius: 5px;
}

#page-header {
  background: linear-gradient(to bottom, #0066cc, #004499);
  border-bottom: 3px solid #003366;
}

footer {
  background-color: #f5f5f5;
  border-top: 2px solid #ddd;
}

button[type="submit"] {
  background-color: #0066cc;
  color: white;
  border: none;
  border-radius: 4px;
  padding: 12px 24px;
  cursor: pointer;
  font-size: 16px;
}

button[type="submit"]:hover {
  background-color: #004499;
}
```

2. Press **Ctrl + S** to save the file

### What to Notice

- **`background-color`** - Solid color background
- **`background`** - Can use gradients: `linear-gradient(direction, color1, color2)`
- **`border`** - Shorthand: `width style color` (like `2px solid #ccc`)
- **`border-left`** - Border on one side only
- **`border-radius`** - Rounded corners (higher values = more rounded)
- **`border: none`** - Removes default button border
- **`:hover`** - Styles applied when user hovers over element

**Preview:** Refresh your browser. Sections should have light backgrounds and blue left borders, header should have a gradient, and submit button should be styled.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see `css/styles.css` as modified. This is correct.**

---

## Step 4: Practice Box Model with Padding and Margin

### What This Step Does

You'll practice the box model by adjusting padding and margin on various elements. This reinforces your understanding of how spacing works in CSS. Padding creates space inside the border, margin creates space outside the border.

### Instructions

1. In `css/styles.css`, update the LAYOUT & STRUCTURE section to practice box model:

```css
/* Box Model Practice */
#main-content {
  max-width: 800px;
  margin: 0 auto;  /* Centers the element */
  padding: 30px;  /* Space inside */
  background-color: white;
  border: 1px solid #ddd;
  border-radius: 8px;
}

section {
  padding: 25px;  /* Space inside border */
  margin: 30px 0;  /* Space outside border (top and bottom) */
  border-left: 4px solid #0066cc;
  background-color: #fafafa;
  border-radius: 5px;
}

.form-input {
  padding: 12px;  /* Space inside input */
  margin: 8px 0;  /* Space outside input */
  border: 1px solid #ccc;
  border-radius: 4px;
}

button[type="submit"] {
  padding: 12px 24px;  /* 12px top/bottom, 24px left/right */
  margin-top: 10px;  /* Space above button */
}
```

2. Press **Ctrl + S** to save the file

### What to Notice

- **Padding** - Space inside the border. Makes content area larger.
- **Margin** - Space outside the border. Creates space between elements.
- **Shorthand values** - `padding: 12px 24px` means 12px top/bottom, 24px left/right
- **`margin: 0 auto`** - 0 top/bottom, auto left/right (centers block elements)
- **Box model visualization** - In developer tools, you can see padding, border, and margin visually

**Visual understanding:** 
- Content is in the center
- Padding is inside the border (space between content and border)
- Border is the line around the element
- Margin is outside the border (space between this element and others)

**Preview:** Refresh your browser. Elements should have better spacing and visual separation.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see `css/styles.css` as modified. This is correct.**

---

## Step 5: Style Form Elements

### What This Step Does

You'll improve the styling of form elements to make them more visually appealing and user-friendly. Good form styling improves the user experience and makes forms easier to use.

### Instructions

1. In `css/styles.css`, expand the FORMS section:

```css
/* ========================================
   FORMS
   ======================================== */
form {
  background-color: #f9f9f9;
  padding: 25px;
  border-radius: 8px;
  border: 1px solid #ddd;
  margin: 20px 0;
}

label {
  display: block;
  margin-top: 15px;
  margin-bottom: 5px;
  font-weight: 600;
  color: #333;
}

.form-input,
input[type="text"],
input[type="email"],
input[type="tel"],
textarea {
  width: 100%;
  padding: 12px;
  margin: 5px 0 15px 0;
  border: 1px solid #ccc;
  border-radius: 4px;
  font-family: Arial, sans-serif;
  font-size: 16px;
  box-sizing: border-box;  /* Includes padding and border in width */
}

.form-input:focus,
input:focus,
textarea:focus {
  outline: none;
  border-color: #0066cc;
  box-shadow: 0 0 5px rgba(0, 102, 204, 0.3);
}

select {
  width: 100%;
  padding: 12px;
  margin: 5px 0 15px 0;
  border: 1px solid #ccc;
  border-radius: 4px;
  font-family: Arial, sans-serif;
  font-size: 16px;
  background-color: white;
}

button[type="submit"] {
  background-color: #0066cc;
  color: white;
  border: none;
  border-radius: 4px;
  padding: 12px 24px;
  margin-top: 10px;
  cursor: pointer;
  font-size: 16px;
  font-weight: 600;
  transition: background-color 0.3s;
}

button[type="submit"]:hover {
  background-color: #004499;
}

button[type="submit"]:active {
  background-color: #003366;
}
```

2. Press **Ctrl + S** to save the file

### What to Notice

- **`:focus`** - Styles applied when input is focused (user clicks in it)
- **`box-shadow`** - Creates a shadow effect (useful for focus states)
- **`box-sizing: border-box`** - Makes width include padding and border (prevents overflow)
- **`transition`** - Smoothly animates property changes (like color on hover)
- **`:active`** - Styles applied when button is being clicked
- **`display: block`** - Makes labels appear on their own line

**User experience improvements:** Focus states help users see which field they're in, transitions make interactions feel smooth, and consistent styling makes forms easier to use.

**Preview:** Refresh your browser. Forms should look much more polished with better spacing, focus effects, and styled buttons.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see `css/styles.css` as modified. This is correct.**

---

## Step 6: Preview Your Styled Page

### What This Step Does

Previewing lets you see all your styling work together. You'll verify that text styling, borders, backgrounds, box model spacing, and form styling all work correctly and look good.

### Instructions

1. In VS Code file explorer, right-click on `index.html`
2. Click **Open with Live Server** (or refresh if already open)

**Expected Result:** Your browser should show a fully styled page.

### Verify What You See

You should see:
- ✅ Styled typography (headings, paragraphs with proper spacing)
- ✅ Sections with backgrounds, borders, and rounded corners
- ✅ Navigation with hover effects
- ✅ Form with styled inputs, focus states, and button
- ✅ Footer with proper styling
- ✅ Good spacing throughout (box model in action)
- ✅ Professional, polished appearance

**If everything looks good, proceed to Step 7.**
**If something doesn't look right, check that you saved the CSS file and refresh the browser.**

---

## Step 7: Use Developer Tools to See Box Model

### What This Step Does

You'll use developer tools to visually see the box model in action. This reinforces your understanding of padding, border, and margin, and shows you how the browser calculates element sizes.

### Instructions

1. In your browser, **right-click** on any element (like a section or form)
2. Click **Inspect** or **Inspect Element**
3. In developer tools, look for the **Box Model** visualization (usually in the Styles or Computed panel)

### What You Can See

- **Content** - The actual element content
- **Padding** - Visual representation of padding space
- **Border** - The border around the element
- **Margin** - Visual representation of margin space
- **Dimensions** - Total width and height including all box model areas

### Try This

1. **Select different elements** - Click on sections, forms, buttons
2. **See box model** - Look at the visual representation of padding, border, margin
3. **Modify values** - Try changing padding or margin values in developer tools (temporary, just for learning)
4. **See calculations** - Notice how total width = content + padding + border + margin

**This visual understanding helps:** When spacing isn't right, you can see exactly which part of the box model is causing the issue.

---

## Step 8: Commit Your Work

### What This Step Does

You've added extensive styling, organized your CSS with comments and sections, and practiced the box model. Now you'll commit this change following professional habits.

### Safety Check Before Committing

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 7 commits.

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
Your branch is ahead of 'origin/main' by 7 commits.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
        modified:   css/styles.css
```

**If you see `css/styles.css` under "Changes to be committed", proceed to commit.**

### Create the Commit

1. In the terminal, type exactly:
   ```bash
   git commit -m "s3: add CSS styling with organized sections and box model practice"
   ```
2. Press **Enter**

**Expected Output:**
```
[main vwx8901] s3: add CSS styling with organized sections and box model practice
 1 file changed, XX insertions(+), X deletions(-)
```

**The commit hash (vwx8901) will be different - that's normal.**

### Verify Commit Success

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 8 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

**Key indicators:**
- ✅ "Your branch is ahead of 'origin/main' by 8 commits" - You now have 8 local commits
- ✅ "nothing to commit, working tree clean" - All changes are committed

**If you see this, your commit was successful. Proceed to final verification.**

---

## Expected Final State

After completing this exercise, you should have:

- ✅ CSS organized with comments and logical sections
- ✅ Advanced text styling (font properties, alignment, spacing)
- ✅ Borders and backgrounds on elements
- ✅ Box model practice (padding, margin, border)
- ✅ Styled form elements with focus states
- ✅ Understanding of how box model works visually
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
Your branch is ahead of 'origin/main' by 8 commits.

nothing to commit, working tree clean
```

**If you see "working tree clean", you're ready for the next exercise.**

---

## What This Sets Up for Exercise 9

You now have a well-styled page with organized CSS. In the next exercise, you'll learn about CSS layout using float, display properties, and responsive design basics. You'll create page layouts and test them with developer tools.

---

## Troubleshooting

### Problem: Box model spacing doesn't look right

**Solution:**
- Check `box-sizing` property - `border-box` includes padding and border in width
- Use developer tools to see actual padding, border, and margin values
- Remember: margin is outside border, padding is inside border
- Check for conflicting margin/padding rules

### Problem: Form inputs overflow container

**Solution:**
- Add `box-sizing: border-box` to inputs (includes padding in width)
- Check that `width: 100%` doesn't conflict with padding
- Use developer tools to see calculated width

### Problem: CSS organization is messy

**Solution:**
- Use section comments to separate logical groups
- Group related styles together (all typography, all forms, etc.)
- Keep sections in logical order (base styles first, then specific styles)
- Add comments for complex or non-obvious rules

---

## Navigation

**Previous Exercise:** [[s3-html-css/s3e7-css-selectors|Exercise 7: CSS Selectors]]

**Next Exercise:** [[s3-html-css/s3e9-css-layout-with-float|Exercise 9: CSS Layout with Float]]

**Home:** [[index 1|Main Course Page]]

**Return to Section:** [[s3-html-css/index|HTML & CSS Section]]
