---
title: "youtube l1e1 creating and cloning a github repository"
description: "youtube script with screen directions and cut notes for lesson 1 exercise 1 creating and cloning a github repository."
tags: [youtube, git, github, beginner]
draft: false
date: "2026-01-30"
---

# lesson 1 exercise 1 video script
## creating and cloning a github repository

this script is designed to be followed line by line while recording.
it assumes the viewer is brand new to git and github.

---

## intro (0:00–0:30)

**on screen:**  
web browser on github home page

**narration:**  
in this exercise, we will create a github repository and clone it to our computer.  
this repository will be used throughout the rest of lesson 1.

**cut note:**  
hard cut. no music.

---

## section 1 — create the repository on github (0:31–1:45)

**on screen:**  
github website

**narration:**  
first, we create the repository on github.  
this gives us a place to store our files and their history.

**on screen actions:**  
- click the plus icon  
- select new repository  

**on screen callouts:**  
repository name:
```text
my-first-github-repo
```

**narration:**  
use lowercase letters and no spaces.  
check the option to initialize the repository with a readme file.

**on screen:**  
click create repository

---

## section 2 — review the repository (1:46–2:20)

**on screen:**  
repository page showing readme.md

**narration:**  
github creates the repository and adds a readme file automatically.  
this is our first commit.

---

## section 3 — edit the readme on github (2:21–3:00)

**on screen:**  
click readme.md → edit icon

**on screen (type):**
```text
this repository is part of my version control portfolio.
```

**narration:**  
we make a small change so you can see how commits are recorded.

**on screen:**  
commit directly to main

---

## section 4 — clone the repository (3:01–4:00)

**on screen:**  
click code → https → copy url

**narration:**  
cloning creates a local copy of the repository on your computer.

**on screen:**  
vs code open → terminal → new terminal

**on screen (type):**
```text
git clone https://github.com/[your-github-username]/[your-repository-name].git
```

---

## section 5 — open the repository in vs code (4:01–4:40)

**on screen:**  
vs code file explorer

**narration:**  
open the newly created folder in vs code.

**on screen callout:**  
if vs code asks if you want to open the git repository, click yes.

---

## section 6 — verify the setup (4:41–5:10)

**on screen:**  
vs code terminal

**on screen (type):**
```text
git status
```

**narration:**  
git status tells us where we are and whether everything is clean.

**callout:**  
on branch main, working tree clean

---

## outro (5:11–5:30)

**on screen:**  
vs code showing readme.md and terminal

**narration:**  
you now have a github repository and a local copy on your computer.  
in the next exercise, we will create our first real project file.

**cut note:**  
end clean.

---

## off camera qa checklist

- repository created with readme  
- readme edited on github  
- clone command shown clearly  
- vs code git prompt handled correctly  
- git status confirms clean main branch
