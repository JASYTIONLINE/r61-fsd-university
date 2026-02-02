---
title: "l1e1 creating and cloning a github repository"
description: "workbook style play by play for creating and cloning a github repository using one continuous project."
tags: [git, github, beginner, workbook]
draft: false
date: "2026-01-30"
---

# lesson 1 exercise 1: creating and cloning a github repository

this exercise is written so you can complete it **without an instructor present**.
read each section fully before performing the steps.

this exercise is designed to:
- use clear explanations
- avoid unnecessary steps
- fit into one continuous project
- reinforce good habits

---

## what you are building

you are creating **the single repository** that will be used throughout lesson 1.

this repository will eventually contain:
- a readme file
- an index.html file

for now, it will start with only a readme file.

this is intentional.

---

## before you start

make sure you have:
- a github account
- vs code installed (or cursor)
- a working internet connection

open vs code now, but do not open any folders yet.

---

## step 1: create the repository on GitHub

### what this step does
this creates an empty project space on GitHub and adds an initial readme file.

### instructions
1. open a web browser and go to https://github.com
2. log in to your github account
3. click the **+** icon in the top right corner
4. select **new repository**

### repository settings
fill out the form as follows:

- **repository name**:  
  use lowercase letters and no spaces  
  example:
  ```text
  my-first-github-repo
  ```

- **visibility**: public

- **initialize this repository with a readme**: checked

leave all other options at their default values.

click **create repository**.

### verify
you should now see:
- a github page showing your repository
- one file named `readme.md`
- one commit listed

---

## step 2: edit the readme on github

### what this step does
this creates a second commit so you can see how changes are recorded.

### instructions
1. on the repository page, click `readme.md`
2. click the pencil (edit) icon
3. add a short sentence, for example:
   ```text
   this repository is part of my version control portfolio.
   ```
4. scroll down to the commit section
5. enter a commit message describing the change
6. commit directly to the `main` branch

### verify
you should now see:
- two commits listed
- the updated readme content visible

---

## step 3: clone the repository to your computer

### what this step does
cloning creates a local copy of the repository so you can work on files using vs code.

### instructions
1. on github, click the **code** button
2. make sure **https** is selected
3. copy the repository url

### open vs code
1. open vs code
2. open the integrated terminal
3. navigate to the folder where you want your projects stored

### run the clone command

**replace the placeholder with your own github username and repository name**

```text
git clone https://github.com/[your-github-username]/[your-repository-name].git
```

press enter and wait for the command to complete.

### verify
in the terminal, run:
```text
ls
```

you should see a new folder with the same name as your repository.

---

## step 4: open the repository folder

### what this step does
this connects vs code to your git repository.

### instructions
1. in vs code, open the newly created repository folder
2. if vs code asks:
   > i see a git repository in this folder. do you want to open it?
   
   click **yes**

### verify
open the terminal and run:
```text
git status
```

you should see:
- on branch main
- working tree clean

this confirms everything is set up correctly.

---

## expected state at the end of this exercise

your repository now has:

- branch: main
- files:
  - readme.md

no other files or branches exist yet.

this is the correct starting point for exercise 2.

---

## why this matters

you now have:
- a remote repository on github
- a local copy on your computer
- a clean starting state

from here on, every lesson builds on this same project.
