# Git Command Cheat Sheet

A comprehensive cheat sheet for the most common and useful Git commands.

## Table of Contents
- [Basic Commands](#basic-commands)
- [Branching & Merging](#branching--merging)
- [Remote Repositories](#remote-repositories)
- [Inspection & History](#inspection--history)
- [Tagging](#tagging)
- [Undo & Cleanup](#undo--cleanup)
- [Stash](#stash)
- [Submodules](#submodules)
- [Miscellaneous](#miscellaneous)
- [Configuration](#configuration)
- [Git Aliases](#git-aliases)
- [References](#references)

---

## Basic Commands

| Command | Description |
|---------|------------|
| `git init` | Initialize a new Git repository |
| `git clone <repo>` | Clone a repository from a remote source |
| `git add <file>` | Add file(s) to staging (index) |
| `git add -A` | Add all new and changed files to staging |
| `git commit -m "message"` | Commit staged changes with a message |
| `git commit --amend` | Amend the previous commit |
| `git status` | Show the working tree status |
| `git diff` | Show unstaged changes between files and index |
| `git mv <old> <new>` | Rename or move a file (staged) |
| `git rm <file>` | Remove file from index and working directory (staged) |
| `git restore <file>` | Discard changes in working directory |
| `git clean -f` | Remove untracked files from working directory (force) |
| `git help` | Show command help |

---

## Branching & Merging

| Command | Description |
|---------|------------|
| `git branch` | List local branches |
| `git branch -a` | List all branches (including remote) |
| `git branch <name>` | Create a new branch |
| `git branch -d <name>` | Delete a local branch (safe) |
| `git branch -D <name>` | Force delete a local branch |
| `git checkout <branch>` | Switch to a branch |
| `git checkout -b <branch>` | Create and switch to a new branch |
| `git checkout <commit>` | Detach HEAD to a specific commit |
| `git merge <branch>` | Merge branch into current branch |
| `git rebase <branch>` | Rebase current branch onto another branch |
| `git cherry-pick <commit>` | Apply a specific commit to current branch |

---

## Remote Repositories

| Command | Description |
|---------|------------|
| `git remote -v` | Show remote repositories |
| `git remote add <name> <url>` | Add a new remote repository |
| `git remote set-url <name> <url>` | Change remote repository URL |
| `git fetch <remote>` | Download changes from remote (do not merge) |
| `git pull` | Fetch and merge changes from remote |
| `git pull <remote> <branch>` | Pull from a specific remote branch |
| `git push` | Push changes to remote |
| `git push <remote> <branch>` | Push branch to remote |
| `git push -u <remote> <branch>` | Push and set tracking branch |
| `git push <remote> --delete <branch>` | Delete a remote branch |

---

## Inspection & History

| Command | Description |
|---------|------------|
| `git log` | View commit history |
| `git log --oneline` | Compact commit history |
| `git log --graph --oneline` | Show commit log as graph |
| `git log --author=<name>` | Show commits by author |
| `git log --since=<date>` | Show commits since date |
| `git log -p <file>` | Show history for a specific file |
| `git blame <file>` | Show who last modified each line |
| `git diff <branch1> <branch2>` | Show changes between branches |
| `git show <commit>` | Show details for a commit |
| `git reflog` | Show reference logs for recovery |

---

## Tagging

| Command | Description |
|---------|------------|
| `git tag` | List all tags |
| `git tag <name>` | Create a lightweight tag |
| `git tag -a <name> -m "message"` | Create an annotated tag |
| `git push --tags` | Push all tags to remote |
| `git checkout <tag>` | Checkout a tag (detached HEAD) |

---

## Undo & Cleanup

| Command | Description |
|---------|------------|
| `git reset <file>` | Unstage a file |
| `git reset --hard` | Reset working directory and index to last commit (dangerous!) |
| `git reset <commit>` | Move HEAD to a specific commit (pointer) |
| `git revert <commit>` | Create a new commit that undoes a previous commit |
| `git clean -f` | Remove untracked files |
| `git gc` | Cleanup unnecessary files and optimize the repository |

---

## Stash

| Command | Description |
|---------|------------|
| `git stash` | Stash changes in working directory |
| `git stash list` | List stashed changes |
| `git stash apply` | Apply the last stashed changes |
| `git stash pop` | Apply and remove the last stash |
| `git stash drop` | Remove the last stash |
| `git stash clear` | Remove all stashes |

---

## Submodules

| Command | Description |
|---------|------------|
| `git submodule add <repo>` | Add a submodule |
| `git submodule update --init --recursive` | Initialize and update submodules |

---

## Miscellaneous

| Command | Description |
|---------|------------|
| `git bisect` | Find which commit introduced a bug |
| `git archive` | Create an archive of files |
| `git shortlog` | Summarize commit logs |
| `git config --global <key> <value>` | Set global Git configuration |
| `git checkout -- .` | Discard all changes in working directory |

---

## Configuration

| Command | Description |
|---------|------------|
| `git config --global user.name "Name"` | Set global username |
| `git config --global user.email "email@example.com"` | Set global email |
| `git config --list` | Show all configurations |
| `git config alias.<alias> "command"` | Create a Git alias |

---

## Git Aliases

| Alias | Command |
|-------|--------|
| `git co` | `git checkout` |
| `git cm` | `git commit -m` |
| `git st` | `git status` |
| `git lg` | `git log --graph --oneline --decorate --all` |
| `git br` | `git branch` |

Add these to your `~/.gitconfig` under `[alias]`:


