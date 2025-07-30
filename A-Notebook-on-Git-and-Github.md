# A Notebook on Git and Github

This is a handy notebook or reference book on one of the most popular SCM (Source Code Management / Software Configuration Management) tool - Git and Github. Staring off with the very basics, it covers almost all the frequently used git commands along with their description.

## Table of Contents

- [Introduction](#introduction)
- [Configuration](#configuration)
- [Create Repository](#create-repository)
- [Working with Repository](#working-with-repository)
- [Commit History](#commit-history)
- [Branches](#branches)
- [Tags](#tag)
- [Update and Publish](#update-and-publish)
- [Merge and Rebase](#merge-and-rebase)
- [Undo](#undo)
- [Miscellaneous](#miscellaneous)
- [Creators](#creators)

## Introduction

Git is a version control system for tracking changes in computer files / directories and coordinating work on those files among multiple people. It was created by Linus Torvalds.

Git is free and open source distributed version control system designed to handle everything from small to large scale projects with speed and efficiency.

Git is easy to learn and has a tiny footprint with lightning fast performance. It outclasses SCM tools like Subversion, CVS, Perforce and ClearCase with features like cheap local branching, convenient staging areas, and multiple workflows.

GitHub is a code hosting platform which allows you to upload your repositories online for collaboration and version control. GitHub lets you (and others) work together on projects thus making collaboration easier. GitHub provides backup of your local repositories in cloud and it also provides visual interface to your repositories.

## Configuration

```bash
git --version
```

To check the version of git currently installed on system.

```bash
git config --list
```

Show the current configurations.

```bash
git config --global user.name "github-username"
```

Set the name you want attached to your commit transactions.

```bash
git config --global user.email "github.email@example.com"
```

Set the email you want attached to your commit transactions.

```bash
git config --global color.ui auto
```

Enable helpful colorization of command line output.

```bash
git config [--local | --global | --system] "name" "value"
```

Setting configuration scope:\
--local or none for current repository,  
--global for user scope,  
--system for system scope.

```bash
git config --get "config-name"
```

Get configuration value for a configuration name.

```bash
git config --unset "config-name"
```

Unset configuration value for a given configuration name.

```bash
git config core.autocrlf true
```

Automatically convert between Unix and Windows end-of-line on commit and checkout.

```bash
git config core.autocrlf input
```

Convert CRLF to LF only when committing, use original line ending on checkout.

```bash
git config core.editor "editor"
```

Change the text editor for writing commit message.

## Create Repository

```bash
git init
```

Initialize an existing directory as a Git repository. Most other Git commands are not available outside of an initialized repository, so this is usually the first command you will run in a new project.

```bash
git clone "url"
```

Clone (download) a repository that already exists on GitHub, Bitbucket, GitLab etc., including all the files, branches, and commits.

## Working with Repository

![Git Workflow](git-workflow.png)

## Branches

Branches are an important part of working with Git which allows users to isolate work, change context and integrating changes once the additions, deletions and modifications are fully verified. Any commits you make will be made on the branch you are currently "checked out" to. Use ```git status``` to see which branch that is.

Whenever you want to do some changes in your code, or you want to add some new feature in your application, it is not recommended that you do all the changes in the main branch or in the master branch. It is recommended that you create a new branch for yourself checkout that branch and do all the changes in that branch and after testing and validating, once everything is working fine we merge those changes in the main i.e. master branch.

```bash
git branch
```

List all local branches. An asterisk (*) will appear next to the currently active branch.

```bash
git branch -a
```

List both local and remote-tracking branches. An asterisk (*) will appear next to the currently active branch.

```bash
git branch "branch-name"
```

Create a new branch referencing the current active branch (generally the current active branch is master).

```bash
git checkout "branch-name"
```

Switch to the specified branch and update the working directory. [Note: ```git checkout``` command operates upon three distinct entities - files, commits and branches].

```bash
git checkout -b "new-branch-name"
```

Create a new branch referencing the current active branch (generally the current active branch is master) and then switch to it.

```bash
git checkout -b "new-branch-name" "source-branch-name"
```

Create a branch referencing the specified branch.

```bash
git merge "branch-name"
```

Combine the specified branch's history into the current branch. This is usually done in pull requests (generally we checkout to the master branch before merging any other branch).

```bash
git branch -m "new-branch-name"
```

Rename current branch with a new branch name.

```bash
git branch -m "old-branch-name" "new-branch-name"
```

Rename specified branch with a new branch name. It is useful when being at the current branch you want to rename some other branch.

```bash
git branch -d "branch-name"
```

Delete the specified branch locally.

```bash
git push "remote-repo-alias" --delete "branch-name"
```

Delete the specified branch from the remote repository.  
e.g. ```git push origin --delete "feature"```

## Miscellaneous

```bash
git help
```

Lists all the commonly used git command and their usages on different contexts.

```bash
git help -a
```

Lists all the commands/sub-commands available in git command and their usages on different contexts.

```bash
git help "command-name"
```

Displays a detailed guideline for the given git command/sub-command along with description, usages, options, examples etc.

```bash
git update-git-for-windows
```

Download and install the latest version of Git if an updated version is available.

## Creators

**Deepjyoti Barman**

- <https://github.com/defiant-dj04>
- <https://www.linkedin.com/in/deepjyoti-barman/>