# Lesson 2 - Installing Git & Configuration

## Learning goals

By the end of this lesson, you should be able to:

- install Git
- check whether Git is installed correctly
- configure your Git username and email
- understand the difference between `--global`, `--local`, and `--system`
- explain why Git needs configuration before you start committing

## Why do we need Git configuration?

Git stores author information in every commit.

That means Git needs to know:

- who made the change
- which email address to attach to the commit
- when the commit was created

Without configuration, your commits may not show the correct author information.

## Installing Git

### On Windows

1. Go to the official Git website.
2. Download Git for Windows.
3. Run the installer.
4. Keep the default options unless your system requires something special.

### On macOS

You can install Git using:

- Homebrew
- Xcode Command Line Tools

### On Linux

You can install Git using your package manager.

## Check whether Git is installed

Run:

```bash
git --version
```

If Git is installed, you will see a version number.

Example:

```bash
git version 2.x.x
```

## Configure your identity

Git should know your name and email address.

### Set your username

```bash
git config --global user.name "Your Name"
```

### Set your email

```bash
git config --global user.email "your_email@example.com"
```

## Verify your configuration

Run:

```bash
git config --list
```

This shows the current configuration values Git is using.

## Configuration levels

Git has three configuration levels.

### 1. System

Applies to every user on the machine.

### 2. Global

Applies to your user account across all repositories.

Example:

```bash
git config --global user.name "Vipin Bhagat"
```

### 3. Local

Applies only to a single repository.

Example:

```bash
git config user.name "Office Account"
```

Local settings override global settings.

## Real-world analogy

Think of Git configuration like a name tag.

When you submit work, Git attaches the name tag so the commit records who made it.

## What we learned in this lesson

- Git is installed on your local machine
- `git --version` checks the installation
- Git uses your name and email in commits
- `git config --global` sets values for all repositories for your user
- `git config` without `--global` can set values only for one repository
- `git config --list` shows current settings

## Common mistake

A very common mistake is forgetting to configure your name and email before making commits.

## Interview question

**Q: Why do we use `git config --global user.name` and `git config --global user.email`?**

**A:** So Git can attach the correct author information to commits across all repositories for that user.

## Mini quiz

1. What command checks the installed Git version?
2. Why does Git need your name and email?
3. What does `--global` mean?
4. What is the difference between global and local configuration?
5. What does `git config --list` do?

## Homework

1. Install Git on your computer if it is not already installed.
2. Run `git --version`.
3. Configure your username and email.
4. Run `git config --list` and observe the output.

## Next lesson

In Lesson 3, we will learn:

- what a repository is
- how to create one using `git init`
- what the hidden `.git` folder means
- what lives inside the `.git` folder
