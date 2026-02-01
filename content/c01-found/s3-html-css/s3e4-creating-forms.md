---
title: "Exercise 4: Creating Forms"
description: "Create HTML forms to collect user input. Learn about different input types, labels, and form accessibility."
tags: [html, forms, user-input, accessibility, beginner, workbook]
draft: false
date: "2026-01-30"
---

# Exercise 4: Creating Forms

**This exercise continues from Exercise 3. You must complete Exercise 3 first.**

**This exercise is a standalone technical manual. Follow each step exactly.**

**Time Required:** 25-30 minutes

---

## Prerequisites Check

Before starting, verify:

1. ✅ **Exercise 3 completed**
   - `index.html` file has a table with semantic structure
   - All changes from Exercise 3 are committed
   - You can preview your page in a browser

2. ✅ **Current State Verification**
   - Open VS Code terminal (Ctrl + ~)
   - Type: `git status`
   - Press Enter

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 3 commits.

nothing to commit, working tree clean
```

**If you see this, proceed.**
**If not, complete Exercise 3 first or resolve any uncommitted changes.**

---

## What You Will Accomplish

By the end of this exercise, you will have:

- Created a contact form with multiple input types
- Used proper labels associated with inputs (for accessibility)
- Added form validation attributes
- Understood different input types and when to use them
- Committed your work with Git

---

## Step 1: Understand Forms and Their Purpose

### What This Step Does

Forms allow users to submit data to your website. They're essential for many web features: contact forms let users send messages, search boxes let users find content, login forms authenticate users, and registration forms collect user information. Understanding forms is crucial for building interactive websites.

**Common uses for forms:**
- Contact forms (name, email, message)
- Search boxes (search terms)
- Login forms (username, password)
- Registration forms (user information)
- Surveys and feedback forms

**Key form concepts:**
- **Input fields** - Where users type or select information
- **Labels** - Text that describes what each input is for (essential for accessibility)
- **Submit button** - Sends the form data
- **Validation** - Ensures users enter data in the correct format

For this exercise, you'll create a contact form that demonstrates these concepts.

---

## Step 2: Create a Basic Contact Form

### What This Step Does

You'll create a contact form with text input, email input, and a textarea for messages. This demonstrates the basic form structure and shows how different input types work. Most importantly, you'll learn about labels and how to associate them with inputs for accessibility.

### Instructions

1. Open `index.html` in VS Code
2. Find the table you added in Exercise 3
3. Add this code **after** the table (before the `</body>` tag):

```html
<h2>Contact Me</h2>
<form>
  <label for="name">Your Name:</label>
  <input type="text" id="name" name="name" required>
  
  <label for="email">Your Email:</label>
  <input type="email" id="email" name="email" required>
  
  <label for="message">Your Message:</label>
  <textarea id="message" name="message" rows="5" required></textarea>
  
  <button type="submit">Send Message</button>
</form>
```

4. Press **Ctrl + S** to save the file

### What to Notice

- **`<form>`** - This is the container for all form elements. Everything related to the form goes inside this tag.
- **`<label>`** - This provides text that describes what the input is for. The `for` attribute connects the label to a specific input using the input's `id`. When users click the label, it focuses the associated input (this is helpful on mobile devices and for accessibility).
- **`for` and `id` attributes** - The `for="name"` in the label matches `id="name"` in the input. This association is essential for screen readers and improves usability.
- **`<input>`** - This creates an input field. The `type` attribute determines what kind of input it is.
- **`type="text"`** - Creates a single-line text input for names, addresses, etc.
- **`type="email"`** - Creates an email input that validates the format (checks for @ symbol, etc.)
- **`name` attribute** - This identifies the input when the form is submitted. Each input needs a unique name.
- **`required` attribute** - This makes the field mandatory. Browsers will prevent form submission if required fields are empty.
- **`<textarea>`** - This creates a multi-line text input, perfect for longer messages. The `rows` attribute sets the visible height.
- **`<button type="submit">`** - This creates a button that submits the form when clicked.

**Accessibility Note:** Always use `<label>` elements with the `for` attribute matching the input's `id`. This helps screen readers understand the form and makes it easier for all users to interact with form fields.

### Verify Changes

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 3 commits.

Changes not staged for commit:
  (use "git add <file>..." to include in what will be committed)
        modified:   index.html
```

**If you see `index.html` listed as modified, proceed to Step 3.**

---

## Step 3: Add More Input Types

### What This Step Does

HTML provides many input types for different kinds of data. You'll add a few more input types to your form to see how they work. This demonstrates the variety of form controls available and when to use each one.

### Instructions

1. In `index.html`, find the form you just created
2. Add these additional fields **before** the submit button (after the textarea):

```html
  <label for="phone">Your Phone (optional):</label>
  <input type="tel" id="phone" name="phone">
  
  <label for="subject">Subject:</label>
  <select id="subject" name="subject" required>
    <option value="">Choose a subject...</option>
    <option value="question">Question</option>
    <option value="feedback">Feedback</option>
    <option value="support">Support Request</option>
  </select>
  
  <label>
    <input type="checkbox" name="newsletter" value="yes">
    Subscribe to newsletter
  </label>
```

3. Press **Ctrl + S** to save the file

### What to Notice

- **`type="tel"`** - This is for phone numbers. On mobile devices, it may show a numeric keypad. Notice this field doesn't have `required`, making it optional.
- **`<select>`** - This creates a dropdown menu. Users can choose from a list of options.
- **`<option>`** - Each option is one choice in the dropdown. The `value` attribute is what gets submitted, while the text between tags is what users see.
- **First option with empty value** - `value=""` creates a placeholder option. This is a common pattern for dropdowns.
- **`type="checkbox"`** - This creates a checkbox for yes/no choices. Notice this label doesn't use `for` and `id` because the input is directly inside the label (this is also valid).

**Input Type Options:** HTML provides many input types: `text`, `email`, `password`, `number`, `date`, `time`, `url`, `tel`, `checkbox`, `radio`, `file`, and more. Each type provides appropriate validation and user interface.

### Verify Changes

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**You should still see `index.html` as modified. This is correct.**

---

## Step 4: Preview Your Form

### What This Step Does

Previewing lets you see how the form looks and test how different input types behave. You'll verify that labels are associated correctly, inputs work as expected, and the form displays properly.

### Instructions

1. In VS Code file explorer, right-click on `index.html`
2. Click **Open with Live Server** (or refresh if already open)

**Expected Result:** Your browser should show the updated page with a form at the bottom.

### Verify What You See

You should see:
- ✅ A heading "Contact Me"
- ✅ A form with several labeled input fields
- ✅ Text input for "Your Name"
- ✅ Email input for "Your Email"
- ✅ Textarea for "Your Message"
- ✅ Phone input for "Your Phone (optional)"
- ✅ Dropdown menu for "Subject"
- ✅ Checkbox for "Subscribe to newsletter"
- ✅ Submit button labeled "Send Message"

### Test the Form

Try these interactions:
1. **Click on a label** - The associated input should become focused (cursor appears in it)
2. **Try submitting empty form** - Browsers should prevent submission and highlight required fields
3. **Enter invalid email** - Try typing "notanemail" in the email field and submitting - browser should show an error
4. **Use the dropdown** - Click the subject dropdown and see the options

**If the form displays and behaves correctly, proceed to Step 5.**
**If something doesn't work, check that you saved the file and that all attributes are correct.**

---

## Step 5: Understand Form Submission (Conceptual)

### What This Step Does

This step explains what happens when forms are submitted. You won't actually make the form submit anywhere (that requires server-side code), but it's important to understand how forms work.

**What happens when a form is submitted:**
1. Browser collects all form data (values from inputs with `name` attributes)
2. Browser validates required fields and input types
3. If validation passes, browser sends data to the server (specified in `action` attribute)
4. Server processes the data (saves to database, sends email, etc.)
5. Server sends a response back to the browser

**For this exercise:**
- Your form doesn't have an `action` attribute, so it won't actually submit anywhere
- This is fine for learning - you're focusing on the HTML structure
- In real projects, you'd add `action="url"` and `method="post"` to make forms functional

**Note:** The form structure you're creating is correct. Making it actually submit data requires backend code (which you'll learn in later courses). For now, focus on creating properly structured, accessible forms.

---

## Step 6: Commit Your Work

### What This Step Does

You've added a complete contact form to your page. Now you'll commit this change following professional habits. You'll check the status first to make sure everything is correct.

### Safety Check Before Committing

1. In the VS Code terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 3 commits.

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
Your branch is ahead of 'origin/main' by 3 commits.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
        modified:   index.html
```

**If you see `index.html` under "Changes to be committed", proceed to commit.**

### Create the Commit

1. In the terminal, type exactly:
   ```bash
   git commit -m "s3: add contact form with multiple input types"
   ```
2. Press **Enter**

**Expected Output:**
```
[main jkl0123] s3: add contact form with multiple input types
 1 file changed, XX insertions(+), X deletions(-)
```

**The commit hash (jkl0123) will be different - that's normal.**

### Verify Commit Success

1. In the terminal, type exactly:
   ```bash
   git status
   ```
2. Press **Enter**

**Expected Output:**
```
On branch main
Your branch is ahead of 'origin/main' by 4 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

**Key indicators:**
- ✅ "Your branch is ahead of 'origin/main' by 4 commits" - You now have 4 local commits
- ✅ "nothing to commit, working tree clean" - All changes are committed

**If you see this, your commit was successful. Proceed to final verification.**

---

## Expected Final State

After completing this exercise, you should have:

- ✅ A contact form with multiple input types
- ✅ Proper labels associated with all inputs (using `for` and `id`)
- ✅ Required fields with validation
- ✅ Text, email, tel, textarea, select, and checkbox inputs
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
Your branch is ahead of 'origin/main' by 4 commits.

nothing to commit, working tree clean
```

**If you see "working tree clean", you're ready for the next exercise.**

---

## What This Sets Up for Exercise 5

You now understand how to create forms for collecting user input. In the next exercise, you'll learn about semantic HTML structure, including how to use ID and class attributes, and semantic elements like header, footer, nav, and section. This will help you organize your page structure better.

---

## Troubleshooting

### Problem: Labels don't focus inputs when clicked

**Solution:**
- Make sure the `for` attribute in the label matches the `id` attribute in the input exactly (case-sensitive)
- Verify both `for` and `id` use the same text
- Check that the input has an `id` attribute (not just `name`)

### Problem: Form submits even with empty required fields

**Solution:**
- Make sure you added the `required` attribute to inputs that should be mandatory
- Check that `required` is spelled correctly (not "require" or "requirement")
- Verify the browser supports HTML5 validation (all modern browsers do)

### Problem: Email validation doesn't work

**Solution:**
- Make sure you used `type="email"` (not `type="text"`)
- Try entering a clearly invalid email like "test" - browser should show error
- Some browsers are lenient with email validation

### Problem: Dropdown doesn't show options

**Solution:**
- Make sure each `<option>` is inside the `<select>` tag
- Verify option tags are properly closed: `</option>`
- Check that you saved the file

---

## Navigation

**Previous Exercise:** [[s3-html-css/s3e3-creating-tables|Exercise 3: Creating Tables]]

**Next Exercise:** [[s3-html-css/s3e5-using-semantic-html-structure|Exercise 5: Using Semantic HTML Structure]]

**Home:** [[index 1|Main Course Page]]

**Return to Section:** [[s3-html-css/index|HTML & CSS Section]]
