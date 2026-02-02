---
title: "HTML & CSS Foundations"
description: "Comprehensive introduction to HTML and CSS, building web pages from structure to styling, culminating in a complete project."
tags: [html, css, web-development, beginner, fundamentals]
draft: false
date: "2026-01-30"
---

# HTML & CSS Foundations

Welcome to Section 3: HTML & CSS Foundations. This section builds directly on the version control skills you learned in Section 2. You'll learn how to build and style web pages, creating a professional portfolio project that demonstrates your HTML and CSS skills.

This is a **level 2 understanding**—enough to grasp the "why" behind web development practices and develop professional habits. By the end, you'll understand how HTML and CSS work together, why semantic HTML matters, how CSS styling works, and you'll have hands-on experience building a complete web project.

---

## What to Expect

In this section, you will:

- Learn HTML document structure and semantic elements
- Understand how HTML and CSS work together
- Build web pages with proper structure and styling
- Use browser developer tools for debugging
- Create responsive, accessible web pages
- **Continue working in your repository from Section 2** (portfolio project)
- Maintain professional Git workflow throughout
- Build a complete Client Meeting Scheduler project

**Important:** All your work in this section continues in the same repository you created in Section 2. This repository is becoming a portfolio piece, not a collection of throwaway demos. Every exercise builds on the previous one.

---

## Prerequisites

Before starting this section, make sure you have:

- ✅ **Completed Section 2: Version Control Foundations**
  - You should have a repository in your `knowledge-base/projects/` folder
  - You understand Git workflow (status, add, commit, push)
  - You're comfortable using VS Code terminal with Git Bash

- ✅ **VS Code installed** (from Orientation)
- ✅ **Live Server extension** (we'll install this in Exercise 1 if needed)

If you haven't completed Section 2, go back and complete it first. The repository you created there is essential for this section.

---

## How Browsers Work

Before we dive into HTML and CSS, it's important to understand how browsers process web pages. This understanding will help you debug issues and write better code.

When you visit a webpage, your browser:

1. **Downloads the HTML file** from the server
2. **Parses the HTML** - Reads the structure and creates a Document Object Model (DOM)
3. **Downloads linked resources** - CSS files, images, etc.
4. **Applies CSS** - Matches selectors to elements and applies styles
5. **Renders the page** - Displays the final visual result

**HTML** provides the structure and content (what's on the page). **CSS** provides the presentation (how it looks). They work together: HTML elements are styled by CSS rules.

Understanding this process helps you debug why styles aren't applying, understand the cascade and specificity, use developer tools effectively, and write more efficient code.

Now that you understand how browsers work, you're ready to create your first webpage. Complete **[[s3-html-css/s3e1-creating-first-webpage|Exercise 1: Creating Your First Webpage]]** to build the foundation.

---

## HTML Document Structure

HTML (HyperText Markup Language) is the foundation of every web page. It provides the structure and content that browsers display.

Every HTML document follows this structure:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <!-- Page settings and metadata -->
  </head>
  <body>
    <!-- Visible content -->
  </body>
</html>
```

- **`<!DOCTYPE html>`** - Tells the browser to use modern HTML5 standards
- **`<html>`** - The root element that wraps everything
- **`<head>`** - Contains page settings, metadata, and links to CSS
- **`<body>`** - Contains all visible content

For responsive design, every HTML document should include a viewport meta tag in the `<head>` section. This tells mobile browsers to use the device width, enabling responsive design.

Semantic HTML uses elements that describe their meaning, not just their appearance. For example, `<header>` for page headers, `<nav>` for navigation, and `<footer>` for page footers. Semantic HTML improves accessibility, SEO, and code maintainability.

Now that you understand HTML structure, complete **[[s3-html-css/s3e1-creating-first-webpage|Exercise 1: Creating Your First Webpage]]** to create your first HTML document.

---

## HTML Content Elements

HTML provides many elements for adding content to your pages.

**Text elements** include headings (`<h1>` through `<h6>`) for creating hierarchy, paragraphs (`<p>`) for body text, and strong/emphasis (`<strong>`, `<em>`) for important or emphasized text.

**Hyperlinks** (`<a href="url">`) create clickable links. You can link to other pages on your site (internal), other websites (external), or sections on the same page (anchors).

**Lists** organize information. Ordered lists (`<ol>`) create numbered lists, while unordered lists (`<ul>`) create bulleted lists. List items (`<li>`) are the individual items in lists.

**Images** (`<img src="path" alt="description">`) display pictures. The `src` attribute specifies the image file, and the `alt` attribute provides a text description that's essential for accessibility.

**Embedded content** includes `<iframe>` for embedding external content (videos, maps), and `<audio>` and `<video>` for media content.

Always include `alt` text for images, use descriptive link text (not "click here"), ensure proper heading hierarchy, and use semantic elements when possible.

Now that you understand content elements, complete **[[s3-html-css/s3e2-adding-rich-content-elements|Exercise 2: Adding Rich Content Elements]]** to add links, lists, images, and embedded content to your page.

---

## Structured Data with Tables

Tables organize data into rows and columns, making information easy to scan and understand.

Tables use semantic elements: `<table>` for the container, `<caption>` for the table title, `<thead>` for header rows, `<tbody>` for body rows, `<tr>` for table rows, `<th>` for header cells, and `<td>` for data cells.

Tables are perfect for tabular data like schedules, comparisons, and statistics—any structured information that benefits from rows and columns.

Now that you understand tables, complete **[[s3-html-css/s3e3-creating-tables|Exercise 3: Creating Tables]]** to add structured data to your page.

---

## Collecting User Input with Forms

Forms allow users to submit data to your website. They're essential for contact forms, search boxes, login pages, and more.

Forms use various input types: `text` for single-line text, `email` for email addresses (with validation), `password` for hidden input, `number` for numeric input, `checkbox` for multiple selections, and `radio` for single selections.

For accessibility, always use `<label>` elements associated with inputs (using `for` and `id` attributes), use appropriate `type` attributes for validation, include `required` attribute for mandatory fields, and provide clear error messages.

Now that you understand forms, complete **[[s3-html-css/s3e4-creating-forms|Exercise 4: Creating Forms]]** to add user input capabilities to your page.

---

## Semantic HTML Structure

Semantic HTML uses elements that describe their meaning, making your code more maintainable and accessible.

**ID and class attributes** help organize and style elements. `id` is a unique identifier for a single element, while `class` is a reusable identifier for multiple elements. Use IDs for unique elements (like header, main content) and classes for repeated patterns (like buttons, cards).

**Semantic elements** include `<header>` for page or section headers, `<footer>` for page or section footers, `<nav>` for navigation menus, `<section>` for thematic grouping of content, `<article>` for independent, reusable content, and `<main>` for the main content area.

**Additional semantic elements** include `<time>` for dates/times (with `datetime` attribute) and `<abbr>` for abbreviations (with `title` attribute for full text).

Use semantic elements instead of generic `<div>` when possible, maintain proper heading hierarchy, use IDs and classes meaningfully (not just for styling), and ensure accessibility with proper element choice.

Now that you understand semantic HTML, complete **[[s3-html-css/s3e5-using-semantic-html-structure|Exercise 5: Using Semantic HTML Structure]]** to improve your page structure.

---

## Introduction to CSS

CSS (Cascading Style Sheets) controls how HTML elements look. It separates presentation from structure, making your code more maintainable.

**How HTML and CSS work together:** HTML provides the structure (elements), CSS targets those elements with selectors, CSS applies styles (colors, fonts, layout), and the browser renders the styled page.

**Three ways to add CSS:** Inline styles use the `style` attribute directly on elements (quick for one-off styles, but not reusable). Internal styles use a `<style>` tag in `<head>` (good for single-page styles). External stylesheets use a separate `.css` file linked in `<head>` (best practice for most projects—reusable, maintainable, organized).

**The CSS Box Model:** Every HTML element is a box with four areas: content (the actual element content), padding (space inside the border), border (the border around the element), and margin (space outside the border). Understanding the box model is essential for layout and spacing.

**Browser Developer Tools** let you inspect and debug your HTML and CSS. You can inspect elements to see HTML structure and applied CSS, view and modify CSS in real-time in the styles panel, see padding, border, and margin in the box model visualization, and test different screen sizes in responsive design mode.

Now that you understand CSS basics, complete **[[s3-html-css/s3e6-introduction-to-css|Exercise 6: Introduction to CSS]]** to add styling to your page and set up proper file organization.

---

## CSS Selectors and Specificity

CSS selectors target HTML elements to apply styles. Understanding selectors and specificity is crucial for writing effective CSS.

**Basic selectors** include element selectors (`p { }` targets all `<p>` elements), ID selectors (`#header { }` targets element with `id="header"`), class selectors (`.button { }` targets elements with `class="button"`), and descendant selectors (`nav a { }` targets `<a>` inside `<nav>`).

**Grouping selectors** lets you apply the same styles to multiple selectors: `h1, h2, h3 { color: blue; }`.

**The CSS Cascade** determines which styles apply when multiple rules target the same element. Source order matters (later rules override earlier ones), specificity matters (more specific selectors override less specific ones), and importance matters (`!important` declarations override others).

**CSS Specificity** is calculated based on selector components. Inline styles are worth 1000 points, IDs are worth 100 points each, classes/attributes/pseudo-classes are worth 10 points each, and elements/pseudo-elements are worth 1 point each. Higher specificity wins when rules conflict.

Developer tools show you which selectors are active, which rules are being overridden, the specificity of each rule, and why styles aren't applying as expected.

Now that you understand selectors and specificity, complete **[[s3-html-css/s3e7-css-selectors|Exercise 7: CSS Selectors]]** to practice targeting elements and understanding the cascade.

---

## CSS Styling Fundamentals

CSS provides extensive control over text, borders, backgrounds, and form styling.

**Text styling** includes font properties (`font-family`, `font-size`, `font-weight`), text properties (`color`, `text-align`, `line-height`), and text decoration (`text-decoration`, `text-transform`).

**Borders and backgrounds** include borders (`border-width`, `border-style`, `border-color`, or shorthand `border`), backgrounds (`background-color`, `background-image`, `background-position`), and border radius (`border-radius` for rounded corners).

**Box Model in Practice:** Understanding padding, margin, and border is essential. Padding creates space inside the border, borders create the border around the element, and margins create space outside the border.

**Form styling** improves user experience. Style input fields (borders, padding, focus states), buttons (colors, hover effects), and labels (spacing, typography).

**CSS Organization:** Organize your CSS for maintainability. Use comments to separate sections, group related styles together, and create logical sections like Typography, Layout, and Forms.

Now that you understand styling fundamentals, complete **[[s3-html-css/s3e8-css-styling-fundamentals|Exercise 8: CSS Styling Fundamentals]]** to style your page and organize your CSS.

---

## CSS Layout and Responsive Design

CSS controls how elements are positioned and displayed on the page.

**Display properties** include `block` (elements take full width, stack vertically), `inline` (elements flow horizontally, respect content width), `inline-block` (combines block and inline behaviors), and `none` (hides element completely).

**Float for layout** moves elements to the left or right, allowing content to wrap around them. Note: Float is legacy technology. Modern CSS uses Flexbox and Grid, but understanding float helps with legacy code and the source material.

**Responsive design** makes pages work on all screen sizes. The viewport meta tag (already added in Exercise 1) is essential. Media queries apply different styles at different screen sizes, allowing you to hide or rearrange content for smaller screens.

**Using Developer Tools:** Test your layouts with responsive design mode (simulate different devices), inspect elements (see computed styles), and use box model visualization (understand spacing).

Now that you understand layout and responsive design, complete **[[s3-html-css/s3e9-css-layout-with-float|Exercise 9: CSS Layout with Float]]** to create page layouts and test responsiveness.

---

## Putting It All Together

You've learned HTML structure, CSS styling, and layout. Now it's time to combine everything into a complete project.

A complete web project requires semantic HTML structure (proper document structure), organized CSS (well-commented, sectioned stylesheets), responsive design (works on all screen sizes), accessibility (alt text, proper labels, semantic elements), professional organization (proper file structure with css/ and images/ folders), and clean code (comments, consistent naming, maintainable structure).

Your capstone project will be a Client Meeting Scheduler—a complete web application that demonstrates all the concepts you've learned.

Now that you're ready, complete **[[s3-html-css/s3e10-capstone-client-meeting-scheduler|Exercise 10: Capstone Project - Client Meeting Scheduler]]** to build your complete project.

---

## Modern Best Practices

As you continue developing, keep these practices in mind:

**HTML Best Practices:** Use semantic HTML elements, maintain proper heading hierarchy, include alt text for all images, use proper form labels, and validate your HTML.

**CSS Best Practices:** Organize CSS with comments and sections, use consistent naming conventions (kebab-case), keep selectors specific but not overly complex, use external stylesheets (not inline styles), and comment complex or non-obvious code.

**File Organization:** Group related files (CSS in `css/` folder, images in `images/` folder), use consistent naming (kebab-case for files), keep structure shallow when possible, and make file names self-explanatory.

**Git Workflow:** Check `git status` before and after changes, commit frequently with clear messages, keep working tree clean, and push regularly to backup work.

**Accessibility:** Semantic HTML improves screen reader support, alt text makes images accessible, proper labels make forms accessible, and color contrast matters for readability.

**Responsive Design:** Always include viewport meta tag, test on multiple screen sizes, use relative units (%, em, rem) when possible, and consider mobile-first approach.

---

## What You'll Accomplish

By completing this section and its exercises, you will have:

- ✅ **HTML document structure** - Created properly structured HTML pages
- ✅ **HTML content elements** - Used headings, paragraphs, links, lists, images
- ✅ **Structured data** - Created tables for organized information
- ✅ **User input** - Built forms for collecting data
- ✅ **Semantic HTML** - Used semantic elements and proper structure
- ✅ **CSS styling** - Applied styles with external stylesheets
- ✅ **CSS selectors** - Targeted elements with various selectors
- ✅ **CSS layout** - Created page layouts with CSS
- ✅ **Responsive design** - Made pages work on all screen sizes
- ✅ **Professional organization** - Maintained proper file structure
- ✅ **Complete project** - Built a Client Meeting Scheduler application
- ✅ **Portfolio-ready work** - Created something you can show employers

---

## Exercises in This Section

Complete these exercises in order to build your HTML and CSS skills:

1. **[[s3-html-css/s3e1-creating-first-webpage|Exercise 1: Creating Your First Webpage]]**
   - Create basic HTML structure
   - Add title, headings, and paragraphs
   - Set up Live Server
   - Preview in browser

2. **[[s3-html-css/s3e2-adding-rich-content-elements|Exercise 2: Adding Rich Content Elements]]**
   - Add hyperlinks, lists, and images
   - Include HTML plug-ins (iframes)
   - Practice accessibility

3. **[[s3-html-css/s3e3-creating-tables|Exercise 3: Creating Tables]]**
   - Create table structure
   - Add semantic table elements
   - Style basic tables

4. **[[s3-html-css/s3e4-creating-forms|Exercise 4: Creating Forms]]**
   - Build form structure
   - Add various input types
   - Include proper labels

5. **[[s3-html-css/s3e5-using-semantic-html-structure|Exercise 5: Using Semantic HTML Structure]]**
   - Use ID and class attributes
   - Implement semantic elements
   - Improve document structure

6. **[[s3-html-css/s3e6-introduction-to-css|Exercise 6: Introduction to CSS]]**
   - Add inline and external CSS
   - Create organized file structure (css/ folder)
   - Understand box model
   - Use developer tools

7. **[[s3-html-css/s3e7-css-selectors|Exercise 7: CSS Selectors]]**
   - Use various selectors
   - Understand cascade and specificity
   - Practice with developer tools

8. **[[s3-html-css/s3e8-css-styling-fundamentals|Exercise 8: CSS Styling Fundamentals]]**
   - Style text, borders, backgrounds
   - Practice box model
   - Organize CSS with comments
   - Style forms

9. **[[s3-html-css/s3e9-css-layout-with-float|Exercise 9: CSS Layout with Float]]**
   - Create page layouts
   - Use float for positioning
   - Add responsive design basics
   - Test with developer tools

10. **[[s3-html-css/s3e10-capstone-client-meeting-scheduler|Exercise 10: Capstone Project - Client Meeting Scheduler]]**
    - Build complete project
    - Combine all concepts
    - Implement best practices
    - Create portfolio-ready work

---

## Next Steps

- [[s3-html-css/s3e10-capstone-client-meeting-scheduler|Exercise 10: Capstone Project - Client Meeting Scheduler]] - Build the complete Client Meeting Scheduler project that brings together everything you've learned in this section.

---

## Navigation

### Section Navigation
- [[index|Home]] - Return to the main course page
- [[s2-vers-ctrl/index|Version Control]] - Previous section
- [[s3-html-css/index|HTML & CSS]] - This page
- [[s4-js/index|JavaScript Basics]] - Next section

### Course Sections
- [[s0-welcome/index|Orientation]] - Get started here
- [[s1-files/index|File Systems]] - Organization principles
- [[s2-vers-ctrl/index|Version Control]] - Git and GitHub basics
- [[s3-html-css/index|HTML & CSS]] - This page
- [[s4-js/index|JavaScript Basics]] - Programming fundamentals
- [[s5-opt-js/index|JavaScript Functions]] - Functions and optimization
- [[s6-adv-js/index|Advanced JavaScript]] - Advanced concepts
- [[s7-tailwind/index|Tailwind CSS]] - Modern styling
- [[s8-tailwind-adv/index|Advanced Tailwind]] - Advanced styling