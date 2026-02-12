---
title: "youtube l1e4 creating a branch in git"
description: "youtube script with screen directions and cut notes for lesson 1 exercise 4 creating a branch in git."
tags: [youtube, git, github, beginner]
draft: false
date: "2026-01-30"
---

# lesson 1 exercise 4 video script
## creating a branch in git

this script is designed to be followed line by line while recording.
it mirrors the workbook play by play exactly.
assume the viewer completed exercises 1 through 3.

---

## intro (0:00–0:25)

**on screen:**  
vs code open with the repository folder visible

**narration:**  
in this exercise, we will create and explore a git branch.  
the goal is to understand what a branch is and why it protects the main branch.

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
before working with branches, we always confirm our current state.  
we should be on the main branch with a clean working tree.

**callout:**  
on branch main, working tree clean

---

## section 2 — list existing branches (0:51–1:15)

**on screen (type):**
```text
git branch
```

**narration:**  
this command lists all branches.  
the asterisk shows which branch we are currently on.

**callout:**  
only main exists

---

## section 3 — create a new branch (1:16–1:50)

**on screen (type):**
```text
git branch text-branch
```

**narration:**  
this creates a new branch without switching to it.

**on screen (type):**
```text
git branch
```

**callout:**  
main is still active

---

## section 4 — switch to the new branch (1:51–2:20)

**on screen (type):**
```text
git checkout text-branch
```

**on screen (type):**
```text
git status
```

**narration:**  
switching branches changes our working context.  
no files change yet because no commits exist on the branch.

---

## section 5 — explain branch isolation (2:21–2:50)

**on screen:**  
file explorer showing no visible changes

**narration:**  
branches only diverge after a commit.  
right now, both branches point to the same files.

this is why branches are safe.

---

## section 6 — switch back to main (2:51–3:15)

**on screen (type):**
```text
git checkout main
```

**on screen (type):**
```text
git status
```

**narration:**  
switching back to main is safe because no uncommitted changes exist.

---

## section 7 — delete the branch (3:16–3:45)

**on screen (type):**
```text
git branch -d text-branch
```

**on screen (type):**
```text
git branch
```

**narration:**  
branches are temporary tools.  
once we are done learning, we remove them.

---

## outro (3:46–4:05)

**on screen:**  
vs code showing terminal and file explorer

**narration:**  
you have created, explored, and deleted a branch safely.  
in the next exercise, we will use a branch to make real file changes.

**cut note:**  
end clean.

---

## off camera qa checklist

- git status shown before branch work  
- git branch output visible  
- branch creation shown without switching  
- checkout command demonstrated  
- branch deletion confirmed
