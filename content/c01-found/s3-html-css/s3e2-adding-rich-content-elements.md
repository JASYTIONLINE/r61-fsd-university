---
title: "Exercise 2: Adding Rich Content Elements"
description: "Add hyperlinks, lists, images, and embedded content to your webpage. Learn about accessibility and proper HTML attributes."
tags: [html, links, lists, images, accessibility, beginner, workbook]
draft: false
date: "2026-01-30"
---

# Exercise 2: Adding Rich Content Elements

**This exercise continues from Exercise 1. You must complete Exercise 1 first.**

**This exercise is a standalone technical manual. Follow each step exactly.**

**Time Required:** 25-30 minutes

---

## Prerequisites Check

Before starting, verify:

1. ✅ **Exercise 1 completed**
   - `index.html` file exists with proper HTML structure
   - Live Server extension is installed
   - You can preview your page in a browser
   - All changes from Exercise 1 are committed

2. ✅ **Current State Verification**
   - Open VS Code terminal (Ctrl + ~)
   - Type: `git status`
   - Press Enter

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 1 commit.

nothing to commit, working tree clean
```

**If you see this, proceed.**
**If not, complete Exercise 1 first or resolve any uncommitted changes.**

---

## What You Will Accomplish

By the end of this exercise, you will have:

- Added hyperlinks (internal, external, and anchor links) to your page
- Created ordered and unordered lists
- Added images with proper alt text for accessibility
- Embedded external content using iframes
- Learned about HTML attributes and accessibility
- Committed your work with Git

---

## Step 1: Add Hyperlinks to Your Page

### What This Step Does

Hyperlinks (also called links) allow users to navigate to other pages or sections. Links are what make the web interconnected. You'll add three types of links: external links (to other websites), internal links (to other pages on your site), and anchor links (to sections on the same page).

### Instructions

1. Open `index.html` in VS Code
2. Find the second paragraph (the one that says "This is my second paragraph...")
3. Replace that entire paragraph with this code:

```html
<p>This is my second paragraph. HTML is the structure of web pages.</p>
<p>Visit <a href="https://www.example.com">Example Website</a> to learn more.</p>
<p>You can also check out <a href="about.html">our about page</a> (we'll create this later).</p>
<p>Jump to <a href="#contact">contact information</a> at the bottom of this page.</p>
```

4. Press **Ctrl + S** to save the file

### What to Notice

- **`<a href="url">`** - This is the anchor tag that creates a link. The `href` attribute (short for "hypertext reference") tells the browser where to go when the link is clicked.
- **External links** - `href="https://www.example.com"` links to another website. Always include `https://` for external links.
- **Internal links** - `href="about.html"` links to another page in your site. This is a relative path (relative to the current file).
- **Anchor links** - `href="#contact"` links to an element with `id="contact"` on the same page. The `#` tells the browser to look for an ID on the current page.

### Verify Changes

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 1 commit.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   index.html
```

**If you see `index.html` listed as modified, proceed to Step 2.**

---

## Step 2: Add Lists to Your Page

### What This Step Does

Lists organize information in an easy-to-read format. You'll create both an unordered list (bulleted) and an ordered list (numbered). Lists are great for navigation menus, feature lists, step-by-step instructions, and any information that benefits from being organized in items.

### Instructions

1. In `index.html`, find the closing `</body>` tag (the last line)
2. Add this code **before** the `</body>` tag:

```html
<h2>Things I'm Learning</h2>
<ul>
  <li>HTML structure</li>
  <li>Adding links</li>
  <li>Creating lists</li>
  <li>Adding images</li>
</ul>

<h2>Steps to Build a Webpage</h2>
<ol>
  <li>Create the HTML structure</li>
  <li>Add content elements</li>
  <li>Style with CSS</li>
  <li>Test in browser</li>
</ol>
```

3. Press **Ctrl + S** to save the file

### What to Notice

- **`<h2>`** - This is a second-level heading. It's smaller than `<h1>` but larger than regular text. Headings create hierarchy in your document.
- **`<ul>`** - Unordered list. Creates a bulleted list. Use this when the order doesn't matter.
- **`<ol>`** - Ordered list. Creates a numbered list. Use this when the order matters (like steps).
- **`<li>`** - List item. Each `<li>` is one item in the list. You can have as many as you need.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should see `index.html` still listed as modified. This is correct - you're building up changes before committing.**

---

## Step 3: Add Images to Your Page

### What This Step Does

Images make web pages more engaging and informative. You'll add an image to your page. For this exercise, you can use a placeholder image service, but in real projects, you'd use your own image files. Most importantly, you'll learn about the `alt` attribute, which is essential for accessibility.

### Instructions

1. In `index.html`, find the first paragraph (after the `<h1>`)
2. Add this code **after** the first paragraph:

```html
<img src="https://via.placeholder.com/400x200" alt="A placeholder image showing 400 by 200 pixels">
```

3. Press **Ctrl + S** to save the file

### What to Notice

- **`<img>`** - This is a self-closing tag (no closing tag needed). It displays an image.
- **`src` attribute** - This tells the browser where to find the image. It can be a URL (like we're using) or a path to a file (like `images/photo.jpg`).
- **`alt` attribute** - This is **required** for accessibility. It provides text that describes the image. Screen readers use this text to tell visually impaired users what the image shows. If the image fails to load, browsers also display this text. Always include descriptive alt text.

**Accessibility Note:** The `alt` attribute is not optional. Every image must have alt text. If an image is purely decorative and adds no information, you can use `alt=""` (empty string), but most images should have descriptive text.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see `index.html` as modified. This is correct.**

---

## Step 4: Add Embedded Content with iframe

### What This Step Does

iframes (inline frames) allow you to embed content from other websites into your page. This is commonly used for embedding videos, maps, or other interactive content. You'll add a simple iframe example.

### Instructions

1. In `index.html`, find the ordered list you added in Step 2
2. Add this code **after** the ordered list (before the `</body>` tag):

```html
<h2>Embedded Content</h2>
<p>Here's an example of embedded content:</p>
<iframe src="https://www.example.com" width="600" height="400" title="Example embedded content"></iframe>
```

3. Press **Ctrl + S** to save the file

### What to Notice

- **`<iframe>`** - This embeds another webpage or content into your page.
- **`src` attribute** - The URL of the content to embed.
- **`width` and `height` attributes** - Set the size of the iframe in pixels.
- **`title` attribute** - Provides a title for the iframe. This is important for accessibility, as screen readers use this to describe the embedded content.

**Note:** Some websites block embedding for security reasons. If an iframe doesn't load, it's likely because the source website doesn't allow embedding. In real projects, you'd embed content from services that allow it (like YouTube videos, Google Maps, etc.).

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should see `index.html` as modified. This is correct.**

---

## Step 5: Preview Your Page

### What This Step Does

Previewing lets you see how all the new elements look and work in a browser. You'll verify that links work, lists display correctly, images load, and the page looks good.

### Instructions

1. In VS Code file explorer, right-click on `index.html`
2. Click **Open with Live Server**

**Expected Result:** Your browser should open (or refresh if already open) showing your updated page.

### Verify What You See

You should see:
- ✅ Your original heading and paragraphs
- ✅ Links that you can click (they may not work yet, but they should be clickable and styled as links)
- ✅ An image displayed on the page
- ✅ Two headings: "Things I'm Learning" and "Steps to Build a Webpage"
- ✅ A bulleted list under "Things I'm Learning"
- ✅ A numbered list under "Steps to Build a Webpage"
- ✅ A heading "Embedded Content" with an iframe below it

**If you see all these elements, proceed to Step 6.**
**If something is missing, check that you saved the file and that you're viewing it with Live Server.**

---

## Step 6: Add Contact Section for Anchor Link

### What This Step Does

Earlier, you added an anchor link (`href="#contact"`), but you haven't created the element with `id="contact"` yet. Anchor links need a target element with a matching ID. You'll add a contact section so the anchor link works.

### Instructions

1. In `index.html`, find the iframe you added
2. Add this code **after** the iframe (before the `</body>` tag):

```html
<h2 id="contact">Contact Information</h2>
<p>This is the contact section. The anchor link at the top of the page will jump here when clicked.</p>
```

3. Press **Ctrl + S** to save the file

### What to Notice

- **`id="contact"`** - This creates an ID on the heading. The anchor link `href="#contact"` will jump to this element when clicked.
- IDs must be unique on a page (only one element can have `id="contact"`).
- IDs are case-sensitive (`contact` is different from `Contact`).

### Test the Anchor Link

1. Refresh your browser (F5) or the page should auto-refresh
2. Click the "contact information" link near the top of the page
3. The page should scroll down to the "Contact Information" heading

**If the anchor link works, proceed to Step 7.**

---

## Step 7: Commit Your Work

### What This Step Does

You've made several changes to your page. Now you'll commit all these changes together as one logical unit. Following professional habits, you'll check the status first to make sure everything is correct.

### Safety Check Before Committing

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 1 commit.

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
Your branch is ahead of 'origin/main' by 1 commit.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
        modified:   index.html
```

**If you see `index.html` under "Changes to be committed", proceed to commit.**

### Create the Commit

1. In the terminal, type exactly:
   ```bash
   git commit -m "s3: add links, lists, images, and embedded content"
   ```
2. Press **Enter**

**Expected Output:**
```
[main def5678] s3: add links, lists, images, and embedded content
 1 file changed, XX insertions(+), X deletions(-)
```

**The commit hash (def5678) will be different - that's normal.**

### Verify Commit Success

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

**Key indicators:**
- ✅ "Your branch is ahead of 'origin/main' by 2 commits" - You now have 2 local commits (Exercise 1 and Exercise 2)
- ✅ "nothing to commit, working tree clean" - All changes are committed

**If you see this, your commit was successful. Proceed to final verification.**

---

## Expected Final State

After completing this exercise, you should have:

- ✅ Hyperlinks added (external, internal, and anchor links)
- ✅ Ordered and unordered lists on your page
- ✅ Image with proper alt text
- ✅ Embedded content using iframe
- ✅ Contact section with ID for anchor link
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
Your branch is ahead of 'origin/main' by 2 commits.

nothing to commit, working tree clean
```

**If you see "working tree clean", you're ready for the next exercise.**

---

## What This Sets Up for Exercise 3

You now have a page with rich content elements. In the next exercise, you'll learn about tables, which are perfect for organizing structured data like schedules, comparisons, and statistics.

---

## Troubleshooting

### Problem: Links don't work when clicked

**Solution:**
- External links should work if you have internet connection
- Internal links (like `about.html`) won't work yet because that file doesn't exist - that's expected
- Anchor links should work if you added the `id="contact"` attribute correctly

### Problem: Image doesn't display

**Solution:**
- Check your internet connection (the placeholder service needs internet)
- Verify the `src` attribute is correct: `https://via.placeholder.com/400x200`
- Make sure you saved the file
- Try refreshing the browser

### Problem: iframe shows blank or error

**Solution:**
- Some websites block embedding - this is normal and expected
- The iframe code is correct; the source website just doesn't allow embedding
- In real projects, you'd use services that allow embedding (YouTube, Google Maps, etc.)

### Problem: Anchor link doesn't jump to section

**Solution:**
- Make sure you added `id="contact"` to the heading (not just the text)
- Verify the link uses `href="#contact"` (with the # symbol)
- Check that both the link and the ID use the same text (case-sensitive)

---

## Navigation

**Previous Exercise:** [[s3-html-css/s3e1-creating-first-webpage|Exercise 1: Creating Your First Webpage]]

**Next Exercise:** [[s3-html-css/s3e3-creating-tables|Exercise 3: Creating Tables]]

**Home:** [[index|Main Course Page]]

**Return to Section:** [[s3-html-css/index|HTML & CSS Section]]

---

## Next Steps

- [[c01-found/s3-html-css/index#HTML Content Elements|Return to Lecture]] - Go back to the lecture section that introduced links, lists, and media elements.
