---
title: "l1e7 lesson 1 recap and professional workflow habits"
description: "workbook style recap that ties together all six exercises, reinforces good habits, and prepares learners for html and css."
tags: [git, github, recap, habits, beginner, workbook]
draft: false
date: "2026-01-30"
---

# lesson 1 exercise 7: recap and professional workflow habits

this exercise replaces the original *checking the status of a file* demo and serves as a **full recap of lesson 1**.

instead of introducing new commands or new repositories, this exercise:
- explains **why** you did what you did in exercises 1–6
- reinforces the habits you practiced
- ties everything into one clear mental model
- prepares you to move on to lesson 2 (html and css)

this delivers the **intent** of the original demo without its broken setup, platform issues, or repetition fileciteturn13file0.

---

## what this recap is about

lesson 1 was not about memorizing commands.

it was about learning how to:
- work safely
- understand context
- avoid mistakes
- leave projects clean and professional

this recap explains the **so what** of each exercise.

---

## the repository you built

by the end of exercise 6, your repository reached this final state:

```text
main
├── readme.md
└── index.html
```

this was not accidental.

every file and every deletion served a purpose.

---

## exercise 1 recap: creating and cloning a repository

**what you did**
- created a github repository
- cloned it locally
- opened it in vs code

**so what**
- you learned the difference between local and remote repositories
- you established one project that everything else built on
- you learned that a repository is the container for both files and history

---

## exercise 2 recap: creating and tracking files

**what you did**
- created index.html
- staged it
- committed it

**so what**
- you learned that git does not track files automatically
- you learned the difference between untracked, staged, and committed
- you saw how `git status` reports each state

this is the foundation of all version control work.

---

## exercise 3 recap: pushing to github

**what you did**
- connected your local repository to github
- pushed commits to the remote repository

**so what**
- you learned that commits stay local until you push
- you learned what a remote is and why `origin` exists
- you confirmed that github reflects your real work only after a push

---

## exercise 4 recap: creating a branch

**what you did**
- listed branches
- created a branch
- switched branches
- deleted the branch

**so what**
- you learned that branches are lightweight and safe
- you learned that creating a branch does not change main
- you learned to clean up branches when they are no longer needed

---

## exercise 5 recap: switching branches with real changes

**what you did**
- created a file on a branch
- committed it
- switched back to main

**so what**
- you saw files appear and disappear without being deleted
- you learned that commits belong to branches
- you experienced real branch isolation

this is where branching becomes intuitive.

---

## exercise 6 recap: merging and cleanup

**what you did**
- merged branch work into main
- removed temporary learning files
- deleted the feature branch
- pushed the final state to github

**so what**
- you learned how work becomes part of main
- you learned that cleanup is part of professionalism
- you finished with a repository you can show others

---

## the habits you practiced (the real lesson)

throughout all six exercises, you repeatedly practiced:

### checking context
- running `git status` before risky actions
- confirming which branch you were on

### working incrementally
- making small, intentional changes
- committing with clear messages

### protecting main
- using branches for experiments
- merging only when ready

### cleaning up
- deleting branches after use
- removing temporary learning files

these habits matter more than any single command.

---

## why this matters before html and css

in lesson 2, you will start writing real code.

as your files grow:
- mistakes become easier to make
- changes become harder to track

version control is what keeps that complexity manageable.

because of lesson 1:
- you know how to work safely
- you know how to recover from mistakes
- you know how to keep your project clean

---

## moving forward

lesson 1 taught you **how to work**.

lesson 2 will teach you **what to build**.

from here on, version control is no longer a separate topic.
it is part of everything you do.
