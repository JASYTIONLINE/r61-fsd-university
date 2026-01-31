---
title: "l2e1 creating the first webpage"
description: "workbook play by play to build a basic html page in vs code and preview it in a local browser using live server."
tags: [html, css, vs-code, live-server, beginner, workbook]
draft: false
date: "2026-01-30"
---

# lesson 2 exercise 1: creating the first webpage

this exercise is based on the original lesson 02 demo 01, but rewritten so a beginner can succeed without guessing. fileciteturn15file0

this lesson 2 work continues inside the same repository you built in lesson 1. that matters because your repo is becoming a portfolio project, not a pile of throwaway demos.

---

## what you are learning

by the end of this exercise you will be able to:

- explain what an html file is
- edit an existing `index.html` file in vs code or cursor
- preview your page in a browser using live server
- confirm your work visually and with `git status`
- commit your change with a clear message

---

## starting state required

you must start with the repository created in lesson 1.

your repo should currently have:

- `readme.md`
- `index.html`

and you should be on `main` with a clean working tree.

### verify now

open vs code (or cursor) and open your lesson 1 repository folder.

in the integrated terminal, run:

```text
git status
```

you should see:

- on branch `main`
- working tree clean

if you do not see that, stop and fix it before continuing. do not build html on top of a messy repo.

---

## step 1: open index.html and understand what you are editing

### what this step does
`index.html` is the default homepage filename used by many web servers. when you open it in a browser, it becomes the first page a user sees.

### instructions
1. in the vs code file explorer, click `index.html`
2. if the file already has content from lesson 1, that is fine. you are about to replace it with a cleaner first webpage template.

---

## step 2: replace the file with the basic html template

the original pdf tells you to create a new `index.html` and paste this template. we already have `index.html`, so we will edit the existing file and paste the template. fileciteturn15file0

### instructions
1. select all text in `index.html`
2. paste this exact code:

```html
<!doctype html>
<html lang="en">
  <head>
  </head>
  <body>
    <h1>welcome to the first webpage</h1>
  </body>
</html>
```

3. save the file

### what to notice
- `<!doctype html>` tells the browser to use modern html rules.
- `<html>` wraps the whole document.
- `<head>` is for page settings and links. we will use it later.
- `<body>` is what the user actually sees.
- `<h1>` is a large headline.

---

## step 3: confirm you actually saved the change

### visual check
look at the file tab in vs code:

- if you see a dot next to `index.html`, it is not saved yet.
- press `ctrl+s` to save.

### git check
run:

```text
git status
```

you should see `index.html` listed as modified.

this is your first html change tracked by git.

---

## step 4: install live server (one time setup)

the pdf uses the live server extension to preview your page in a browser. this is the easiest way to preview html during learning. fileciteturn15file0

### instructions
1. open the extensions view in vs code
2. search for:

```text
live server
```

3. install the extension named live server (by ritwick dey)

### verify
after install, vs code may ask you to reload. if it does, reload.

note: you only install live server once. after this, you just use it.

---

## step 5: open your page in the browser

### instructions
1. in the file explorer, right click `index.html`
2. click:

- open with live server

your default browser should open a new tab showing your page.

### verify
you should see the headline:

- welcome to the first webpage

if you do not see it:
- confirm the file is saved
- confirm you opened `index.html` with live server (not by double clicking the file in windows)

---

## step 6: commit your work (small, clean history)

we are not teaching git here, but we are keeping professional habits.

### safety check
run:

```text
git status
```

confirm:
- you are on `main`
- only `index.html` is modified

### stage and commit
run:

```text
git add index.html
git commit -m "lesson 2: create first webpage html skeleton"
```

### verify the commit exists
run:

```text
git log --oneline -1
```

you should see your commit message at the top.

---

## end state (what you should have now)

- `index.html` contains a valid html skeleton and a visible headline
- live server can preview the page in your browser
- your work is committed on `main`
- your repo is clean

final safety check:

```text
git status
```

you should see:
- working tree clean

---

## what this sets up for exercise 2

you now have a page that loads reliably.

next, we will start adding:
- more content elements
- structure
- basic styling (css)

this is where the page starts to look like a real website.
