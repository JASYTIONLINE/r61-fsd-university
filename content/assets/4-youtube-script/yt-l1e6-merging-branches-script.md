---
title: "youtube l1e6 merging branches in git"
description: "youtube script with screen directions and cut notes for lesson 1 exercise 6 merging branches, pushing to github, and cleanup."
tags: [youtube, git, github, beginner]
draft: false
date: "2026-01-30"
---

# lesson 1 exercise 6 video script
## merging branches, push, and cleanup

this script is designed to be followed line by line while recording.
it mirrors the workbook play by play exactly.
assume the viewer completed exercises 1 through 5.

---

## intro (0:00–0:35)

**on screen:**  
vs code open with repository folder visible

**narration:**  
this is the final exercise of lesson 1.  
we will merge our branch work into main, clean up temporary files, and finish with a professional repository.

**cut note:**  
hard cut. no background music.

---

## section 1 — confirm starting state (0:36–1:00)

**on screen:**  
vs code terminal

**on screen (type):**
```text
git status
```

**narration:**  
before merging, we always confirm our state.  
we should be on main with a clean working tree.

**callout:**  
on branch main, working tree clean

---

## section 2 — confirm the branch exists (1:01–1:25)

**on screen (type):**
```text
git branch
```

**narration:**  
we confirm that the feature branch still exists before merging.

**callout:**  
main and text-branch listed

---

## section 3 — inspect the branch contents (1:26–2:05)

**on screen (type):**
```text
git checkout text-branch
git status
```

**on screen:**  
vs code file explorer

**narration:**  
on the branch, we confirm the file created in the previous exercise exists.

**callout:**  
branch-test.html visible

---

## section 4 — verify the branch commit (2:06–2:25)

**on screen (type):**
```text
git log --oneline -1
```

**narration:**  
this confirms the work we intend to merge is real.

---

## section 5 — switch back to main (2:26–2:50)

**on screen (type):**
```text
git checkout main
git status
```

**on screen:**  
vs code file explorer

**narration:**  
back on main, the branch-only file disappears.  
this confirms isolation one last time.

---

## section 6 — merge the branch into main (2:51–3:35)

**on screen (type):**
```text
git merge text-branch
```

**on screen (type):**
```text
git status
```

**on screen:**  
vs code file explorer

**narration:**  
after the merge, the file appears on main.  
this is the merge payoff.

---

## section 7 — remove the temporary learning file (3:36–4:30)

**on screen (type):**
```text
del branch-test.html
```

**on screen (type):**
```text
git status
```

**narration:**  
we remove the file because it was created only to demonstrate branching.

**on screen (type):**
```text
git add -a
git commit -m "remove temporary branch-test file"
```

---

## section 8 — verify cleanup (4:31–4:55)

**on screen (type):**
```text
git status
git log --oneline -1
```

**narration:**  
the working tree is clean and the cleanup commit is recorded.

---

## section 9 — push main to github (4:56–5:25)

**on screen (type):**
```text
git push -u origin main
```

**on screen:**  
browser showing github repository

**narration:**  
github now reflects the final, cleaned state.

---

## section 10 — delete the branch (5:26–5:50)

**on screen (type):**
```text
git branch -d text-branch
git branch
```

**narration:**  
after merging, the branch is no longer needed.

**callout:**  
only main remains

---

## outro (5:51–6:20)

**on screen:**  
vs code showing final file list

**narration:**  
lesson 1 is complete.  
we started with nothing and finished with a clean, professional repository.

in the next lesson, we will recap what we learned and explain how to read git status as a habit.

**cut note:**  
end clean.

---

## off camera qa checklist

- git status shown before merge  
- branch file confirmed on text-branch  
- file disappears on main before merge  
- file appears on main after merge  
- cleanup commit recorded  
- github verified  
- branch deleted
