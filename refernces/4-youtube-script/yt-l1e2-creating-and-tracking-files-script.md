---
title: "youtube l1e2 creating and tracking files with git"
description: "youtube script with screen directions and cut notes for lesson 1 exercise 2 creating and tracking files with git."
tags: [youtube, git, github, beginner]
draft: false
date: "2026-01-30"
---

# lesson 1 exercise 2 video script
## creating and tracking files with git

this script is designed to be followed line by line while recording.
it assumes the viewer completed exercise 1.

---

## intro (0:00–0:25)

**on screen:**  
vs code open with the repository folder visible

**narration:**  
in the last exercise, we created and cloned a github repository.  
in this exercise, we will create our first real file and learn how git tracks it.

**cut note:**  
hard cut. no background music.

---

## section 1 — confirm starting state (0:26–0:50)

**on screen:**  
vs code terminal

**on screen (type):**
```text
git status
```

**narration:**  
before doing anything, we check git status.  
this tells us where we are and whether it is safe to continue.

**callout:**  
on branch main, working tree clean

---

## section 2 — create index.html (0:51–1:40)

**on screen:**  
vs code file explorer

**narration:**  
now we will create our first project file.  
git does not track files automatically, so this file will start untracked.

**on screen:**  
create new file named `index.html`

**on screen:**  
editor view

**on screen (type):**
```html
<html>
  <body>
    <p>this is my first tracked html file.</p>
  </body>
</html>
```

**narration:**  
save the file.

---

## section 3 — observe an untracked file (1:41–2:10)

**on screen:**  
vs code terminal

**on screen (type):**
```text
git status
```

**narration:**  
git now reports index.html as untracked.  
this means git sees the file, but it is not part of the project history yet.

---

## section 4 — stage the file (2:11–2:45)

**on screen (type):**
```text
git add index.html
```

**on screen (type):**
```text
git status
```

**narration:**  
staging tells git that this file should be included in the next commit.

**callout:**  
changes to be committed

---

## section 5 — commit the file (2:46–3:15)

**on screen (type):**
```text
git commit -m "create initial index.html"
```

**narration:**  
a commit records a snapshot of the file in the repository history.

---

## section 6 — verify the commit (3:16–3:45)

**on screen (type):**
```text
git status
```

**narration:**  
the working tree is clean again.

**on screen (type):**
```text
git log --oneline -1
```

**narration:**  
this confirms the commit exists.

---

## outro (3:46–4:05)

**on screen:**  
vs code split view showing file explorer and terminal

**narration:**  
you have created your first tracked file and committed it correctly.  
in the next exercise, we will create a branch.

**cut note:**  
end clean.

---

## off camera qa checklist

- git status shown before any changes  
- untracked file state visible  
- staged state visible  
- clean working tree confirmed  
- commit visible in git log
