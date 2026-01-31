---
title: "l1e6 merging branches in git"
description: "workbook style play by play for merging branch work into main, pushing to github, and cleaning up temporary learning artifacts."
tags: [git, github, merge, branches, beginner, workbook]
draft: false
date: "2026-01-30"
---

# lesson 1 exercise 6: merging branches in git

this exercise continues **directly from exercises 1 through 5**.
you are still working in the same repository.
do not create a new repository and do not reinitialize git.

read the entire exercise before starting.
this is written so you can complete it without an instructor present.

this exercise completes the running theme of lesson 1:
- we started with nothing
- we worked safely on a branch
- now we merge that work into main
- and we finish with a clean, professional repository

---

## what you are learning

in this exercise, you will learn how to:

- merge a feature branch into `main`
- verify the merge using `git status` and the file explorer
- push the merged `main` branch to github
- delete the feature branch after merging
- remove temporary learning files so the final repository is clean

---

## starting state (required)

before you begin, your repository must be in this state:

- branch: `main`
- working tree clean
- a branch named `text-branch` exists
- `text-branch` contains the file `branch-test.html` from exercise 5

verify now.

open the vs code terminal and run:

```text
git status
```

you should see:
- on branch main
- working tree clean

if you do not have `text-branch`, stop and complete exercise 5 first.

---

## step 1: confirm the branch exists

### what this step does
this prevents you from merging the wrong thing.

run:

```text
git branch
```

### what to look for
you should see both:
- `main`
- `text-branch`

and you should see the asterisk on `main`.

---

## step 2: switch to the branch and confirm the branch file

### what this step does
this confirms the work you intend to merge is real.

run:

```text
git checkout text-branch
git status
```

### what to look for
git should report:
- on branch text-branch
- working tree clean

### visual check (vs code or cursor)
confirm that this file exists in the file explorer:

- `branch-test.html`

---

## step 3: verify the most recent commit on the branch

run:

```text
git log --oneline -1
```

### what to look for
you should see the commit message from exercise 5.
this proves the work exists on this branch.

---

## step 4: switch back to main and confirm isolation

### what this step does
this shows that main does not have the branch-only file yet.

run:

```text
git checkout main
git status
```

### visual check (critical)
in the file explorer:
- `branch-test.html` should **not** be visible

this confirms branch isolation one last time before the merge.

---

## step 5: merge `text-branch` into `main`

### what this step does
this applies the branch commits to `main`.

run:

```text
git merge text-branch
```

now run:

```text
git status
```

### what to look for
you should see:
- on branch main
- working tree clean

### visual check (critical)
in the file explorer:
- `branch-test.html` should now appear

this is the merge payoff.
the file is now part of main because the branch history was merged.

---

## step 6: remove the temporary learning file (clean finish)

### why we do this
we created `branch-test.html` only to demonstrate branch isolation.
the goal of lesson 1 is to end with a clean project that contains only:
- readme.md
- index.html

so we remove the temporary file now, after the merge has proven the concept.

### delete the file (powershell)
run:

```text
del branch-test.html
```

now run:

```text
git status
```

you should see the file listed as deleted.

### stage and commit the cleanup
run:

```text
git add -a
git commit -m "remove temporary branch-test file"
```

### verify the cleanup commit
run:

```text
git status
git log --oneline -1
```

you should see:
- working tree clean
- the cleanup commit message at the top

---

## step 7: push the updated main branch to github

### what this step does
this sends your merged (and cleaned) main branch to github.

run:

```text
git push -u origin main
```

---

## step 8: verify on github

open your repository in a web browser and refresh the page.

confirm you see only:
- readme.md
- index.html

and confirm the most recent commit message matches your cleanup commit.

---

## step 9: delete the feature branch

### what this step does
after a successful merge, the feature branch is no longer needed.

run:

```text
git branch -d text-branch
git branch
```

### what to look for
you should see:

```text
* main
```

only main remains.

---

## expected final state (end of lesson 1)

your repository should now be clean and professional:

```text
main
├── readme.md
└── index.html
```

no extra branches.
no extra learning files.

this is the finish line for lesson 1.
