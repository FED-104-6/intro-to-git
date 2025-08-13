# Introduction to Git. 
  
  * [Git Documentation](https://git-scm.com/book/en/v2)

Git is a distributed version control system, which we use to keep track of our software. This helps us when we are working with others, and especially with sharing code and code changes.  
  
Let's have a look at some of the common Git commands that we use.

## Getting Started

First of all, we "initialize" a directory as a Git repository. "Repository" is a word we use that just really means this directory is managed by Git.

```bash
git init
```

The `git init` command creates a hidden directory (directory is just another word for folder) called `.git`. This directory contains all the information Git needs to manage our project. We don't need to look in here, but it's good to know it's there.

Some other commands that we are going to get used to pretty quickly are:

```bash
git status
git log
```

```bash
git add <file>...
git add -A
```

What this does is it adds the file to staging.

Once a file is "staged" you can use the `git commit` command to save the changes you have made to the file.

```bash
git commit -m "Your message here"
```

Another very interesting _feature_ of Git is _branches_. Branches are a way to work on different versions of your code at the same time. You can think of them as different "copies" of your code.

## Branches

```bash
git branch <branch-name>
git checkout <branch-name>

# example
git branch new-feature-001
git checkout new-feature-001
```

Note: An interesting command is `git checkout -` which will checkout the previous branch you were on.  
  
Now that we have created a new branch, and done some work on it (we added some text, made some commits, etc.), if we want to add those changes to the main branch, we can do something called a "merge".  
  
Here's how:

```bash
git checkout main
git merge new-feature-001
```