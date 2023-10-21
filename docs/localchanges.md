---
icon: material/source-commit
---

## Show Changes
Show changes in your working directory.
```shell
git status
```

## Show File Differences
Show all differences of what is changed but not staged.   
```shell
git diff
```
??? Options "Options _git diff_"

    `--staged` for what's staged, but not commited  
    parameter `my-filename` shows a specific file only


## Handle Changes

### Add Changes for Next Commit
Add all tracked and untracked files or just a specific file to your next commit (stage).  
```shell  
git add <file_or_directory>
```
??? Options "Options _git add_"

    `.` add all tracked or untracked files  
    `my-changed-file` add a specific file only

### Commit Changes
Commit your changed content as a new commit.  
```shell
git commit -am "<descriptive message>"
```
??? Options "Options _git diff_"

    `-a` automatically stage all tracked, modified files before the commit  
    `-m <msg>` use the given <msg> as the commit message  
    `-am <msg>` stage tracked and commit with <msg> in one step  

### Amend last message
Change last commit message.  

```shell
git commit --amend "<descriptive message>"
```
!!! warning "Don't amend pushed commits"

### Rebase
Rebase the current branch onto `<base>`, where `<base>` can be a commit ID, branch name or tag.
```shell
git rebase <base>
```
!!! warning "Don't rebase pushed commits"

### Explicit versioning a file remove
Delete the file from repo and stage the removal for commit.
```shell
git rm <file>
```

## Undo Changes

### Undo last Changes
Discard all changes,
```shell
git reset HEAD
```

Unstage a file while retaining the changes.
```shell
git reset <file-name>
``` 

??? Options "Options _git reset_"

    `--hard` automatically stage all tracked, modified files before the commit  
    `-m <msg>` use the given <msg> as the commit message  
    `-am <msg>` stage tracked and commit with <msg> in one step 

Discard any local, uncommitted changes and thereby restore their last committed state.
```shell
git restore .
```

### Revert
Use this command to undo changes to a repository's puplished commit history. The other undo-commands such as, git checkout or git reset, move the HEAD/branch ref pointers to a specified commit. The `revert` operation will take the specified commit, inverse its changes and creates a new & reverted commit.

```shell
git revert <SHA>
``` 


## Show Commit History
Show the commit history for the currently active branch, starting with the newest.  
```shell
git log
```
??? Options "Options _git log_"

    `--oneline` shows only short _SHA_ and _message_  
    `--graph` show branches in a graphical way  
    `--follow <file-name>` Show the commits that changed a file, even across renames

### Show Git Object
Show any object in Git `<SHA>` in human-readable format.
```shell
git show <SHA>
```

## Temporary commits 

This is useful to temporarily store modified files (on a stash stack) in order to change branches.
For example when pulling into a dirty working directory (1)
{ .annotate }

1.   _Example pulling to dirty directory_  
```shell
$ git pull
...
file foobar not up to date, cannot merge.
$ git stash
$ git pull
$ git stash pop
```

Save modified and staged local modifications away and revert the working directory.
```shell
git stash
```

List stack-order of stashed file changes.
```shell
git stash list
```

Re-apply stored changes from top of the stash stack. 
```shell
git stash pop
```

Discard the changes from top of the stash stack.
```shell
git stash drop
```
