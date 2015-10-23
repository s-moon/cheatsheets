# Git Cheat Sheet

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

Written by Stephen Moon stephen@logicalmoon.com, 2015