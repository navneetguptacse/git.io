# Git Cheat Sheet

## Stage & Snapshot

### Working with snapshots and the Git staging area

- **git status:** Show modified files in the working directory, staged for your next commit.
- **git add [file]:** Add a file as it looks now to your next commit (stage).
- **git reset [file]:** Unstage a file while retaining the changes in the working directory.
- **git diff:** Diff of what is changed but not staged.
- **git diff --staged:** Diff of what is staged but not yet committed.
- **git commit -m "[descriptive message]":** Commit your staged content as a new commit snapshot.

## Setup

### Configuring user information used across all local repositories

- **git config --global user.name "[firstname lastname]":** Set a name that is identifiable for credit when reviewing version history.
- **git config --global user.email "[valid-email]":** Set an email address that will be associated with each history marker.
- **git config --global color.ui auto:** Set automatic command line coloring for Git for easy reviewing.

## Setup & Init

### Configuring user information, initializing and cloning repositories

- **git init:** Initialize an existing directory as a Git repository.
- **git clone [url]:** Retrieve an entire repository from a hosted location via URL.

## Branch & Merge

### Isolating work in branches, changing context, and integrating changes

- **git branch:** List your branches. A \* will appear next to the currently active branch.
- **git branch [branch-name]:** Create a new branch at the current commit.
- **git checkout [branch]:** Switch to another branch and check it out into your working directory.
- **git merge [branch]:** Merge the specified branch’s history into the current one.
- **git log:** Show all commits in the current branch’s history.

Git is the free and open-source distributed version control system that's responsible for everything GitHub-related that happens locally on your computer. This cheat sheet features the most important and commonly used Git commands for easy reference.

## Installation & GUIs

With platform-specific installers for Git, GitHub also provides the ease of staying up-to-date with the latest releases of the command line tool while providing a graphical user interface for day-to-day interaction, review, and repository synchronization.

- **GitHub for Windows:** [Download Here](https://windows.github.com)
- **GitHub for Mac:** [Download Here](https://mac.github.com)
- **Git for All Platforms:** [Download Here](http://git-scm.com)

## Share & Update

### Retrieving updates from another repository and updating local repos

- **git remote add [alias] [url]:** Add a Git URL as an alias.
- **git fetch [alias]:** Fetch down all the branches from that Git remote.
- **git merge [alias]/[branch]:** Merge a remote branch into your current branch to bring it up to date.
- **git push [alias] [branch]:** Transmit local branch commits to the remote repository branch.
- **git pull:** Fetch and merge any commits from the tracking remote branch.

## Tracking Path Changes

### Versioning file removes and path changes

- **git rm [file]:** Delete the file from the project and stage the removal for commit.
- **git mv [existing-path] [new-path]:** Change an existing file path and stage the move.
- **git log --stat -M:** Show all commit logs with an indication of any paths that moved.

## Temporary Commits

### Temporarily store modified, tracked files in order to change branches

- **git stash:** Save modified and staged changes.
- **git stash list:** List stack-order of stashed file changes.
- **git stash pop:** Write working from the top of the stash stack.
- **git stash drop:** Discard the changes from the top of the stash stack.

## Rewrite History

### Rewriting branches, updating commits, and clearing history

- **git rebase [branch]:** Apply any commits of the current branch ahead of the specified one.
- **git reset --hard [commit]:** Clear the staging area, rewrite working tree from the specified commit.

## Inspect & Compare

### Examining logs, diffs, and object information

- **git log:** Show the commit history for the currently active branch.
- **git log branchB..branchA:** Show the commits on branchA that are not on branchB.
- **git log --follow [file]:** Show the commits that changed a file, even across renames.
- **git diff branchB...branchA:** Show the diff of what is in branchA that is not in branchB.
- **git show [SHA]:** Show any object in Git in a human-readable format.

## Ignoring Patterns

### Preventing unintentional staging or committing of files

- **git config --global core.excludesfile [file]:** System-wide ignore pattern for all local repositories.
    
    Example patterns:

    - **logs/** : Ignore logs directory
    - ***.notes** : Ignore files with .notes extension
    - **pattern_/** : Ignore directories with pattern prefix


### Share & Update (⭐ New)

- **git branch -m <oldname> <newname>** : Rename branch locally
- **git branch -m <newname>** : Rename current branch locally
- **git push origin :<oldname> <newname>** : Delete the old branch
- **git push origin -u <newname>** : Push the new branch, set local branch to track the new remote

- **git push origin --delete <branchName>** : Delete a remote branch
- **git push origin :<branchName>** : Delete a remote branch

- **git push origin <branchName>** : Push a branch to remote repository
- **git push --all origin** : Push all branches to your remote repository

- **git push -u origin <branchName>** : Push changes to remote repository (and remember the branch)
- **git push origin <branchName>** : Push changes to remote repository (remembered branch)
