---
icon: material/run-fast
hide:
  - toc
---


## How to look up a specific Command

:bulb:  Use the top right "Search" to find a command or action (e.g. "differences").  
To show examples use the (1) icon.
{ .annotate }

1.   _Examples_  
:material-console: `git <command>`

## Basic Commands

Initialize __new repository__ (1)
{ .annotate }

1.   _Examples_  
:material-console: `git init` _no parameter to initialize the current directory_  
:material-console: `git init /temp/somedir` _use for to initialize a specific directory_  

```shell
git init
```


Or __clone__ existing __repository__. (1)
{ .annotate }

1.  _Examples_  
:material-console: `git clone /path/to/git-repository.git`  
:material-console: `git clone https://github.com/rainan16/PVmeter.git`

```shell
git clone <repository>
```


__Stage__ all changes in `<directory>` or `<file>` for next commit. (1)
{ .annotate }

1.  _Examples_  
:material-console: `git add .`  
:material-console: `git add some_file.md`

```shell  
git add <directory_or_file>
```

__Commit__ your staged content as a new commit with a descriptive message `<msg>`. (1)
{ .annotate }

1.  _Examples_  
:material-console: `git commit -m"initial commit"`  
_Option `-a` automatically stages changes:_  
:material-console: `git commit -am"some other commit"`  

```shell
git commit -m "<msg>"
```

__Show changes__ in your working directory. (1)
{ .annotate }

1.  _Examples_  
:material-console: `git status`  
:material-console: `git status --oneline`  _non-verbose format_

```shell
git status
```


Display __commit history__.  (1)
{ .annotate }

1.  _Examples_  
:material-console: `git log`  
:material-console: `git log --oneline`  _non-verbose format_  
:material-console: `git log --graph`  _graphical format_

```shell
git log
```


Show unstages changes in your working directory.  (1)
{ .annotate }

1.  _Examples_  
:material-console: `git diff`  
:material-console: `git diff <file_name>`  _diff only one file_  

```shell
git diff
```

