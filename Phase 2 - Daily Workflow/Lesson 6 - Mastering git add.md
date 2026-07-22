# Lesson 6 - Mastering `git add`

## Learning goals

By the end of this lesson, you should be able to explain:

- what `git add` actually does
- why the staging area exists
- how `git add` relates to the Working Directory and the Local Repository
- how to stage one file, many files, or all files
- the difference between `git add .` and `git add -A`
- how to think about staged changes before committing

## What does `git add` do?

`git add` copies the current version of a file into the Staging Area (Index).

It does **not**:

- create a commit
- save history permanently
- upload anything to GitHub

It simply prepares the selected changes for the next commit.

## Why is `git add` important?

The staging area lets you choose exactly which changes should go into the next commit.

This is useful when:

- some files are ready and others are not
- you want to make a clean, focused commit
- you do not want to include unfinished work

## Working Directory, Staging Area, Repository

```text
Working Directory
        │
     git add
        ▼
Staging Area
        │
   git commit
        ▼
Local Repository
```

`git add` moves the file snapshot into the staging area, not into the final history.

## Real-world analogy

Think of an assignment:

- Working Directory = your draft
- Staging Area = the final pages you selected to submit
- Commit = submitting the assignment

If you edit the draft after selecting pages, you must select them again.

## Example

Create a file:

```bash
echo Hello > app.txt
```

The file is untracked until you run:

```bash
git add app.txt
```

Now the current content of `app.txt` is staged.

If you edit the file again after staging, the staged version does not change automatically.

You need to run `git add app.txt` again.

## Different ways to use `git add`

### Add one file

```bash
git add app.py
```

### Add multiple files

```bash
git add app.py login.py README.md
```

### Add everything in the current tree

```bash
git add .
```

### Add all changes, including deletions

```bash
git add -A
```

## `git add .` vs `git add -A`

- `git add .` stages changes in the current directory tree.
- `git add -A` stages all changes across the repository, including deletions.

In many root-level workflows, they may feel similar, but `-A` is the more explicit "stage everything" option.

## Internal working

When you run `git add`, Git:

1. Reads the file content.
2. Calculates an object ID for that content.
3. Stores the content as an object in `.git/objects`.
4. Updates the Index to point to that object.

That is why `git add` is about preparing a snapshot for the next commit.

## Common mistakes

- thinking `git add` creates a commit
- editing a file after staging and forgetting to stage again
- using `git add .` without checking `git status`
- assuming staged content updates automatically when the file changes

## Best practice

Before and after staging, check:

```bash
git status
```

Before committing staged content, it is also good to review:

```bash
git diff --staged
```

## Interview question

**Q: What does `git add` do?**

**A:** It copies the current version of selected file changes into the Staging Area so they can be included in the next commit.

## Mini quiz

1. What does `git add` actually do?
2. Does `git add` create a commit?
3. What is the purpose of the staging area?
4. What is the difference between `git add .` and `git add -A`?
5. What happens if you edit a file after staging it?

## Homework

Create three files, modify them, and stage only one of them. Then run `git status` and explain why only one file is ready for commit.

## Next lesson

In Lesson 7, we will learn:

- what a commit really is
- how `git commit` stores snapshots
- why commits are the heart of Git
- how commit history is built
- how to write good commit messages
