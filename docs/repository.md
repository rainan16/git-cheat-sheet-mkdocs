---
icon: material/source-repository
---

## Initialize Repository
Initialize any existing directory as a Git repository.
```shell
git init
```

## Download Repository
Download an entire repository from any location.
```shell
git clone <path-or-url-to-repository>
```

## Remote Repositories
Show all configured remotes.
```shell
git remote -v
```

Create a new connection to a remote repository. After adding you can use `<shortname>` as a shortcut for `<url>` in other commands.
```shell
git remote add <shortname> <url>
```

Fetches remote refs. Do this before actually pulling all changes to local.
```shell
git fetch
```
??? Options "Options _git fetch_"

    `<remote>` fetch from a secific remote repository
    `<branch>` fetch only one branch, not all remote refs

Fetches remote copy of current branch and immediatly merge it into local copy.
```shell
git pull
```
??? Options "Options _git pull_"

    `<remote>` fetch from a secific remote repository

Push curent branch to remote repository including all necessary commits and objects. This automatically creates a new remote branch if it doesn't exist.
```shell
git push
```
??? Options "Options _git push_"

    `<remote>` push to a secific remote repository  
    `<branch>` push specific branch
