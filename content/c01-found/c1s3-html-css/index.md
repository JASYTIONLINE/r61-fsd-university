---
title: "C1S3: HTML & CSS Foundations"
description: Comprehensive introduction to HTML and CSS, building web pages from structure to styling, culminating in a complete project.
tags:
  - html
  - css
  - web-development
  - beginner
  - fundamentals
draft: false
date: 2026-01-30
---
# C1S3: HTML & CSS Foundations
In this section, you will move from managing code to actually creating what users see in a browser. You will learn how web pages are structured using HTML and how they are styled and laid out using CSS. 
## Getting Started
### Prerequisites

Before starting this section, make sure you have:

- ✅ **Completed Section 2: Version Control Foundations**
  - You should have a repository in your `knowledge-base/projects/` folder
  - You understand Git workflow (status, add, commit, push)
  - You're comfortable using VS Code terminal with Git Bash

- ✅ **VS Code installed** (from Orientation)
- ✅ **Live Server extension** (we'll install this in Exercise 1 if needed)

If you haven't completed Section 2, go back and complete it first. The repository you created there is essential for this section.
### What to Expect
In this section, you will:

- Learn HTML document structure and semantic elements
- Understand how HTML and CSS work together
- Build web pages with proper structure and styling
- Use browser developer tools for debugging
- Create responsive, accessible web pages
- **Continue working in your repository from Section 2** (portfolio project)
- Maintain professional Git workflow throughout
- Build a complete Client Meeting Scheduler project
-  By the end of this section, you will understand how websites are built from the ground up and will have created a clean, structured, and beautifully styled web page that can serve as the foundation of your professional portfolio.

**Important:** All your work in this section continues in the same repository you created in Section 2. This repository is becoming a portfolio piece.  I highly recommend following the storage location recommendations in these lectures as all links depend on files being in the right place.  Every page builds on the pages before, and most are interconnected.

---
## 1. How Browsers Work
Before we dive into [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) and [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS), it's important to understand how a [web browser](https://developer.mozilla.org/en-US/docs/Glossary/Browser) processes web pages. This understanding will help you [debug](https://www.bing.com/ck/a?!&&p=69031b31a1acec92758683b7cd6319b1fe05ba985badef5c1749a3f8901e436dJmltdHM9MTc3MDk0MDgwMA&ptn=3&ver=2&hsh=4&fclid=07f802bb-eb29-6f86-2b0a-1404ea816ee4&u=a1aHR0cHM6Ly9lbi53aWtpcGVkaWEub3JnL3dpa2kvRGVidWdnaW5n) issues and write better code.

When you visit a webpage, your browser:

1. **Downloads the HTML file** from the [server](https://developer.mozilla.org/en-US/docs/Learn_web_development/Howto/Web_mechanics/What_is_a_web_server)
2. [Parses](https://www.bing.com/ck/a?!&&p=2a21e9f9cf1e29f021d9821076f3823d045d8ce3ee8268aa59fb3d383b67ac93JmltdHM9MTc3MDk0MDgwMA&ptn=3&ver=2&hsh=4&fclid=07f802bb-eb29-6f86-2b0a-1404ea816ee4&u=a1aHR0cHM6Ly9lbi53aWtpcGVkaWEub3JnL3dpa2kvUGFyc2luZw) the HTML** - Reads the structure and creates a Document Object Model (DOM)
3. **Downloads linked resources** - CSS files, images, etc.
4. **Applies CSS** - Matches [selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Selectors) to [elements](https://developer.mozilla.org/en-US/docs/Glossary/Element) and applies [styles](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics)
5. [Renders](https://terminalnotes.com/how-browsers-work-understanding-rendering-parsing-and-repainting/) the page and displays the final visual result

**HTML** provides the structure and content (what's on the page). **CSS** provides the presentation (how it looks). They work together: HTML elements are styled by CSS rules.

Understanding this process helps you debug why styles aren't applying, understand the cascade and specificity, use developer tools effectively, and write more efficient code.

---
## HTML Document Structure

HTML (Hypertext Markup Language) is the foundation of every web page. It provides the structure and content that browsers display.

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
![[vsc-meta-mob.png]]
Semantic HTML uses elements that describe their meaning, not just their appearance. For example, `<header>` for page headers, `<nav>` for navigation, and `<footer>` for page footers. Semantic HTML improves accessibility, SEO, and code maintainability.

Now that you understand HTML structure, complete [Exercise 1: Creating Your First Webpage](s3e1-first-page.md) to create your first HTML document.

---
## 2. HTML Content Elements
[HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)  provides many elements for adding content to your pages.

Text [elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/Heading_Elements) include headings (`<h1>` through `<h6>`)for creating hierarchy, [paragraphs (`<p>`)](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/p) for body text, and strong/emphasis ([`<strong>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/strong), [`<em>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/em) for important or emphasized text.

**Hyperlinks** [(`<a href="url">`)](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/a) create clickable links. You can link to other pages on your site (internal), other websites (external), or sections on the same page (anchors).

**Lists** organize information. Ordered lists [(`<ol>`)](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/ol) create numbered lists, while unordered lists [(`<ul>`)](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/ul) create bulleted lists. List items [(`<li>`)](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/li) are the individual items in lists.

**Images** [(`<img src="path" alt="description">`)](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/img) display pictures. The [`src`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/src) attribute specifies the image file, and the `alt` attribute provides a text description that's essential for accessibility.

**Embedded content** includes [`<iframe>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/iframe) for embedding external content (videos, maps), and [`<audio>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/audio) and[`<video>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/video) for media content.

Always include [`alt` text](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/alt) for images, use descriptive link text (not "click here"), ensure proper heading hierarchy, and use [semantic elements](https://developer.mozilla.org/en-US/docs/Glossary/Semantics) when possible.

Now that you have a basic understanding content [elements](https://developer.mozilla.org/en-US/docs/Glossary/Element), complete [Exercise 2: Adding Rich Content Elements](s3e2-elements.md) to add links, lists, images, and embedded content to your page.

---
## 3. Structured Data with Tables

Tables organize data into rows and columns, making information easy to scan and understand.

Tables use semantic elements: [`<table>`](http://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/table) for the container, [`<caption>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/caption) for the table title, [`<thead>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/thead) for header rows, [`<tbody>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/tbody) for body rows, [`<tr>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/tr) for table rows, [`<th>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/th) for header cells, and [`<td>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/td) for data cells.

Tables are perfect for tabular data like schedules, comparisons, and statistics—any structured information that benefits from rows and columns.

Now that you understand tables, complete [Exercise 3: Creating Tables](s3e3-tables.md) to add structured data to your page.

---

## 4. Collecting User Input with Forms

Forms allow users to submit data to your website. They're essential for contact forms, search boxes, login pages, and more.

Forms use various input types: `text` for single-line text, `email` for email addresses (with validation), `password` for hidden input, `number` for numeric input, `checkbox` for multiple selections, and `radio` for single selections.

For accessibility, always use `<label>` elements associated with inputs (using `for` and `id` attributes), use appropriate `type` attributes for validation, include `required` attribute for mandatory fields, and provide clear error messages.

Now that you understand forms, complete [Exercise 4: Creating Forms](s3e4-forms.md) to add user input capabilities to your page.

---

## 5. Semantic HTML Structure

Semantic HTML uses elements that describe their meaning, making your code more maintainable and accessible.

**ID and class attributes** help organize and style elements. `id` is a unique identifier for a single element, while `class` is a reusable identifier for multiple elements. Use IDs for unique elements (like header, main content) and classes for repeated patterns (like buttons, cards).

**Semantic elements** include `<header>` for page or section headers, `<footer>` for page or section footers, `<nav>` for navigation menus, `<section>` for thematic grouping of content, `<article>` for independent, reusable content, and `<main>` for the main content area.

**Additional semantic elements** include `<time>` for dates/times (with `datetime` attribute) and `<abbr>` for abbreviations (with `title` attribute for full text).

Use semantic elements instead of generic `<div>` when possible, maintain proper heading hierarchy, use IDs and classes meaningfully (not just for styling), and ensure accessibility with proper element choice.

Now that you understand semantic HTML, complete [Exercise 5: Using Semantic HTML Structure](s3e5-semantic.md) to improve your page structure.

---
## 6. Introduction to CSS

CSS (Cascading Style Sheets) controls how HTML elements look. It separates presentation from structure, making your code more maintainable.

**How HTML and CSS work together:** HTML provides the structure (elements), CSS targets those elements with selectors, CSS applies styles (colors, fonts, layout), and the browser renders the styled page.

**Three ways to add CSS:** Inline styles use the `style` attribute directly on elements (quick for one-off styles, but not reusable). Internal styles use a `<style>` tag in `<head>` (good for single-page styles). External stylesheets use a separate `.css` file linked in `<head>` (best practice for most projects—reusable, maintainable, organized).

**The CSS Box Model:** Every HTML element is a box with four areas: content (the actual element content), padding (space inside the border), border (the border around the element), and margin (space outside the border). Understanding the box model is essential for layout and spacing.

**Browser Developer Tools** let you inspect and debug your HTML and CSS. You can inspect elements to see HTML structure and applied CSS, view and modify CSS in real-time in the styles panel, see padding, border, and margin in the box model visualization, and test different screen sizes in responsive design mode.

Now that you understand CSS basics, complete [Exercise 6: Introduction to CSS](s3e6-css-intro.md) to add styling to your page and set up proper file organization.

---
## 7. CSS Selectors and Specificity

CSS selectors target HTML elements to apply styles. Understanding selectors and specificity is crucial for writing effective CSS.

**Basic selectors** include element selectors (`p { }` targets all `<p>` elements), ID selectors (`#header { }` targets element with `id="header"`), class selectors (`.button { }` targets elements with `class="button"`), and descendant selectors (`nav a { }` targets `<a>` inside `<nav>`).

**Grouping selectors** lets you apply the same styles to multiple selectors: `h1, h2, h3 { color: blue; }`.

**The CSS Cascade** determines which styles apply when multiple rules target the same element. Source order matters (later rules override earlier ones), specificity matters (more specific selectors override less specific ones), and importance matters (`!important` declarations override others).

**CSS Specificity** is calculated based on selector components. Inline styles are worth 1000 points, IDs are worth 100 points each, classes/attributes/pseudo-classes are worth 10 points each, and elements/pseudo-elements are worth 1 point each. Higher specificity wins when rules conflict.

Developer tools show you which selectors are active, which rules are being overridden, the specificity of each rule, and why styles aren't applying as expected.

Now that you understand selectors and specificity, complete [Exercise 7: CSS Selectors](s3e7-css-selectors.md) to practice targeting elements and understanding the cascade.

---
## 8. CSS Styling Fundamentals

CSS provides extensive control over text, borders, backgrounds, and form styling.

**Text styling** includes font properties (`font-family`, `font-size`, `font-weight`), text properties (`color`, `text-align`, `line-height`), and text decoration (`text-decoration`, `text-transform`).

**Borders and backgrounds** include borders (`border-width`, `border-style`, `border-color`, or shorthand `border`), backgrounds (`background-color`, `background-image`, `background-position`), and border radius (`border-radius` for rounded corners).

**Box Model in Practice:** Understanding padding, margin, and border is essential. Padding creates space inside the border, borders create the border around the element, and margins create space outside the border.

**Form styling** improves user experience. Style input fields (borders, padding, focus states), buttons (colors, hover effects), and labels (spacing, typography).

**CSS Organization:** Organize your CSS for maintainability. Use comments to separate sections, group related styles together, and create logical sections like Typography, Layout, and Forms.

Now that you understand styling fundamentals, complete [Exercise 8: CSS Styling Fundamentals](s3e8-css-styling.md) to style your page and organize your CSS.

---
## 9. CSS Layout and Responsive Design

CSS controls how elements are positioned and displayed on the page.

**Display properties** include `block` (elements take full width, stack vertically), `inline` (elements flow horizontally, respect content width), `inline-block` (combines block and inline behaviors), and `none` (hides element completely).

**Float for layout** moves elements to the left or right, allowing content to wrap around them. Note: Float is legacy technology. Modern CSS uses Flexbox and Grid, but understanding float helps with legacy code and the source material.

**Responsive design** makes pages work on all screen sizes. The viewport meta tag (already added in Exercise 1) is essential. Media queries apply different styles at different screen sizes, allowing you to hide or rearrange content for smaller screens.

**Using Developer Tools:** Test your layouts with responsive design mode (simulate different devices), inspect elements (see computed styles), and use box model visualization (understand spacing).

Now that you understand layout and responsive design, complete **[Exercise 9: CSS Layout with Float](s3e9-css-layout.md) to create page layouts and test responsiveness.

---
## 10. Putting It All Together
Capstone Project - Client Meeting Scheduler

You've learned HTML structure, CSS styling, and layout. Now it's time to combine everything into a complete project.

A complete web project requires semantic HTML structure (proper document structure), organized CSS (well-commented, sectioned stylesheets), responsive design (works on all screen sizes), accessibility (alt text, proper labels, semantic elements), professional organization (proper file structure with css/ and images/ folders), and clean code (comments, consistent naming, maintainable structure).

Your capstone project will be a Client Meeting Scheduler—a complete web application that demonstrates all the concepts you've learned.

Now that you're ready, complete **[Exercise 10: Capstone Project - Client Meeting Scheduler](s3e10-capstone.md) to build your complete project.

---
## 11. Wrap Up
Modern Best Practices

As you continue developing, keep these practices in mind:

**HTML Best Practices:** Use semantic HTML elements, maintain proper heading hierarchy, include alt text for all images, use proper form labels, and validate your HTML.

**CSS Best Practices:** Organize CSS with comments and sections, use consistent naming conventions (kebab-case), keep selectors specific but not overly complex, use external stylesheets (not inline styles), and comment complex or non-obvious code.

**File Organization:** Group related files (CSS in `css/` folder, images in `images/` folder), use consistent naming (kebab-case for files), keep structure shallow when possible, and make file names self-explanatory.

**Git Workflow:** Check `git status` before and after changes, commit frequently with clear messages, keep working tree clean, and push regularly to backup work.

**Accessibility:** Semantic HTML improves screen reader support, alt text makes images accessible, proper labels make forms accessible, and color contrast matters for readability.

**Responsive Design:** Always include viewport meta tag, test on multiple screen sizes, use relative units (%, em, rem) when possible, and consider mobile-first approach.

---
## What You've Accomplished

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
#### Next Steps: [Section 04: Fundamentals of JavaScript](c01-found/c1s4-js/index)
JavaScript gives you the core building blocks of modern web development, teaching you how variables, functions, conditionals, and logic work together to create interactive, dynamic behavior in your applications.

---
[Back to the top](#Getting%20Started)
## Navigation
Exercises in This Section

Complete these exercises in order to build your HTML and CSS skills:

1. **[Exercise 1: Creating Your First Webpage](s3e1-first-page.md)
   - Create basic HTML structure
   - Add title, headings, and paragraphs
   - Set up Live Server
   - Preview in browser

2. [Exercise 2: Adding Rich Content Elements](s3e2-elements.md)
   - Add hyperlinks, lists, and images
   - Include HTML plug-ins (iframes)
   - Practice accessibility

3. [Exercise 3: Creating Tables](s3e1-first-page.md)
   - Create table structure
   - Add semantic table elements
   - Style basic tables

4. **[Exercise 4: Creating Forms](s3e4-forms.md)
   - Build form structure
   - Add various input types
   - Include proper labels

5. [Exercise 5: Using Semantic HTML Structure](s3e5-semantic.md)
   - Use ID and class attributes
   - Implement semantic elements
   - Improve document structure

6. [Exercise 6: Introduction to CSS](s3e6-css-intro.md)
   - Add inline and external CSS
   - Create organized file structure (css/ folder)
   - Understand box model
   - Use developer tools

7. [Exercise 7: CSS Selectors](s3e7-css-selectors.md)
   - Use various selectors
   - Understand cascade and specificity
   - Practice with developer tools

8. [Exercise 8: CSS Styling Fundamentals](s3e8-css-styling.md)
   - Style text, borders, backgrounds
   - Practice box model
   - Organize CSS with comments
   - Style forms

9. [Exercise 9: CSS Layout with Float](s3e9-css-layout.md)
   - Create page layouts
   - Use float for positioning
   - Add responsive design basics
   - Test with developer tools

1. **[Exercise 10: Capstone Project - Client Meeting Scheduler](s3e10-capstone.md)
   - Build complete project
   - Combine all concepts
   - Implement best practices
   - Create portfolio-ready work
	
---
### Global Navigation

- [HOME:](index) JASYTI's Full Stack Development Foundations Course -
- [Course 01:](c01-found/index) Foundations of Front End Development
- [Course 02:](c02-genai-fun/index.md) Fundamentals of Generative AI
- [Course 03:](c03-fe-react/index.md) Designing a Dynamic Frontend with React
- [Course 04:](c04-genai-design/index.md) Harnessing Gen AI: From Design to Code Optimization
- [Course 05:](c05-data/index) Understanding Data Structures and Algorithms
- [Course 06:](c06-mongol/index) Using MongoDB to Design and Manage Databases
- [Course 07:](c07-express/index) Developing a Reliable Back-end with Node and Express
- [Course:08](c08-ai-test/index) The Power of Generative AI Software Testing
- [Course 09:](c09-publish/index) Publishing your Website to the Live Internet