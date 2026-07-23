# Lesson 7 - Mastering `git commit`

## Learning goals

By the end of this lesson, you should be able to explain:

- what a commit really is
- how Git saves snapshots
- why commits are the heart of Git
- what `HEAD` points to after a commit
- how to write good commit messages
- what `git commit --amend` does

## What is a commit?

A commit is a snapshot of your staged project at a specific point in time.

It includes:

- the staged file contents
- author information
- date and time
- commit message
- parent commit reference

## What does `git commit` do?

`git commit` takes the changes from the Staging Area and stores them in the Local Repository.

It does **not**:

- upload code to GitHub
- create a branch
- stage files automatically

## Why commits matter

Commits build the history of your project.

Each commit becomes a point you can return to later.

## What is `HEAD` doing after a commit?

`HEAD` normally follows the current branch.

After a new commit, the branch reference moves forward, and `HEAD` still points to that branch.

## Good commit messages

Good commit messages are clear and specific.

Examples:

- Add login validation
- Fix user profile crash
- Update README installation steps
- Refactor payment service

Bad messages:

- update
- fix
- changes
- test

## `git commit --amend`

Use `git commit --amend` to modify the most recent local commit.

This is useful when:

- you forgot to include a file
- you want to correct the message
- you want to improve the last commit before pushing

Be careful if the commit is already shared with others.

## Real-world analogy

Think of a commit like submitting an assignment.

- Working Directory = drafting the work
- Staging Area = selecting the final content
- Commit = submitting the finished version

## Internal idea

When you commit, Git creates a new commit object and stores it in `.git`.

That commit points to the snapshot of the staged content.

## Common mistakes

- writing vague commit messages
- committing unrelated changes together
- thinking `git add` creates a commit
- forgetting to check `git status` before committing

## Interview question

**Q: What is a Git commit?**

**A:** A Git commit is a snapshot of the staged project state at a specific point in time, stored in the local repository with metadata such as author, date, and message.

## Mini quiz

1. What is a commit?
2. What does `git commit` do?
3. Does `git commit` upload code to GitHub?
4. What does `git commit --amend` do?
5. Why are good commit messages important?

## Homework

Create three meaningful commits in your practice repository and use descriptive commit messages.

## Next lesson

In Lesson 8, we will learn:

- what `HEAD` is
- how `HEAD` points to the current branch
- what Detached HEAD means
- how to view `HEAD` directly
