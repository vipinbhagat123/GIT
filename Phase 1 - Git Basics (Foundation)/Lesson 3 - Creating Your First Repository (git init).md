# Lesson 3 - Creating Your First Repository (`git init`)

## Learning goals

By the end of this lesson, you should be able to explain:

- what a Git repository is
- the difference between a normal folder and a Git repository
- what `git init` does
- what the hidden `.git` folder is
- the difference between a local repository and a remote repository

## What is a repository?

A Git repository is a project that Git manages.

It contains:

- your project files
- commit history
- branches
- tags
- configuration
- references
- internal Git objects

A simple way to think about it:

```text
Project files + .git folder = Git repository
```

## Normal folder vs Git repository

A normal folder becomes a Git repository when you run `git init`.

Example before initialization:

```text
Calculator/
├── app.py
└── README.md
```

After initialization:

```text
Calculator/
├── app.py
├── README.md
└── .git/
```

The hidden `.git` folder is what turns a normal folder into a repository.

## What does `git init` do?

`git init` initializes a new local repository.

It does **not**:

- create commits
- push anything to GitHub
- upload files to the internet

It **does**:

- create the `.git` folder
- initialize Git metadata
- prepare the project for tracking changes
- set up the repository structure

## What is inside `.git`?

The `.git` folder stores Git's internal data, such as:

- commit history
- branch references
- configuration
- objects
- logs
- hooks

Some common items you may see right after `git init` are:

- `HEAD`
- `config`
- `objects/`
- `refs/`
- `hooks/`
- `info/`

## Local repository vs remote repository

### Local repository

The repository on your own computer.

### Remote repository

The repository on a server such as GitHub.

You usually create the local repository first, then connect it to GitHub later.

## Hands-on lab

Create a folder and initialize Git:

```bash
mkdir Git-Lab
cd Git-Lab
git init
```

Check hidden files:

### Windows

```bash
dir /a
```

### Linux/macOS

```bash
ls -la
```

You should now see the `.git` folder.

## Common mistakes

- thinking `git init` creates a GitHub repository
- deleting the `.git` folder by mistake
- running `git init` in the wrong folder
- expecting commits to appear before any `git commit`

## Interview question

**Q: What does `git init` do?**

**A:** It creates a new local Git repository by initializing the hidden `.git` directory and preparing the folder to track changes.

## Mini quiz

1. What is a Git repository?
2. What does `git init` create?
3. What is stored inside `.git`?
4. What happens if `.git` is deleted?
5. Does `git init` create commits?

## Homework

1. Create a folder called `Git-Lab`.
2. Run `git init`.
3. Inspect the hidden `.git` folder.
4. Explain the difference between a normal folder and a Git repository.

## Next lesson

In Lesson 4, we will learn:

- Working Directory
- Staging Area (Index)
- Local Repository
- how files move through Git
- why Git needs a staging area
- the complete Git workflow
