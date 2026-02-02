---
title: "Exercise 9: CSS Layout with Float"
description: "Learn CSS layout using float, display properties, and responsive design. Test layouts with developer tools."
tags: [css, layout, float, responsive-design, display, beginner, workbook]
draft: false
date: "2026-01-30"
---

# Exercise 9: CSS Layout with Float

**This exercise continues from Exercise 8. You must complete Exercise 8 first.**

**This exercise is a standalone technical manual. Follow each step exactly.**

**Time Required:** 30-35 minutes

---

## Prerequisites Check

Before starting, verify:

1. ✅ **Exercise 8 completed**
   - CSS file is organized with sections and comments
   - Page has styling for text, borders, backgrounds, and forms
   - All changes from Exercise 8 are committed

2. ✅ **Current State Verification**
   - Open VS Code terminal (Ctrl + ~)
   - Type: `git status`
   - Press Enter

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 8 commits.

nothing to commit, working tree clean
```

**If you see this, proceed.**
**If not, complete Exercise 8 first or resolve any uncommitted changes.**

---

## What You Will Accomplish

By the end of this exercise, you will have:

- Understood CSS display properties (block, inline, inline-block)
- Used float for page layout
- Created a two-column layout
- Learned responsive design basics (viewport, media queries)
- Tested layouts with developer tools
- Committed your work with Git

---

## Step 1: Understand Display Properties

### What This Step Does

Every HTML element has a display property that determines how it behaves in the layout. Understanding display properties is essential for controlling how elements are positioned and how they interact with other elements.

**Common display values:**
- **`block`** - Element takes full width, stacks vertically (like `<div>`, `<p>`, `<section>`)
- **`inline`** - Element flows horizontally, respects content width (like `<span>`, `<a>`, `<strong>`)
- **`inline-block`** - Combines block and inline: flows horizontally but respects width/height
- **`none`** - Element is hidden completely
- **`flex`** - Modern layout method (you'll learn this in advanced courses)

**Why it matters:** Display properties control the fundamental layout behavior. Changing display can completely change how elements are positioned.

---

## Step 2: Add Display Properties to CSS

### What This Step Does

You'll add display properties to see how they affect element layout. This demonstrates the difference between block, inline, and inline-block elements.

### Instructions

1. Open `css/styles.css` in VS Code
2. Add a new section for display properties:

```css
/* ========================================
   DISPLAY PROPERTIES
   ======================================== */
header, main, section, footer {
  display: block;  /* Default for these elements */
}

.nav-link {
  display: inline-block;  /* Allows padding and width while staying inline */
}

img {
  display: block;  /* Prevents inline spacing issues */
  max-width: 100%;  /* Makes images responsive */
  height: auto;
}
```

3. Press **Ctrl + S** to save the file

### What to Notice

- **`display: block`** - These elements already default to block, but explicitly setting it is good practice
- **`display: inline-block`** - Navigation links can have padding and width while staying in a horizontal line
- **`display: block` on images** - Prevents weird spacing that sometimes happens with inline images
- **`max-width: 100%`** - Makes images responsive (they won't overflow their container)

**Preview:** Refresh your browser. Images should display better, and navigation should work smoothly.

### Verify Changes

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 8 commits.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   css/styles.css
```

**If you see `css/styles.css` listed as modified, proceed to Step 3.**

---

## Step 3: Create a Two-Column Layout with Float

### What This Step Does

Float is a CSS property that moves elements to the left or right, allowing other content to wrap around them. While modern CSS uses Flexbox and Grid, understanding float is important because it's in the source material and you'll encounter it in legacy code. You'll create a simple two-column layout.

### Instructions

1. In your HTML file (`index.html`), find your main content section
2. Add a wrapper div around your sections to create a layout structure. Update your main content like this:

```html
  <main id="main-content">
    <div class="content-wrapper">
      <div class="main-column">
        <section id="about">
          <!-- Your about content here -->
        </section>
        
        <section id="schedule">
          <!-- Your schedule/table content here -->
        </section>
      </div>
      
      <aside class="sidebar">
        <h3>Quick Links</h3>
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#schedule">Schedule</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </aside>
    </div>
    
    <section id="contact">
      <!-- Your contact form here -->
    </section>
  </main>
```

3. In `css/styles.css`, add layout styles:

```css
/* ========================================
   LAYOUT WITH FLOAT
   ======================================== */
.content-wrapper {
  overflow: hidden;  /* Contains floated elements */
}

.main-column {
  float: left;
  width: 70%;
  padding-right: 20px;
  box-sizing: border-box;
}

.sidebar {
  float: right;
  width: 30%;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 5px;
  box-sizing: border-box;
}

.sidebar ul {
  list-style: none;
  padding: 0;
}

.sidebar li {
  margin-bottom: 10px;
}

.sidebar a {
  color: #0066cc;
  text-decoration: none;
}

.sidebar a:hover {
  text-decoration: underline;
}
```

4. Press **Ctrl + S** to save both files

### What to Notice

- **`float: left`** - Moves element to the left, content flows to the right
- **`float: right`** - Moves element to the right, content flows to the left
- **`width: 70%` and `30%`** - Percentages create flexible layouts (adds up to 100%)
- **`overflow: hidden`** - Contains floated elements (prevents layout issues)
- **`box-sizing: border-box`** - Includes padding in width calculation (prevents overflow)

**How float works:** Floated elements are taken out of normal flow and positioned to the left or right. Other content wraps around them.

**Preview:** Refresh your browser. You should see a two-column layout with main content on the left and sidebar on the right.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 8 commits.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   css/styles.css
        modified:   index.html
```

**You should see both files modified. This is correct.**

---

## Step 4: Clear Floats

### What This Step Does

When you use float, you often need to "clear" floats to prevent layout issues. Elements after floated elements can sometimes wrap incorrectly. You'll add clearfix to ensure proper layout.

### Instructions

1. In `css/styles.css`, update the layout section:

```css
/* Clear floats */
.content-wrapper::after {
  content: "";
  display: table;
  clear: both;
}

#contact {
  clear: both;  /* Ensures contact section appears below floated elements */
  margin-top: 40px;
}
```

2. Press **Ctrl + S** to save the file

### What to Notice

- **`clear: both`** - Clears floats on both left and right sides
- **`::after` pseudo-element** - Creates an invisible element after the content-wrapper
- **Clearfix pattern** - This is a common technique to contain floated elements

**Why clear floats:** Without clearing, elements after floated content can behave unexpectedly. Clearing ensures proper layout flow.

**Preview:** Refresh your browser. The contact section should appear below the two-column layout, not beside it.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see both files as modified. This is correct.**

---

## Step 5: Understand Responsive Design

### What This Step Does

Responsive design makes web pages work on all screen sizes - from large desktop monitors to small mobile phones. You already added the viewport meta tag in Exercise 1, which is the foundation. Now you'll add media queries to adjust styles for different screen sizes.

**Responsive design basics:**
- **Viewport meta tag** - Already added in Exercise 1, tells mobile browsers to use device width
- **Media queries** - Apply different CSS rules at different screen sizes
- **Flexible units** - Use percentages, `em`, `rem` instead of fixed `px` when possible
- **Max-width** - Prevent elements from getting too wide

**Why it matters:** More people browse on mobile devices than desktop. Responsive design ensures your site works for everyone.

---

## Step 6: Add Media Queries for Responsive Design

### What This Step Does

You'll add media queries that change your layout for smaller screens. On mobile devices, the two-column layout should stack vertically instead of side-by-side. This is a basic responsive design pattern.

### Instructions

1. In `css/styles.css`, add a new section at the end for media queries:

```css
/* ========================================
   RESPONSIVE DESIGN
   ======================================== */
/* For screens smaller than 768px (tablets and phones) */
@media (max-width: 768px) {
  .main-column {
    float: none;
    width: 100%;
    padding-right: 0;
  }
  
  .sidebar {
    float: none;
    width: 100%;
    margin-top: 20px;
  }
  
  #main-content {
    padding: 15px;
  }
  
  h1 {
    font-size: 2em;  /* Smaller heading on mobile */
  }
  
  nav ul {
    flex-direction: column;  /* Stack navigation vertically */
  }
  
  nav li {
    margin-right: 0;
    margin-bottom: 10px;
  }
}
```

2. Press **Ctrl + S** to save the file

### What to Notice

- **`@media (max-width: 768px)`** - This media query applies styles when screen width is 768px or less
- **`float: none`** - Removes float on small screens, elements stack vertically
- **`width: 100%`** - Full width on small screens (no side-by-side layout)
- **Flexible layout** - Layout adapts to screen size

**How it works:** When the browser window is 768px or narrower, the media query styles apply, overriding the default styles. This creates a mobile-friendly layout.

**Preview:** Refresh your browser and resize the window (make it narrower). At 768px and below, the layout should stack vertically.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see both files as modified. This is correct.**

---

## Step 7: Test Responsive Design with Developer Tools

### What This Step Does

Developer tools have a responsive design mode that lets you test how your page looks on different screen sizes. This is essential for ensuring your responsive design works correctly.

### Instructions

1. Open your page in the browser with Live Server
2. Open developer tools (F12 or right-click → Inspect)
3. Look for the **responsive design mode** icon (usually looks like a phone/tablet, or press Ctrl+Shift+M)

**Expected Result:** Developer tools enter responsive design mode, showing your page at a mobile size.

### What You Can Do

- **Select device presets** - Choose iPhone, iPad, etc. to see common screen sizes
- **Adjust width/height** - Manually resize to test different breakpoints
- **Rotate device** - Test portrait and landscape orientations
- **See actual size** - View how your page looks on real devices

### Test Your Media Query

1. **Start at desktop size** - Your two-column layout should be visible
2. **Resize to 768px or less** - The layout should change to stacked (single column)
3. **Check navigation** - Should stack vertically on mobile
4. **Verify spacing** - Padding and margins should adjust for mobile

**This is how developers test responsive design:** Developer tools let you test multiple screen sizes quickly without needing actual devices.

---

## Step 8: Review Viewport Meta Tag

### What This Step Does

You'll verify that the viewport meta tag is in your HTML (you added it in Exercise 1). This tag is essential for responsive design - without it, mobile browsers assume desktop width and zoom out, making pages hard to use.

### Instructions

1. Open `index.html` in VS Code
2. Check the `<head>` section
3. Verify you have this line:

```html
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
```

**If the viewport tag is present, you're good.**
**If it's missing, add it to the `<head>` section.**

### What the Viewport Tag Does

- **`width=device-width`** - Tells mobile browsers to use the device width (not desktop width)
- **`initial-scale=1.0`** - Sets initial zoom level to 100% (no zoom)
- **Why it matters** - Without this, mobile browsers zoom out to show desktop layout, making text tiny and requiring users to zoom in

**This is the foundation of responsive design:** The viewport meta tag makes everything else possible.

---

## Step 9: Commit Your Work

### What This Step Does

You've added layout with float, responsive design with media queries, and tested with developer tools. Now you'll commit these changes following professional habits.

### Safety Check Before Committing

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 8 commits.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   css/styles.css
        modified:   index.html

no changes added to commit (use "git add" or "git commit -a")
```

**Verify:**
- ✅ You are on `main` branch
- ✅ Both `index.html` and `css/styles.css` are modified
- ✅ No unexpected files are listed

**If everything looks correct, proceed to staging.**
**If you see unexpected files, review your work before committing.**

### Stage Both Files

1. In the terminal, type exactly:
   ```bash
   git add index.html css/styles.css
   ```
2. Press **Enter**

**Expected Result:** No error message, prompt returns.

### Verify Files are Staged

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 8 commits.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
        modified:   css/styles.css
        modified:   index.html
```

**If you see both files under "Changes to be committed", proceed to commit.**

### Create the Commit

1. In the terminal, type exactly:
   ```bash
   git commit -m "s3: add CSS layout with float and responsive design"
   ```
2. Press **Enter**

**Expected Output:**
```
[main yza1234] s3: add CSS layout with float and responsive design
 2 files changed, XX insertions(+), X deletions(-)
```

**The commit hash (yza1234) will be different - that's normal.**

### Verify Commit Success

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 9 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

**Key indicators:**
- ✅ "Your branch is ahead of 'origin/main' by 9 commits" - You now have 9 local commits
- ✅ "nothing to commit, working tree clean" - All changes are committed

**If you see this, your commit was successful. Proceed to final verification.**

---

## Expected Final State

After completing this exercise, you should have:

- ✅ Understanding of display properties (block, inline, inline-block)
- ✅ Two-column layout created with float
- ✅ Responsive design with media queries
- ✅ Viewport meta tag verified in HTML
- ✅ Experience testing layouts with developer tools
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
Your branch is ahead of 'origin/main' by 9 commits.

nothing to commit, working tree clean
```

**If you see "working tree clean", you're ready for the final exercise - the capstone project!**

---

## What This Sets Up for Exercise 10

You now have a complete understanding of HTML structure, CSS styling, and layout. In the final exercise, you'll build a complete Client Meeting Scheduler project that combines all the concepts you've learned. This will be a portfolio-ready project that demonstrates your HTML and CSS skills.

---

## Troubleshooting

### Problem: Two-column layout doesn't work

**Solution:**
- Check that widths add up to 100% (70% + 30% = 100%)
- Verify `box-sizing: border-box` is set (includes padding in width)
- Make sure `overflow: hidden` is on the container
- Check that elements are actually floated (`float: left` and `float: right`)

### Problem: Layout breaks on mobile

**Solution:**
- Verify media query syntax is correct: `@media (max-width: 768px)`
- Check that media query styles override float (use `float: none`)
- Make sure widths are 100% in media query
- Test in developer tools responsive mode

### Problem: Elements overlap or don't clear properly

**Solution:**
- Add `clear: both` to elements that should appear below floats
- Use the clearfix pattern (`::after` with `clear: both`)
- Check that container has `overflow: hidden` or clearfix

### Problem: Media query doesn't apply

**Solution:**
- Check syntax: `@media (max-width: 768px)` (not `max-width:` with colon in wrong place)
- Verify viewport meta tag is in HTML
- Test by resizing browser window
- Check browser console for CSS errors

---

## Navigation

**Previous Exercise:** [[s3-html-css/s3e8-css-styling-fundamentals|Exercise 8: CSS Styling Fundamentals]]

**Next Exercise:** [[s3-html-css/s3e10-capstone-client-meeting-scheduler|Exercise 10: Capstone Project - Client Meeting Scheduler]]

**Home:** [[index|Main Course Page]]

**Return to Section:** [[s3-html-css/index|HTML & CSS Section]]

---

## Next Steps

- [[c01-found/s3-html-css/index#CSS Layout and Responsive Design|Return to Lecture]] - Go back to the CSS Layout and Responsive Design section of the lecture before starting the capstone.
