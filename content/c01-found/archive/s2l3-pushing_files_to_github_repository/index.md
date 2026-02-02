---
title: "l1e3 pushing local changes to github"
description: "workbook style play by play for pushing committed local changes to github using the existing repository."
tags: [git, github, beginner, workbook]
draft: false
date: "2026-01-30"
---

# lesson 1 exercise 3: pushing local changes to github

this exercise continues **directly from exercises 1 and 2**.
do not create a new repository.
do not initialize git again.

read the full exercise before starting.
this is written so you can complete it without instructor assistance.

source intent: lesson 01 demo 03 pushing files to github repository fileciteturn9file0

---

## what you are learning

in this exercise, you will learn how to:

- connect your local repository to github
- push committed changes from your computer to github
- verify that local and remote repositories are in sync

this delivers the same learning objective as the original pdf, but using:
- one continuous repository
- files you already created
- habits reinforced earlier

---

## starting state (required)

before you begin, your repository must be in this state:

- branch: `main`
- files:
  - `readme.md`
  - `index.html`
- at least one local commit exists

verify now.

open the vs code terminal and run:

```text
git status
```

you should see:
- on branch main
- working tree clean

if this is not true, stop and complete exercises 1 and 2 first.

---

## step 1: understand what a remote is

a **remote** is a saved connection to a github repository.

- your local repository lives on your computer
- your remote repository lives on github
- git needs to know how to connect the two

by convention, the primary remote is named `origin`.

---

## step 2: add the github repository as a remote

### what this step does
this tells git where your github repository is located.

**important:** replace the placeholder below with your own github username.

```text
git remote add origin https://github.com/[your-github-username]/[your-repository-name].git
```

press enter.

---

## step 3: verify the remote connection

run:

```text
git remote -v
```

### what to look for
you should see:
- `origin` listed for fetch
- `origin` listed for push

this confirms the remote was added correctly.

if you see an error, stop and fix it before continuing.

---

## step 4: push your local commits to github

### what this step does
pushing sends your local commit history to github.

run:

```text
git push -u origin main
```

### what to look for
the output should indicate:
- `main -> main`
- the branch is now tracking `origin/main`

this means your local and remote branches are connected.

---

## step 5: verify on github

### instructions
1. return to your web browser
2. refresh the github repository page

### what to confirm
you should now see:
- `readme.md`
- `index.html`
- the commits you created locally

this confirms the push was successful.

---

## step 6: confirm local status

return to vs code and run:

```text
git status
```

you should see:
- on branch main
- your branch is up to date with `origin/main`
- working tree clean

this confirms local and remote are synchronized.

---

## expected state at the end of this exercise

your repository now has:

- a local copy on your computer
- a matching copy on github
- synchronized commit history

no new files were created in this exercise.
no branches were added.

---

## why this exercise matters

you have learned:

- commits do not automatically go to github
- pushing is a deliberate action
- git status helps confirm safety before and after pushing
- github reflects your real work only after a push

these concepts are essential for collaboration and portfolios.

---

## transition to exercise 4

in the next exercise, you will create a branch.

you will not change files yet.
the focus will be on understanding context.
