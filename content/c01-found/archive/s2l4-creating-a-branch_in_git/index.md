---
title: "l1e4 creating a branch in git"
description: "workbook style play by play for creating, using, and cleaning up a git branch while protecting main."
tags: [git, github, branching, beginner, workbook]
draft: false
date: "2026-01-30"
---

# lesson 1 exercise 4: creating a branch in git

this exercise continues **directly from exercises 1, 2, and 3**.
you are still working in the same repository.
do not create a new repository.

read the entire exercise before starting.
this is written so you can complete it without an instructor present.

this exercise delivers the same learning objective as the original pdf, but corrects its gaps and sequencing issues fileciteturn10file1.

---

## what you are learning

in this exercise, you will learn:

- what a git branch actually is
- how to list existing branches
- how to create a new branch safely
- how to switch between branches
- how to confirm which branch you are on
- why branches exist to protect `main`

no files will be permanently changed in this exercise.

---

## starting state (required)

before you begin, your repository must be in this state:

- branch: `main`
- files:
  - `readme.md`
  - `index.html`
- local and github repositories are in sync

verify now.

open the vs code terminal and run:

```text
git status
```

you should see:
- on branch main
- working tree clean

if this is not true, stop and complete exercises 1–3 first.

---

## step 1: list existing branches

### what this step does
this shows you which branches already exist and which one is active.

run:

```text
git branch
```

### what to look for
you should see:

```text
* main
```

the asterisk (`*`) marks the branch you are currently on.

at this point, only `main` exists.

---

## step 2: create a new branch

### what this step does
this creates a new branch **without switching to it**.

run:

```text
git branch text-branch
```

now run:

```text
git branch
```

### what to look for
you should see:

```text
* main
  text-branch
```

this means:
- the branch exists
- you are still on `main`

creating a branch does not move you into it.

---

## step 3: switch to the new branch

### what this step does
this changes your working context.

run:

```text
git checkout text-branch
```

now run:

```text
git status
```

### what to look for
git should report:
- on branch text-branch
- working tree clean

you are now working on the branch.

---

## step 4: understand branch isolation

### important concept
right now:
- `main` and `text-branch` point to the same files
- no changes have been made yet

branches only diverge **after a commit**.

this is why branches are safe.

---

## step 5: return to main

### what this step does
this confirms that switching branches is safe when no changes exist.

run:

```text
git checkout main
```

now run:

```text
git status
```

### what to look for
you should see:
- on branch main
- working tree clean

nothing changed.

---

## step 6: clean up the branch

this exercise is about **creating and understanding** branches.
the branch is no longer needed.

### instructions
delete the branch while on `main`:

```text
git branch -d text-branch
```

now verify:

```text
git branch
```

### expected result
you should see:

```text
* main
```

only `main` remains.

---

## expected state at the end of this exercise

your repository now has:

- one branch: `main`
- unchanged files:
  - `readme.md`
  - `index.html`

no branches were merged.
no files were modified.

---

## why this exercise matters

you have learned:

- branches are lightweight and safe
- creating a branch does not affect main
- switching branches only changes context
- branches should be deleted when no longer needed
- `git status` confirms safety before every action

these ideas are essential for collaboration.

---

## transition to exercise 5

in the next exercise, you will:
- create a branch
- make real changes on it
- switch between branches
- observe files appear and disappear

this will demonstrate **true branch isolation**.
