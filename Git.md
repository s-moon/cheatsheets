# Git Cheat Sheet

> This is based on a number of sources but especially the excellent http://git-scm.com/book
> written by Scott Chacon and Ben Straub and published by Apress.
> Anything in angled brackets needs to be replaced with something suitable.
> A # indicates the start of a comment - so ignore the rest of the line.

> E.g. $ git help <command> might mean $git help *config*

### Setting User Options
```
$ git config --global user.name "Stephen Moon"
$ git config --global user.email stephen@logicalmoon.com
$ git config --global core.editor "'<path to your editor>'" 
```

### Viewing User Options
```
$ git config --list
```

### Starting a New Repository
```
$ git init		# inside the directory you want to begin using source control with
```

### Cloning (Copying) a Repository
```
$ git clone <url to repository> # e.g. https://github.com/s-moon/CheatSheets.git
$ git clone <url to repository> <your choice of directory name> # e.g. https://github.com/s-moon/CheatSheets.git CheatSheetsGalore
```

### Viewing the Status of Your Repository
```
$ git status # long form
$ git status --short # short form of the same (see: http://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository#Short-Status)
```

### Ignoring Files in your Repository
```
$ cat .gitignore
*.[oa] 	# ignore everything ending in o or a e.g. file.oa
*~ 		# ignore all files which end in the tilde character
# see (http://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository#Ignoring-Files)
```

### Getting Help
```
$ git help <command>
```

### Adding a File
```
$ git add <file path>
```

### Committing a Change
```
$ git commit
```

### Pushing Changes to Your Remote Repository
```
$ git push origin
```

### Adding a Submodule
```
$ git submodule add <git reference> # e.g. https://github.com/zendframework/zf1.git
```

Written by Stephen Moon stephen@logicalmoon.com, 2015