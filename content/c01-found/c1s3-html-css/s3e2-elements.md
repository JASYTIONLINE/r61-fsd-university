---
title: "C1S3E2: Adding Rich Content Elements"
description: Add hyperlinks, lists, images, and embedded content to your webpage. Learn about accessibility and proper HTML attributes.
tags:
  - html
  - links
  - lists
  - images
  - accessibility
  - beginner
  - workbook
draft: false
date: 2026-01-30
---

# Exercise 2: Adding Rich Content Elements

**This exercise continues from [[s3e1-first-page|Exercise 1]]. You must complete Exercise 1 first.** Follow each step exactly.**
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
## Setup
### Part One
Download the image we will use in this exercise.

1. Download this image and save it to your project folder (the same folder where `index.html` is located):
![[local-img.jpg]]
**Note:** Right-click the image above and choose "Save image as..." Save it as `local-img.jpg` in the same folder as your `index.html` file.
![[vsc-jpgsaved.png]]

### Part 2: 
Create a basic About me page

1. Make sure you are in the projects folder.
2. In VS Code find the NEW FILE button
![[vsc-newfile.png]]
2. Create a file with the filename about.html
3. on line 1 type: "!", then hit enter.
4. VS Code should create an HTML5 basic structure for you.
![[vsc-html5.png]]
5. Change line 6 to read 
```
<title>About Me</title>
```

4. Replace the empty `<body>  </body>` section with the following code: 
```
<body>
    <P>This is a page about ME. I Like ME!</p>
    <p>Let's go <a href="index.html">Home</a>
</body>
```
4. Right Click and Choose "Format Document"
5. Hit *CTRL+s* and close the document

---
## What You Will Accomplish

By the end of this exercise, you will have:

- Added [hyperlinks](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Creating_links) (internal, external, and anchor links) to your page
- Created ordered and unordered [lists](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Lists)
- Added [images](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/HTML_images) from both local files and remote URLs with proper alt text for accessibility
- Embedded external content using [iframes](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/iframe)
- Learned about [HTML attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Attributes) and [accessibility](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Accessibility/HTML)
- Committed your work with Git (including image files)

---

## Step 1: Add [[https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Creating_links|Hyperlinks]] to Your Page

### What This Step Does

Hyperlinks (also called links) allow users to navigate to other pages or sections. Links are what make the web interconnected. You'll add three types of links: [external links](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Creating_links) (to other websites), [internal links](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Creating_links#same_directory) (to other pages on your site), and [anchor links](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Creating_links#document_fragments) (to sections on the same page).

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

4. Right Click anywhere in the code and choose "Format Document" to clean up the format after you copy and paste![[vsc-format.png]]
5. Press **Ctrl + S** to save the file

### What to Notice

- **`<a href="url">`** - This is the anchor tag that creates a link. The `href` attribute (short for "hypertext reference") tells the browser where to go when the link is clicked.
- **External links** - `href="https://www.example.com"` links to another website. Always include `https://` for external links.
- **Internal links** - `href="about.html"` links to another page in your site. This is a relative path (relative to the current file).
- **Anchor links** - `href="#contact"` links to an element with `id="contact"` on the same page. The `#` tells the browser to look for an ID on the current page.

### Verify Changes

1. Preview your page: Use Live server to open your page in a locally hosted web browser.  Make sure everything looks like it is supposed to.
2. Fix any problems and Hit *CTRL+s* to save your file 
3. In the VS Code terminal, type:
   ```bash
   git status
   ```
4. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 1 commit.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   index.html
```
**Note:** you may see "Your branch is ahead of 'origin/main' by 1 commit." if you have not pushed your last commit (that is ok, we did not tell you to)

**If you see `index.html` listed as modified, proceed to Step 2.**
(We will commit and push later after a few more changes)

---

## Step 2: Add Lists to Your Page

### What This Step Does

Lists organize information in an easy-to-read format. You'll create both an unordered list (bulleted) and an ordered list (numbered). Lists are great for navigation menus, feature lists, step-by-step instructions, and any information that benefits from being organized in items.

### Instructions

1. In `index.html`, find the closing `</body>` tag (the last line)
2. Add this code **before** the `</body>` tag:

```html
<h2>Steps to Build a Webpage</h2>
<ol>
  <li>Create the HTML structure</li>
  <li>Add content elements</li>
  <li>Style with CSS</li>
  <li>Test in browser</li>
</ol>

<h2>I am Learning many things:</h2>
<ul>
  <li>Creating lists</li>
  <li>Adding links</li>
  <li>Adding images</li>
</ul>
```

3. Press **Ctrl + S** to save the file

### What to Notice

- **`<h2>`** - This is a second-level heading. It's smaller than `<h1>` but larger than regular text. Headings create hierarchy in your document.
- **`<ul>`** - Unordered list. Creates a bulleted list. Use this when the order doesn't matter.
- **`<ol>`** - Ordered list. Creates a numbered list. Use this when the order matters (like steps).
- **`<li>`** - List item. Each `<li>` is one item in the list. You can have as many as you need.
- **List items can contain other elements** - List items aren't limited to just text. You can put paragraphs, images, links, and even other lists inside a list item. This allows you to create rich, contextual content within your lists.

---
## Step 3: Add Links to Your Page
### What This Step Does
Links allow the user to move from one web page to another, or from one place on the web page to another.  Just as lists organize information in an easy-to-read format, links allows you to move from one idea to the next and back. You'll create external links and internal links.
### Instructions:
1. In `index.html`, find the list item that says `<li>Adding links</li>![[vsc-linksline.png]]`
![[vsc-linksline.png]]
2. Replace that line with this code to add the link examples inside the list item. (These are the same links you added in Step 1, now integrated into the list structure):

```html
<li>Adding links
  <p>Visit <a href="https://www.example.com">Example Website</a> to learn more.</p>
  <p>You can also check out <a href="about.html">my about page</a> </p>
  <p>Jump to <a href="#contact">contact information</a> at the bottom of this page.</p>
</li>
```
3. Right Click and "Format Document" or try a hot key *SHFT+Alt+f* to clean things up a bit.
4. Hit *CTRL+s* to save the file
5. If your index page is still open in your browser, refresh and take a look. If it is not, right-click on **'index.html'** and "Open with Live Server"

---
## Step 4: Add Images to Your Page

### What This Step Does

Images make web pages more engaging and informative. You'll add two images to your page: one from a local file in your project folder and one from an external URL. This will teach you the two main ways to include images: from files in your project folder and from external websites. You'll also learn about the `alt` attribute, which is essential for accessibility. In this step, you'll also integrate the links and images into your list structure, showing how list items can contain rich content.

### Instructions
1. Find the list item that says `<li>Adding images</li>`
2. Replace that line with this code to add the image examples inside the list item:

```html
<li>Adding images
  <p>This is a local image from my server. It is MINE!</p>
  <img src="local-img.jpg" alt="A local image demonstrating HTML image embedding">
  <br>
  <p>This image is hosted on another server. I am borrowing it!</p>
  <img src="https://placehold.co/400x200" alt="A placeholder image showing 400 by 200 pixels">
  <br>
</li>
```

3. Hit *SHFT+ALT+F* to format the document
4. Press *Ctrl + S* to save the file
5. You'll notice you don't actually have to refresh your browser when using live server. It automatically refreshes when you save the file. Take a look at what you have so far.
6. 
**CAUTION: - DO NOT** copy and paste over the `<ul>` tag after `<Adding images>`, this will break your list.  
![[vsc-cp-warning.png]]
### What to Notice
- **`<img>`** - This is a [self-closing tag](https://developer.mozilla.org/en-US/docs/Glossary/Void_element#self-closing_tags) (no closing tag needed). It displays an image.
- [`src` attribute](http://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/src) - This tells the browser where to find the image. It can be:
  - **A local file path** (like `local-img.jpg`) - This is a [relative path](https://developer.mozilla.org/en-US/docs/Learn_web_development/Howto/Web_mechanics/What_is_a_URL#path_to_resource) from your HTML file to the image file. Since the image is in the same folder as your HTML file, you just use the filename.
  - A [URL](https://developer.mozilla.org/en-US/docs/Learn_web_development/Howto/Web_mechanics/What_is_a_URL) (like `https://placehold.co/400x200`) - This links to an image hosted on another server. The browser downloads it from the internet.
- [`alt` attribute](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/alt) - This is **required** for accessibility. It provides text that describes the image. Screen readers use this text to tell visually impaired users what the image shows. If the image fails to load, browsers also display this text. Always include descriptive alt text.

**Path Notes:**
- When using local files, the path is relative to your HTML file's location
- `local-img.jpg` means "look for the file in the same folder as this HTML file"
- If the image was in a subfolder called `images`, you'd use `images/local-img.jpg`
- If the image was in a parent folder, you'd use `../local-img.jpg` (the `..` means "go up one folder")

**Accessibility Note:** The `alt` attribute is not optional. Every image must have alt text. If an image is purely decorative and adds no information, you can use `alt=""` (empty string), but most images should have descriptive text.

### Verify Changes

1. In the terminal, type exactly:
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

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        local-img.jpg
```

**Note:** You should see both `index.html` as modified AND `local-img.jpg` as an untracked file. This is correct - the new image file needs to be added to your repository. We'll commit both files together later.

---

## Step 4: Add Embedded Content with iframe

### What This Step Does

[iframes](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/iframe) (inline frames) allow you to embed content from other websites into your page. This is commonly used for embedding videos, maps, or other interactive content. You'll add a simple iframe example.

### Instructions

1. In `index.html`, right after your unordered list containing your images, add this code (after `<ul>` and before the `</body>` tag):

```html
<h2>Embedded Content</h2>
<p>Here's an example of embedded content:</p>
<iframe src="https://www.example.com" width="600" height="400" title="Example embedded content"></iframe>
```

3. Press **Ctrl + S** to save the file

### What to Notice

- **`<iframe>`** - This embeds another webpage or content into your page.
- **`src` attribute** - The URL of the content to embed.
- [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/width) and [`height`](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/height) attributes** - Set the size of the iframe in pixels.
- The [`title`](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/title) attribute - Provides a descriptive name for the iframe. This is important for accessibility, as screen readers use this to describe the embedded content.

**Note:** Some websites block embedding for security reasons. If an iframe doesn't load, it's likely because the source website doesn't allow embedding. In real projects, you'd embed content from services that allow it (like YouTube videos, Google Maps, etc.).

### Get used to this

1. Hot *CTRL+S*
2. Check your web page on Live Server. (Make sure it works)
3. In the terminal, type:
   ```bash
   git status
   ```
4. Press **Enter**

**You should see 
```
 (use "git add <file>..." to include in what will be committed)
        projects/local-img.jpg
        projects/project-index.html
```
This is correct. We will add and commit in a minute

---

## Step 5: Check Your Work with Live Server

### What This Step Does

Previewing lets you see how all the new elements look and work in a browser. You'll verify that links work, lists display correctly, images load, and the page looks good.

### Instructions

1. In VS Code file explorer, right-click on `index.html`
2. Click **Open with Live Server**

**Expected Result:** Your browser should open (or refresh if already open) showing your updated page.

### Verify What You See

You should see:
- ✅ Your original heading and paragraphs
- ✅ A heading "I am Learning many things:" with a bulleted list
- ✅ Links inside the "Adding links" list item (they may not work yet, but they should be clickable and styled as links)
- ✅ Two images inside the "Adding images" list item (one local image from your project folder and one remote image from the placeholder service)
- ✅ A heading "Steps to Build a Webpage" with a numbered list
- ✅ A heading "Embedded Content" with an iframe below it

**If you see all these elements, proceed to Step 6.**
**If something is missing, check that you saved the file and that you're viewing it with Live Server.**

---

## Step 6: Add Contact Section for Anchor Link

### What This Step Does

Earlier, you added an anchor link (`href="#contact"`), but you haven't created the element with `id="contact"` yet. Anchor links need a target element with a matching ID. You'll add a contact section so the anchor link works.

### Instructions
1. Find the first line of your page's `<body>`.  Ity should be `<h1>Welcome to My First Webpage</h1>`
2. Replace just that line with the following code:
```
<h1 id="top">Welcome to My First Webpage</h1>
```
1. In `index.html`, find the iframe you added
2. Add this code **after** the iframe (before the `</body>` tag):

```html
<h2 id="contact">Contact Information</h2>
<p>This is the contact section. The anchor link at the top of the page will jump here when clicked.</p>
  <p>Return to <a href="#top">Top of Page</a> </p>
```

3. "Format" your document to clean it **up**
4. Press **Ctrl + S** to save the file

### What to Notice

- You created two anchors. One at the top of the page and one at the bottom.  
- You can jump between the two.
	- **`id="contact"`** - This creates an ID on the heading. 
	- The anchor link `href="#contact"` will jump to this element when clicked.
-  You created a link back to the top of the page with:
	- `<p>Return to <a href="#top">Top of Page</a> </p>`
	and
	- ` <h1 id="top">Welcome to My First Webpage</h1>`
**Note:** 
- IDs must be unique on a page (only one element can have `id="contact"`).
-  IDs are case-sensitive (`contact` is different from `Contact`).
---
### Test the Anchor Link

1. Refresh your browser (F5) or the page should auto-refresh
2. Click the "contact information" link near the top of the page
3. The page should scroll down to the "Contact Information" heading.
4. Now click  "Return to Top" land you should return to the top of the page.

**If the anchor links work, proceed to Step 7.**

---

## Step 7: Commit Your Work

### What This Step Does

You've made several changes to your page. It is important to commit your work to the repository on a regular basis. Do not wait too long to commit work. A good rule for developers is to commit your work a soon as you have working code.   This gives you a good reset point in the event something goes wrong further down the line.  

Now that you have verified you have a good working index page that performs as intended (you have good code), it is time to commit these changes together as one logical unit. Following professional habits, you'll check the status first to make sure everything is correct.

### Safety Check Before Committing
Do this every time to save yourself a few headaches

1. In the VS Code terminal, type exactly:
   ```bash
   clear
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

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        local-img.jpg

no changes added to commit (use "git add" or "git commit -a")
```

**Verify:**
- ✅ You are on `main` branch
- ✅ `index.html` is modified
- ✅ `local-img.jpg` appears as an untracked file (this is expected - we'll add it)
- ✅ No other unexpected files are listed

**If everything looks correct, proceed to staging.**
**If you see unexpected files, review your work before committing.**

### Stage the Files

1. In the terminal, type exactly:
   ```bash
   git add index.html local-img.jpg
   ```
2. Press **Enter**

**Expected Result:** No error message, prompt returns.

**Note:** We're adding both the modified HTML file and the new image file to the staging area.

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
        new file:   local-img.jpg
```

**If you see both `index.html` and `local-img.jpg` under "Changes to be committed", proceed to commit.**

### Create the Commit

1. In the terminal, type exactly:
   ```bash
   git commit -m "s3e1: add links, lists, images, and embedded content"
   ```
2. Press **Enter**

**Expected Output:**
```
[main def5678] s3: add links, lists, images, and embedded content
 2 files changed, XX insertions(+), X deletions(-)
 create mode 100644 local-img.jpg
```

**The commit hash (def5678) will be different - that's normal. You should see 2 files changed, which includes both the HTML file and the new image file.**

### Verify Commit Success

1. In the terminal, type:
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
- ✅ Two images with proper alt text (one local file, one remote URL)
- ✅ `local-img.jpg` file saved in your project folder
- ✅ Embedded content using iframe
- ✅ Contact section with ID for anchor link
- ✅ All changes committed to Git (including the image file)
- ✅ Working tree clean

### Final Step
Push your local changes to the remote server on GitHub

1. In the terminal, type exactly:
   ```bash
   git push
   ```
2. Press **Enter**

**Expected Output:**  (Something Like)
```
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 24 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 395 bytes | 395.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/JASYTIONLINE/knowledge-base.git
   f5986fc..7ce89c0  main -> main
```

**If you see:
"On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean",

Congratulations Code Monkey, you're ready for the next exercise.**

---

## What This Sets Up for Exercise 3

You now have a page with rich content elements. In the next exercise, you'll learn about tables, which are perfect for organizing structured data like schedules, comparisons, and statistics.

---
#### Next Steps: [Return to HTML-CSS Lecture](c01-found/c1s3-html-css/s3e3-tables#3.-Structured-Data-with-Tables)
3. Structured Data with Tables
---
## Troubleshooting

### Problem: Links don't work when clicked

**Solution:**
- External links should work if you have internet connection
- Internal links (like `about.html`) won't work yet because that file doesn't exist - that's expected
- Anchor links should work if you added the `id="contact"` attribute correctly

### Problem: Local image doesn't display

**Solution:**
- Verify that `local-img.jpg` is in the same folder as your `index.html` file
- Check that the filename matches exactly (including capitalization): `local-img.jpg`
- Verify the `src` attribute is correct: `local-img.jpg` (just the filename, since it's in the same folder)
- Make sure you saved the HTML file
- Try refreshing the browser
- Check the browser console (F12) for error messages about the image path

### Problem: Remote image doesn't display

**Solution:**
- Check your internet connection (the placeholder service needs internet)
- Verify the `src` attribute is correct: `https://placehold.co/400x200`
- Make sure you saved the file
- Try refreshing the browser
- Some networks block external image requests - try a different network if possible

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