---
title: "l1e2 creating and tracking files with git"
description: "workbook style play by play for creating the first real file in a repository and understanding git status."
tags: [git, github, beginner, workbook]
draft: false
date: "2026-01-30"
---

# lesson 1 exercise 2: creating and tracking files with git

this exercise continues **directly from exercise 1**.
do not start a new repository.

read each section fully before performing the steps.
assume no instructor is present.

---

## what you are building

in this exercise, you will create your first real project file:

- `index.html`

by the end of this exercise, you will understand how a file moves through git’s basic states:
- untracked
- staged
- committed

this exercise delivers the **same learning goal as the original pdf**, but uses our single-repository workflow and reinforced habits.

---

## starting state (required)

before you begin, your repository should have:

- branch: `main`
- files:
  - `readme.md`

verify this now.

open the vs code terminal and run:

```text
git status
```

you should see:
- on branch main
- working tree clean

if this is not true, stop and return to exercise 1.

---

## step 1: create the index.html file

### what this step does
this creates a new file that git has never seen before.

### instructions
1. make sure your repository folder is open in vs code
2. create a new file named:

```text
index.html
```

3. add the following content to the file:

```html
<html>
  <body>
    <p>this is my first tracked html file.</p>
  </body>
</html>
```

4. save the file

---

## step 2: observe an untracked file

### what this step does
this shows how git reports files it is not tracking yet.

run:

```text
git status
```

### what to look for
git should report:
- an untracked file named `index.html`

this means:
- the file exists
- git sees it
- git is not tracking it yet

no changes have been recorded.

---

## step 3: stage the file

### what this step does
staging tells git:
> “i want this file included in the next commit.”

run:

```text
git add index.html
```

now run:

```text
git status
```

### what to look for
git should now show:
- `index.html` under “changes to be committed”

the file is staged but not saved to history yet.

---

## step 4: commit the file

### what this step does
a commit records a snapshot of the file in the repository history.

run:

```text
git commit -m "create initial index.html"
```

---

## step 5: verify the commit

run:

```text
git status
```

you should see:
- working tree clean
- on branch main

now run:

```text
git log --oneline -1
```

you should see:
- the commit message you just created

this confirms the file is now tracked and saved.

---

## expected state at the end of this exercise

your repository now contains:

- branch: `main`
- files:
  - `readme.md`
  - `index.html`

there are no untracked or staged changes.

---

## why this exercise matters

you have learned:

- git does not track files automatically
- files must be staged before they can be committed
- `git status` tells you exactly where a file is in the process

these ideas will be reused in every future lesson.

---

## transition to exercise 3

in the next exercise, you will create a branch.
no files will change yet.

the goal will be to understand **context**, not content.
