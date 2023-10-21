---
icon: material/git
---

### Installation
Install Git for any platform [http://git-scm.com](http://git-scm.com)


### Configuration
Set user name and email that is shown in version history.  

```shell
git config user.name "Firstname Lastname"
git config user.email "my-email@domain.com"
```
??? Options "Options _git config_"

    `--global` set user.name for all, not just the current repository

Automatic command line coloring.
```shell
git config --global color.ui auto
```

To ignore some files create a `.gitignore` with desired patterns as with either direct string matches or wildcard globs.