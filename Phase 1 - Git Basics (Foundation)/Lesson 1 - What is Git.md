# Lesson 1 - What is Git?

## What is Git?

Git is a distributed version control system (DVCS).

It helps you track changes in files over time, compare versions, recover old work, and collaborate safely with others.

## What is version control?

Version control means keeping track of every change made to your project files.

Instead of saving files like:

- `Project_Final.docx`
- `Project_Final_Really_Final.docx`
- `Project_Final_Really_Really_Final.docx`

Git keeps one project and remembers the history of changes behind the scenes.

## Why was Git created?

Git was created in 2005 by Linus Torvalds to help manage the Linux kernel project.

It was designed to be:

- fast
- reliable
- able to work offline
- good for large projects
- useful for many developers working together

## Git vs GitHub

Git and GitHub are not the same.

- Git is the version control software installed on your computer.
- GitHub is an online platform that hosts Git repositories.

A simple way to think about it:

- Git = the engine
- GitHub = the online place where you store and collaborate

## How Git works at a high level

```text
Your files
   ↓
Working directory
   ↓ git add
Staging area
   ↓ git commit
Local repository
   ↓ git push
GitHub
```

## Real-world analogy

Think of Google Docs version history.

You can see older versions, compare changes, and restore work. Git does something similar for code and other files.

## Why companies use Git

Companies use Git because many people can work on the same project without overwriting each other’s work.

Git helps with:

- tracking changes
- branching new work
- reviewing code
- merging safely
- reverting mistakes

## Common misconception

Git does not just store files.

It stores the history of your project as snapshots.

## Interview question

**Q: Why is Git called a distributed version control system?**

**A:** Because each developer has a full copy of the repository and its history on their machine, so work can happen locally even without a central server.

## Mini quiz

1. What problem does Git solve?
2. What does DVCS stand for?
3. What is a version?
4. Can Git work without GitHub?
5. Who created Git?
6. What is the difference between Git and GitHub?
7. Does Git store files or project history?

## Homework

1. Think of one real-life situation where version control would be useful.
2. Write your own one-line definition of Git.
3. Try to explain Git vs GitHub in simple words.

## Next lesson

In Lesson 2, we will learn:

- how to install Git
- how to configure Git
- how to check the Git version
- what the `.git` folder is
- how to create your first repository
- how the working directory, staging area, and repository work together
