---
title: "youtube l1e3 pushing local changes to github"
description: "youtube script with screen directions and cut notes for lesson 1 exercise 3 pushing local changes to github."
tags: [youtube, git, github, beginner]
draft: false
date: "2026-01-30"
---

# lesson 1 exercise 3 video script
## pushing local changes to github

this script is designed to be read while recording.
it mirrors the workbook play by play exactly.
assume the viewer completed exercises 1 and 2.

---

## intro (0:00–0:25)

**on screen:**  
vs code open with repository folder visible

**narration:**  
in the last exercise, we created and committed our first file locally.  
in this exercise, we will send those commits to github.

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
before pushing anything, we always check git status.  
this confirms we are on the main branch and the working tree is clean.

**callout:**  
on branch main, working tree clean

---

## section 2 — explain remotes (0:51–1:25)

**on screen:**  
diagram or browser showing github vs local computer (optional)

**narration:**  
a remote is a saved connection to a github repository.  
our local repository lives on our computer.  
the remote repository lives on github.

by convention, the main remote is named origin.

---

## section 3 — add the github remote (1:26–2:10)

**on screen:**  
vs code terminal

**on screen (type):**
```text
git remote add origin https://github.com/[your-github-username]/[your-repository-name].git
```

**narration:**  
this command tells git where our github repository is located.

**cut note:**  
pause briefly so viewers can copy the command.

---

## section 4 — verify the remote (2:11–2:35)

**on screen (type):**
```text
git remote -v
```

**narration:**  
this confirms that the remote was added correctly.  
we should see origin listed for both fetch and push.

---

## section 5 — push commits to github (2:36–3:15)

**on screen (type):**
```text
git push -u origin main
```

**narration:**  
this sends our local commits to github and links the main branch.

**callout:**  
main → main

---

## section 6 — verify on github (3:16–3:50)

**on screen:**  
browser showing github repository

**narration:**  
refresh the repository page.  
you should now see readme.md and index.html.

this confirms the push worked.

---

## section 7 — final status check (3:51–4:10)

**on screen:**  
back to vs code terminal

**on screen (type):**
```text
git status
```

**narration:**  
git confirms that the local branch is up to date with origin.

---

## outro (4:11–4:30)

**on screen:**  
vs code split view showing file explorer and terminal

**narration:**  
your local repository and github are now synchronized.  
in the next exercise, we will create a branch.

**cut note:**  
end clean.

---

## off camera qa checklist

- git status shown before push  
- remote added correctly  
- git remote -v verified  
- push output visible  
- github page refreshed showing files
