---
title: "l1e5 switching branches in git"
description: "workbook style play by play for switching branches, making real file changes on a branch, and observing branch isolation."
tags: [git, github, branches, checkout, beginner, workbook]
draft: false
date: "2026-01-30"
---

# lesson 1 exercise 5: switching branches in git

this exercise continues **directly from exercises 1 through 4**.
you are still working in the same repository.
do not create a new repository and do not reinitialize git.

read the entire exercise before starting.
this exercise is written so you can complete it without an instructor present.

this exercise delivers the **intended lesson of the original pdf**, but removes errors, platform-specific tools, and misdirection fileciteturn11file1.

---

## what you are learning

in this exercise, you will learn:

- how switching branches changes what files you see
- how commits belong to a specific branch
- how `git status` confirms which branch you are on
- how to safely move between branches with committed work

this is the exercise where branches become *real*.

---

## starting state (required)

before you begin, your repository must be in this state:

- branch: `main`
- files:
  - `readme.md`
  - `index.html`
- working tree clean
- local and github repositories are in sync

verify now.

open the vs code terminal and run:

```text
git status
```

you should see:
- on branch main
- working tree clean

if this is not true, stop and complete exercises 1–4 first.

---

## step 1: create and switch to a new branch

### what this step does
this creates a safe space to make changes without affecting `main`.

run:

```text
git branch text-branch
git checkout text-branch
```

now verify:

```text
git status
```

### what to look for
git should report:
- on branch text-branch
- working tree clean

---

## step 2: create a file on the branch

### what this step does
this creates a file that will exist **only on this branch**.

to avoid editor confusion, we create the file and content in one step.

run:

```text
echo "<html><body><p> this is a test html file. </p></body></html>" > branch-test.html
```

### visual check (vs code or cursor)
- a new file named `branch-test.html` appears
- the file contains html content

---

## step 3: stage and commit the file

### what this step does
this permanently records the file on `text-branch`.

run:

```text
git status
git add branch-test.html
git commit -m "create branch-only test file"
```

### verify
run:

```text
git status
```

expected:
- on branch text-branch
- working tree clean

---

## step 4: confirm branch-specific history

run:

```text
git log --oneline -1
```

### what to notice
- the commit message reflects the branch work
- this commit does not yet exist on `main`

---

## step 5: switch back to main

### what this step does
this proves that branches can hold different files.

run:

```text
git checkout main
```

now verify:

```text
git status
```

### visual check (critical)
in vs code or cursor:
- `branch-test.html` **disappears** from the file list

this is expected and correct.

---

## step 6: understand what just happened

- the file exists on `text-branch`
- the file does not exist on `main`
- switching branches changed your working folder
- no files were lost

this is the core purpose of branches.

---

## expected state at the end of this exercise

- `main` branch:
  - readme.md
  - index.html

- `text-branch` branch:
  - readme.md
  - index.html
  - branch-test.html

no merges have occurred yet.

---

## why this exercise matters

you have learned:

- commits belong to branches
- switching branches changes visible files
- `git status` confirms your context
- branch isolation protects main

this is the foundation for safe collaboration.

---

## transition to exercise 6

in the next exercise, you will:

- merge branch work into main
- confirm the file appears on main
- delete the branch after merging

this will complete the lesson 1 workflow.
