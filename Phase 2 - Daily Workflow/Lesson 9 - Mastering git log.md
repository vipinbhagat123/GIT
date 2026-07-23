# Lesson 9 - Mastering `git log`

## Learning goals

By the end of this lesson, you should be able to explain:

- what `git log` does
- how to read commit history
- what commit hashes are
- how to use `--oneline`, `--graph`, and `--decorate`
- how to search commit history
- how to compare commits

## What is `git log`?

`git log` shows the commit history of your current branch.

Each commit usually includes:

- commit hash
- author
- date
- commit message

## Why use `git log`?

It helps you answer questions like:

- Who changed this?
- When was it changed?
- What was the message?
- What came before this commit?

## Reading the output

By default, Git shows the newest commit first.

That is useful because developers usually want to inspect the latest changes first.

## Helpful options

### `git log --oneline`

Shows each commit in a compact one-line format.

### `git log --graph`

Shows history as an ASCII graph.

### `git log --decorate`

Shows branch names and `HEAD` labels.

### Combined view

```bash
git log --oneline --graph --decorate
```

This is one of the most useful day-to-day history views.

## Searching history

You can search commit messages using:

```bash
git log --grep="keyword"
```

## Comparing commits

You can compare two commits using:

```bash
git diff <commit1> <commit2>
```

## Real-world analogy

Think of `git log` like a timeline of your project.

It shows what happened, when it happened, and who did it.

## Common mistakes

- using only the full log when `--oneline` is easier
- ignoring history and relying only on the latest code
- writing vague commit messages that make history hard to read

## Interview question

**Q: What does `git log` do?**

**A:** `git log` displays the commit history of the current branch, including commit hashes, authors, dates, and messages.

## Mini quiz

1. What does `git log` show?
2. What does `--oneline` do?
3. What does `--decorate` show?
4. Why is the newest commit listed first?
5. Can you compare two commits with Git?

## Homework

1. Create a few commits in your practice project.
2. Run `git log`.
3. Run `git log --oneline`.
4. Run `git log --graph --decorate --oneline`.
5. Compare the outputs.

## Next lesson

In Lesson 10, we will learn:

- what `git diff` does
- how to compare Working Directory vs Staging Area
- how to compare Staging Area vs Repository
- how to compare two commits
