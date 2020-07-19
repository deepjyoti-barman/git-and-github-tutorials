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


## Creators

**Deepjyoti Barman**

- <https://github.com/defiant-dj04>
- <https://www.linkedin.com/in/deepjyoti-barman/>