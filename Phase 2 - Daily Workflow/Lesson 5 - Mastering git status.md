# Lesson 5 - Mastering `git status`

## Learning goals

By the end of this lesson, you should be able to explain:

- what `git status` does
- why it is one of the most used Git commands
- the difference between untracked, modified, staged, and committed files
- how Git decides the current state of files
- how to read `git status` output confidently

## What does `git status` do?

`git status` shows the current state of your repository.

It tells you:

- which branch you are on
- whether you have commits or not
- which files are untracked
- which files are modified
- which files are staged
- whether the working tree is clean

## Why is `git status` important?

It helps you avoid mistakes before committing.

Professional developers use it constantly to check:

- what changed
- what is ready to commit
- what is still unfinished

## Basic example

After initializing a repository, you may see something like:

```text
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
```

This means:

- you are on the `main` branch
- there are no commits yet
- there is nothing staged or tracked yet

## File states in Git

A file can be in one of these main states:

### 1. Untracked

Git sees the file, but it has not started tracking it yet.

### 2. Staged

The file has been added with `git add` and is ready for the next commit.

### 3. Committed / Tracked

The file changes are saved in Git history through a commit.

### 4. Modified

A tracked file has been changed again after the last commit.

## File lifecycle

```text
Untracked
   ↓ git add
Staged
   ↓ git commit
Committed / Tracked
   ↓ edit file
Modified
   ↓ git add
Staged again
```

## Real-world analogy

Think of a shopping process:

- Working Directory = store shelf where you choose items
- Staging Area = shopping cart
- Commit = checkout and payment

`git status` tells you what is in your cart and what is still on the shelf.

## Working Directory, Staging Area, and Repository

`git status` compares these three places:

- Working Directory
- Staging Area (Index)
- Last commit (HEAD)

It checks whether the file content is different between them.

## Common outputs

### Clean repository

```text
nothing to commit, working tree clean
```

Meaning: everything is committed and no file has changed.

### Untracked file

```text
Untracked files:
```

Meaning: Git sees a new file that is not being tracked yet.

### Modified file

```text
Changes not staged for commit:
```

Meaning: a tracked file has changed, but the new version has not been staged.

### Staged file

```text
Changes to be committed:
```

Meaning: the change is staged and will be included in the next commit.

## What `git status` does not do

`git status` does **not**:

- change your files
- stage files
- commit files
- push files to GitHub

It only reports information.

## Hands-on lab

Create a test repository and observe the output step by step:

```bash
mkdir Status-Lab
cd Status-Lab
git init
git status
echo Hello > app.txt
git status
git add app.txt
git status
git commit -m "Initial commit"
git status
echo "Git Rocks" >> app.txt
git status
```

## Common mistakes

- ignoring `git status`
- confusing modified files with staged files
- thinking `git status` changes the repository
- forgetting to check status before committing

## Interview question

**Q: What does `git status` do?**

**A:** It shows the current state of the repository, including the branch name, tracked and untracked files, staged changes, modified files, and whether the working tree is clean.

## Mini quiz

1. What does `git status` tell you?
2. What is an untracked file?
3. What does it mean when a file is staged?
4. What does `working tree clean` mean?
5. Does `git status` modify your repository?

## Homework

1. Create a test repository.
2. Add a file and run `git status` after each step.
3. Observe how the output changes after `git add` and `git commit`.

## Next lesson

In Lesson 6, we will learn:

- what `git add` really does
- how the staging area works in practice
- how to stage selected files
- how to check what is staged before committing
