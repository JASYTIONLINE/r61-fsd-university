---
title: "C1S5: Optimizing JavaScript with Functions"
description: a beginner friendly workbook lesson that introduces git and github by building one clean repository from start to finish.
tags:
  - git
  - github
  - version-control
  - beginner
  - workbook
draft: false
date: 2026-01-30
---

# lesson 1: version control foundations

this lesson is written as a **workbook**, not a quick reference.

assume:
- you are brand new to git and github
- no instructor is present to answer questions
- you are working step by step and reading as you go

take your time. do not skip explanations.

---

## why this lesson matters

if you complete this lesson exactly as written, you will finish with:

- a real github repository
- clean commit history
- professional file naming
- correct branch usage
- a clean main branch

this repository is not practice or disposable.  
it can be shown to prospective employers as evidence that you understand professional version control habits.

this lesson can stand on its own, or it can complement full stack bootcamps and training programs.

---

## how this lesson is structured

lesson 1 is made up of **six connected exercises**.

they are not independent tasks.  
each exercise builds on the previous one.

you will use:
- one repository
- one main branch
- one final set of files

temporary branches and changes are created only to teach concepts, then removed.

at the end of the lesson, your repository will be clean and intentional.

---

## before you begin

### tools you need
- a github account
- vs code installed (or cursor as an alternative)
- an internet connection

### important habit (introduced now)
throughout this lesson, you will run the command:

```text
git status
```

this command:
- never changes anything
- only reports your current state
- is completely safe

you should run it:
- before committing
- before switching branches
- before merging
- before deleting branches

if you are ever unsure what to do next, run `git status` first.

---

## naming rules used in this workbook

all files and branches in this lesson follow these rules:

- lowercase letters only
- no spaces
- use hyphens instead of underscores

these rules prevent errors and match professional standards.

examples you will see:
- readme.md
- index.html
- text-branch

---

## exercise 1: create your repository

### goal
create the single github repository you will use for the rest of lesson 1.

### what you are doing
a repository is a container for files and their history.  
github stores repositories online so they can be shared and reviewed.

### steps
1. log in to github in your web browser
2. create a new repository
3. check the option to initialize the repository with a readme file
4. name the repository appropriately (no spaces, lowercase recommended)
5. clone the repository to your computer
6. open the folder in vs code

when vs code displays a message saying it detected a git repository, **click yes**.  
this allows vs code to show helpful git information.

### verify your work
open the vs code terminal and run:

```text
git status
```

you should see:
- you are on the main branch
- the working tree is clean

at this point, your repository contains one file:
- readme.md

---

## exercise 2: create your first tracked file

### goal
learn how git tracks files and records changes.

### what you are doing
you will create a simple html file and commit it to the repository.

### steps
1. create a file named index.html
2. add minimal html content to the file
3. save the file
4. run `git status` and observe that the file is untracked
5. stage the file
6. run `git status` again and observe the change
7. commit the file with a clear message

### verify your work
after committing, run:

```text
git status
```

you should see:
- working tree clean
- still on the main branch

your repository now contains:
- readme.md
- index.html

---

## exercise 3: create a branch

### goal
understand what a branch is and why it exists.

### what you are doing
a branch allows you to work without affecting the main version of the project.

### steps
1. create a branch named text-branch
2. switch to the new branch
3. run `git status` to confirm your branch

### verify your work
`git status` should show:
- on branch text-branch

your files have not changed yet. only your working context has.

---

## exercise 4: make changes on a branch

### goal
see how branches isolate work.

### what you are doing
you will change index.html on the branch and observe that main is unaffected.

### steps
1. modify index.html on text-branch
2. save the file
3. run `git status` to see the change
4. stage the file
5. commit the change
6. switch back to main

### verify your work
when you return to main:
- index.html should revert to its earlier version
- your changes are not visible

this confirms branch isolation.

---

## exercise 5: merge the branch into main

### goal
apply branch work to the main branch.

### what you are doing
merging takes completed work from a branch and integrates it into main.

### steps
1. confirm you are on main using `git status`
2. merge text-branch into main
3. run `git status` after the merge

### verify your work
- index.html now includes the changes from the branch
- working tree is clean

the branch work is now part of main.

---

## exercise 6: clean up

### goal
leave the repository in a professional state.

### what you are doing
branches are temporary tools. once merged, they should be removed.

### steps
1. delete text-branch
2. confirm only main remains
3. push main to github

### final state
your repository should contain:

```text
main
├── readme.md
└── index.html
```

no extra branches.  
no extra files.

---

## what you accomplished

you have:
- created a real github repository
- tracked files correctly
- used branches safely
- merged work intentionally
- practiced professional habits

this repository is suitable for a portfolio.

---

## moving forward

lesson 1 built the foundation.

future lessons will build on this same repository and workflow.
