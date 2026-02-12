---
title: "youtube l1e5 switching branches in git"
description: "youtube script with screen directions and cut notes for lesson 1 exercise 5 switching branches in git."
tags: [youtube, git, github, beginner]
draft: false
date: "2026-01-30"
---

# lesson 1 exercise 5 video script
## switching branches in git

this script is designed to be followed line by line while recording.
it mirrors the workbook play by play exactly.
assume the viewer completed exercises 1 through 4.

---

## intro (0:00–0:30)

**on screen:**  
vs code open with the repository folder visible

**narration:**  
in this exercise, we will switch between branches and watch files appear and disappear.  
this is where branch isolation becomes obvious.

**cut note:**  
hard cut. no background music.

---

## section 1 — confirm starting state (0:31–0:55)

**on screen:**  
vs code terminal

**on screen (type):**
```text
git status
```

**narration:**  
before switching branches, we always check git status.  
we should be on the main branch with a clean working tree.

**callout:**  
on branch main, working tree clean

---

## section 2 — create and switch to the branch (0:56–1:30)

**on screen (type):**
```text
git branch text-branch
git checkout text-branch
```

**on screen (type):**
```text
git status
```

**narration:**  
we create a branch and immediately switch to it.  
git status confirms our context.

---

## section 3 — create a branch-only file (1:31–2:20)

**on screen (type):**
```text
echo "<html><body><p> this is a test html file. </p></body></html>" > branch-test.html
```

**on screen:**  
vs code file explorer

**narration:**  
this file exists only on this branch.

---

## section 4 — stage and commit the file (2:21–2:55)

**on screen (type):**
```text
git status
git add branch-test.html
git commit -m "create branch-only test file"
```

**narration:**  
commits belong to branches.  
this commit exists only on text-branch.

---

## section 5 — verify branch history (2:56–3:15)

**on screen (type):**
```text
git log --oneline -1
```

**narration:**  
this confirms the commit was created on this branch.

---

## section 6 — switch back to main (3:16–3:50)

**on screen (type):**
```text
git checkout main
```

**on screen (type):**
```text
git status
```

**on screen:**  
vs code file explorer

**narration:**  
watch the file list.  
branch-test.html disappears.

this is expected.

---

## section 7 — explain what happened (3:51–4:15)

**on screen:**  
split view showing terminal and file explorer

**narration:**  
the file was not deleted.  
it exists on the branch, not on main.

switching branches changed the working folder.

---

## outro (4:16–4:40)

**on screen:**  
vs code showing main branch

**narration:**  
you have seen real branch isolation in action.  
in the next exercise, we will merge this work into main.

**cut note:**  
end clean.

---

## off camera qa checklist

- git status shown before switching  
- branch creation and checkout shown  
- file appears on branch  
- commit confirmed  
- file disappears on main
