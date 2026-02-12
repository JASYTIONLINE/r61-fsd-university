---
title: "Exercise 3: Creating Tables"
description: "Create HTML tables to organize structured data. Learn about semantic table elements and proper table structure."
tags: [html, tables, structured-data, beginner, workbook]
draft: false
date: "2026-01-30"
---

# Exercise 3: Creating Tables

**This exercise continues from Exercise 2. You must complete [[c01-found/s3-html-css/s3e2-adding-rich-content-elements|Exercise 2]] first.**

** Follow each step exactly.**

**Time Required:** 20-25 minutes

---

## Prerequisites Check

Before starting, verify:

1. ✅ **Exercise 2 completed**
   - `index.html` file has [[s3e2-adding-rich-content-elements|links, lists, images, and embedded content]]
   - All changes from Exercise 2 are [[c01-found/s2-vers-ctrl/s2e3-pushing-changes#Step 3: Commit the File|committed]].
   - You have [[c01-found/s2-vers-ctrl/s2e3-pushing-changes#Step 5: Push to GitHub|pushed your changes]] to the remote GitHub server on the command line.
   - You can [[r61-fsd-university/content/c01-found/s3-html-css/s3e1-creating-first-webpage#Step 4: Install Live Server Extension (One-Time Setup)|preview your page in a browser]]

2. ✅ **Current State Verification**
   - Open VS Code 
	<details>
<summary>How to open Run</summary>

Press **Win + R**  
Type `code`  
Press Enter

</details>
   - Open VS Code terminal (Ctrl + ~)
   - Type: `git status`
   - Press Enter

**Expected Output:**
```
On branch main
Your branch is up to date with 'origin/main'.
```

**If you see this, proceed.**
**If not, complete Exercise 2 first or resolve and push any uncommitted changes.**

---

## What You Will Accomplish

By the end of this exercise, you will have:

- Created a properly structured HTML table
- Used semantic table elements (thead, tbody, th, td)
- Added a table caption
- Understood when and how to use tables
- Committed your work with Git

---

## Step 1: Understand When to Use Tables

### What This Step Does

Before creating a [table in HTML](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/HTML_table_basics), it's important to understand when tables are appropriate. Tables are perfect for organizing structured data that has a clear relationship between rows and columns. They're ideal for schedules, comparisons, statistics, and any information that benefits from being displayed in a grid format.

**Good uses for tables:**
- Schedules (time slots, days of the week)
- Product comparisons (features, prices)
- Statistics (data with multiple related values)
- Contact lists (names, emails, phone numbers)

**Not good uses for tables:**
- Page layout (use CSS for layout, not tables)
- Simple lists (use `<ul>` or `<ol>` instead)
- Text content (use paragraphs and headings)

For this exercise, you'll create a simple schedule table to demonstrate table structure.

---

## Step 2: Add a Table to Your Page

### What This Step Does

You'll create a table that shows a weekly schedule. This demonstrates all the important [table elements:](https://cmastris.github.io/html-tables-cheat-sheet/) caption (table title), thead (header row), tbody (body rows), th (header cells), and td (data cells). Using semantic table elements makes your tables more accessible and easier to style later.

### Instructions

1. Open `index.html` ``` (knowledge-base\projects\index.html)```  in VS Code
2. Find the contact section you added in Exercise 2 (the one with `id="contact"`)
3. ![[vsc-id-contacts.png]]
4. Add this code **after** the contact section (before the `<p>Return...` line:

```html
<h2>Weekly Schedule</h2>
<table>
  <caption>My first HTML Table.</caption>
   <caption>It is my Schedule for This Week</caption>
  <thead>
    <tr>
      <th>Day</th>
      <th>Topic</th>
      <th>Time</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Monday</td>
      <td>HTML Structure</td>
      <td>2 hours</td>
    </tr>
    <tr>
      <td>Tuesday</td>
      <td>HTML Elements</td>
      <td>2 hours</td>
    </tr>
    <tr>
      <td>Wednesday</td>
      <td>Tables and Forms</td>
      <td>2 hours</td>
    </tr>
    <tr>
      <td>Thursday</td>
      <td>CSS Introduction</td>
      <td>2 hours</td>
    </tr>
    <tr>
      <td>Friday</td>
      <td>CSS Styling</td>
      <td>2 hours</td>
    </tr>
  </tbody>
</table>
```

4. Press **Ctrl + S** to save the file
5. Format the document to clean it up
6. Open in live server

### What to Notice

- **`<table>`** - This is the container for the entire table. Everything related to the table goes inside this tag.
- **`<caption>`** - This provides a title or description for the table. It appears above the table and helps users understand what the table shows. Screen readers also use this to describe the table.
- **`<thead>`** - This is the table header section. It contains the header row(s) that describe what each column represents. Thead is semantic HTML that helps screen readers understand the table structure.
- **`<tbody>`** - This is the table body section. It contains all the data rows. Separating thead and tbody makes the table more semantic and easier to style.
- **`<tr>`** - This is a table row. Each `<tr>` creates one horizontal row in the table.
- **`<th>`** - This is a table header cell. It's used in the `<thead>` section to label columns. Header cells are bold by default and help users understand what each column represents.
- **`<td>`** - This is a table data cell. It contains the actual data in the table. Each `<td>` is one cell in a row.
- notice how each nested piece is moved one tab tot he right when you format the document showing you the parent child relationship between each line.
![[vsc-nested.png]]
**Semantic Structure:** Notice how the table is organized with thead and tbody. This semantic structure helps screen readers navigate the table, makes it easier to style different sections, and clearly separates headers from data.

### Verify Changes

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   projects/index.html
```

**If you see `index.html` >

- copy and paste this line onto your command line:

 ```
    git commit -m "added table to project/index.html"
    git add projects/index.html

 ```
  
  You will see a warning about running multiple commands.  This is normal. Just verify you have the correct syntax and click "Paste"
  
  ![[term-multiline.png]]
  
- Expected output: you should see something very similar to this>
```
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   projects/index.html

```

- USE git add to "Stage" your index file, push it, then verify your tree is up to date with git status
- proceed to Step 3.**

---

## Step 3: Preview Your Table

### What This Step Does

Previewing lets you see how the table looks in a browser. You'll verify that the table displays correctly with proper rows and columns, and that the caption appears above the table.

### Instructions

1. In VS Code file explorer, right-click on `index.html`
2. Click **Open with Live Server** (or refresh if already open)

**Expected Result:** Your browser should show the updated page with a table at the bottom.

### Verify What You See

You should see:
- ✅ A heading "Weekly Schedule"
- ✅ A caption above the table: "My Learning Schedule for This Week"
- ✅ A table with three columns: Day, Topic, Time
- ✅ Five rows of data (Monday through Friday)
- ✅ The header row (Day, Topic, Time) should appear bold or styled differently
- ✅ All data should be organized in neat rows and columns

**If you see the table displayed correctly, proceed to Step 4.**
**If the table doesn't look right, check that you saved the file and that all tags are properly closed.**

---

## Step 4: Add More Table Rows (Optional Practice)

### What This Step Does

This step gives you practice adding more data to your table. In real projects, tables often have many rows, and you'll need to know how to add them. This also reinforces the table structure you just learned.

### Instructions

1. In `index.html`, find the table you just created
2. Inside the `<tbody>` section, after the Friday row, add these two more rows:

```html
    <tr>
      <td>Saturday</td>
      <td>Practice and Review</td>
      <td>3 hours</td>
    </tr>
    <tr>
      <td>Sunday</td>
      <td>Rest Day</td>
      <td>0 hours</td>
    </tr>
```

3. Press **Ctrl + S** to save the file

### What to Notice

- Each new row follows the same pattern: `<tr>` opens the row, three `<td>` elements contain the data (matching the three columns), and `</tr>` closes the row.
- The number of `<td>` elements in each row must match the number of columns (in this case, three: Day, Topic, Time).
- All rows go inside the `<tbody>` section, not in `<thead>`.

### Here we go again. Its time to Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see `index.html` as modified. This is correct.**

---

## Step 5: Commit Your Work

### What This Step Does

You've added a table to your page. Now you'll commit this change following the professional habits from Section 2. You'll check the status first to make sure everything is correct.

### Safety Check Before Committing

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 2 commits.

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

---
**Note:** You must be in the "projects" to add the index file with just add index.html.

If you are in the root knowledge base directory, you must give the relative path in your add command:

```
git add projects/index.html
```

or change directories into knowledge-base/projects 

```
cd projects 
```

to get into the projects folder in Terminal

---
### Verify File is Staged

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 2 commits.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
        modified:   index.html
```

**If you see `index.html` under "Changes to be committed", proceed to commit.**

### Create the Commit

1. In the terminal, type exactly:
   ```bash
   git commit -m "s3: add table with semantic structure"
   ```
2. Press **Enter**

**Expected Output:**
```
[main ghi7890] s3: add table with semantic structure
 1 file changed, XX insertions(+), X deletions(-)
```

**The commit hash (ghi7890) will be different - that's normal.**

### Verify Commit Success

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 1 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

**Key indicators:**
- ✅ "Your branch is ahead of 'origin/main' by 1 commits" - You now have 1 local commit to push
- ✅ "nothing to commit, working tree clean" - All changes are committed

**If you see this, your commit was successful, PUSH your commit and proceed to final verification.**

---

## Expected Final State

After completing this exercise, you should have:

- ✅ A properly structured HTML table on your page
- ✅ Table with caption, thead, and tbody sections
- ✅ Header row with `<th>` elements
- ✅ Data rows with `<td>` elements
- ✅ All changes committed to Git
- ✅ All commits pushed to remote
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
Your branch is up to date with 'origin/main'.
```

**If you see "Your branch is up to date...", you're ready for the next exercise.**

---

## What This Sets Up for Exercise 4

You now understand how to create tables for organizing structured data. In the next exercise, you'll learn about forms, which allow users to submit data to your website. Forms are essential for contact forms, search boxes, login pages, and any interactive data collection.

---
## Next Steps

- [[c01-found/s3-html-css/index#Collecting User Input with Forms|Return to Lecture]] - Go back to the "Collecting User Input with Forms section" of the lecture before moving on.

---
## Troubleshooting

### Problem: Table doesn't display in rows and columns

**Solution:**
- Check that all tags are properly closed (`</tr>`, `</td>`, `</tbody>`, `</table>`)
- Make sure each row has the same number of cells (three `<td>` elements in this case)
- Verify that `<th>` elements are in `<thead>` and `<td>` elements are in `<tbody>`

### Problem: Caption doesn't appear

**Solution:**
- Make sure `<caption>` is directly inside `<table>` (not inside thead or tbody)
- Verify the caption tag is properly closed: `</caption>`
- Check that you saved the file

### Problem: Table looks messy or unaligned

**Solution:**
- This is normal! Tables look basic without CSS styling
- The structure is correct; you'll learn to style tables in later exercises
- For now, focus on getting the HTML structure right

### Problem: Header row doesn't look different

**Solution:**
- `<th>` elements are bold by default, but without CSS they may not look very different
- The important thing is that you're using `<th>` in the header, which is semantically correct
- You'll learn to style tables with CSS in later exercises

---
## Navigation

**Previous Exercise:** [[s3-html-css/s3e2-adding-rich-content-elements|Exercise 2: Adding Rich Content Elements]]

**Next Exercise:** [[s3-html-css/s3e4-creating-forms|Exercise 4: Creating Forms]]

**Home:** [[r61-fsd-university/content/c01-found/s3-html-css/index|Main Course Page]]

**Return to Section:** [[s3-html-css/index|HTML & CSS Section]]
