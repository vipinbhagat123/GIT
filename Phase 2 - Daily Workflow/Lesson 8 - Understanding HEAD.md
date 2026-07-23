# Lesson 8 - Understanding `HEAD`

## Learning goals

By the end of this lesson, you should be able to explain:

- what `HEAD` is
- why Git needs `HEAD`
- how `HEAD` normally points to a branch
- what Detached HEAD means
- how to inspect `HEAD`
- how branches and `HEAD` work together

## What is `HEAD`?

`HEAD` is a special pointer that tells Git where you are currently in the repository.

A simple way to think about it is:

- `HEAD` = "you are here"

## `HEAD` and branches

Most of the time, `HEAD` points to a branch, not directly to a commit.

Example:

```text
HEAD -> main -> latest commit
```

When you make a new commit, the branch moves forward, and `HEAD` follows that branch.

## Detached HEAD

If `HEAD` points directly to a commit instead of a branch, that is called Detached HEAD.

This can happen when you check out an older commit directly.

Detached HEAD is useful for:

- inspecting old versions
- testing older code
- debugging historical commits

## How to view `HEAD`

You can inspect the `.git/HEAD` file directly.

On Linux/macOS:

```bash
cat .git/HEAD
```

On Windows PowerShell:

```powershell
Get-Content .git\HEAD
```

It usually shows something like:

```text
ref: refs/heads/main
```

## Real-world analogy

Think of `HEAD` like a bookmark in a book.

The bookmark shows your current reading position.

When you move to another page, the bookmark moves too.

## Why `HEAD` matters

Git uses `HEAD` to know:

- where the current branch is
- where the next commit should go
- what history you are viewing

## Common mistakes

- thinking `HEAD` is a commit itself
- forgetting that detached HEAD is temporary unless you create a branch
- confusing `HEAD` with a branch name

## Interview question

**Q: What is `HEAD` in Git?**

**A:** `HEAD` is a pointer that tells Git the current location in the repository. Normally it points to the current branch, which points to the latest commit.

## Mini quiz

1. What is `HEAD`?
2. Does `HEAD` normally point to a branch or a commit?
3. What is Detached HEAD?
4. How can you view the contents of `.git/HEAD`?
5. Why is `HEAD` important?

## Homework

1. Create a repository and make a commit.
2. Inspect `.git/HEAD`.
3. Create a branch and switch to it.
4. Observe how `HEAD` changes.

## Next lesson

In Lesson 9, we will learn:

- what `git log` does
- how to read commit history
- how to use `--oneline`, `--graph`, and `--decorate`
- how to compare and search history
