# Git Cheat Sheet

Git is a widely used version control system for software development which 
emphasises speed, data integrity and support for distributed, non-linear
workflows -- [source](https://en.wikipedia.org/wiki/Git_%28software%29).

> This is based on a number of sources but especially the excellent 
> http://git-scm.com/book written by Scott Chacon and Ben Straub and 
> published by Apress.
> Anything in angled brackets needs to be replaced with something suitable.
> A "#" indicates the start of a comment - so ignore the rest of the line.

> E.g. $ git help \<command\> might mean $git help *config*

### Setting user options
```
$ git config --global user.name "Stephen Moon"
$ git config --global user.email stephen@logicalmoon.com
$ git config --global core.editor "'<path to your editor>'" 
```

### Viewing user options
```
$ git config --list
```

### Starting a new repository
```
$ git init # inside the directory you want to begin using source control with
```

### Cloning (copying) a repository
```
$ git clone <url to repository> # e.g. https://github.com/s-moon/CheatSheets.git
$ git clone <url to repository> <your choice of directory name> # e.g. https://github.com/s-moon/CheatSheets.git CheatSheetsGalore
```

### Viewing the status of your repository
```
# long form
$ git status 

# short form of the same (see: http://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository#Short-Status)
$ git status --short 
```

### Ignoring files in your repository
```
$ cat .gitignore
*.[oa] # ignore everything ending in o or a e.g. file.oa
*~ # ignore all files which end in the tilde character
# see (http://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository#Ignoring-Files)
```

### Getting help
```
$ git help <command>
```

### Adding files
```
# Add a specific file
$ git add <file path>

# Add all files in current directory
$ git add .

# Adding files one by one (use y, n or q to end)
$ git add -p
```

### Viewing your unstaged commits
```
$ git diff
```

### Undoing an edit to a file
```
$ git checkout --- <file you want to lose the edit for>
```

### Committing a change
```
$ git commit # commit message will be required
$ git commit -m "This is my commit message" # commit message supplied
$ git commit -a # stage all modified (but not new) files and commit them in one.
```

### Viewing your staged commits
```
$ git diff --staged
```

### Pushing changes to your remote repository
```
$ git push origin
$ git push origin master # use this if it complains about branches/which branch
```

### Adding remote repositories
```
$ git remote add <name of remote> <url of remote>
```

### Listing remotes
```
$ git remote -v
```

### Making your remotely forked repository match the original
```
$ git pull upstream master
$ git push origin master
# NB - this assumes you have origin pointing to your forked repository
# and that upstream points to the source repository.
```

### Removing files
```
$ git rm PROJECTS.md # removes from the file system AND from staging
```

### Renaming files
```
$ git mv file_from file_to
```

### Viewing commit history
```
$ git log

# show difference AND limit to last two entries
$ git log -p -2	

$ git log --pretty=oneline # one line version
```

### Undoing a commit message
```
# this will allow you to re-do your commit message
$ git commit --amend 

$ git add <file-that-I-forgot>

# a second file is added and included in the original commit
$ git commit --amend 
```

### Unstaging a commit
```
$ git reset HEAD <file to undo>
```

### Undoing a file modification
```
$ git checkout -- <file to undo> # this will revert a file back to before you modified it

# remove all changes
$ git co --
```

### Creating a branch and switching to it
```
$ git checkout -b <branch-name>
```

### Deleting a branch
```
$ git branch -d <branch-name>
```

### Force deleting a branch with unmerged commits
```
$ git branch -D <branch-name>
```

### Switching between branches
```
$ git co -
# repeat to switch back to previous branch

or
$ git checkout <branch-name>
```

### Merging a branch with master
Let's say thay you have a branch called master (you will) and
another which is named <branch name>. <branch name> already
contains committed changes that you want to merge back into 
master.
```
$ git checkout master
$ git merge <branch-name>
```

## Setting upstream tracking for a branch
After creating a new branch, ```foo```, you can make it track a remote branch ```origin``` with
the following command if IN THE BRANCH:
```
$ git branch -u origin/foo
```
or if not in the branch, foo:
```
$ git branch -u origin/foo foo
```

### Adding a Submodule
```
$ git submodule add <git-reference> # e.g. https://github.com/zendframework/zf1.git
```

Written by Stephen Moon (stephen@logicalmoon.com)
