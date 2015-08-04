# Cheat Sheets
*One cheat sheet to rule them all!*

A collection of cheat sheets for programming stuff because why not.

Inspired by [github-cheat-sheet](https://github.com/tiimgreen/github-cheat-sheet) and [commandlinefu](http://commandlinefu.com).

## Table of Contents
 - [Terminal](#terminal)
    - [General](#general)
    - [Files](#files)
    - [Directories](#Directories)
 - [Git / GitHub](#gitgithub)
    - [Basics](#Basics)
    - [Branching](#branching)
        - [General](#general)
        - [Checkout](#checkout)
        - [Delete](#delete)
        - [Push](#push)
    - [Tips and tricks](#tipsandtricks)
 - [Sublime Text](#sublimetext)
 - [VIM](#vim)
 - [Symfony](#symfony)

## Terminal

A collection of cool and useful UNIX command line stuff I've learned over time.

*For more, check out [commandlinefu](http://commandlinefu.com)!*

### General

- Display manual for terminal commands:
   
   `$ man command` (e.g. `$ man cd`)

- List files with more info:

   `$ ls -l`
   
- Perform last command:
   
   `$ !!`
- Perform last command with sudo:
    > `$ sudo !!`
- Go back to previous dir:
    > `$ cd -`

### Files
- `$ cat filename`
    - Display contents of file:
- `$ find path/to/dir filename | grep string`
    - Find _filename_ and only display results that contain _string_:
- `$ head -n 10 file.xxx`
    - Display first 10 lines of file:
- `$ tail -n 10 file.xxx`
    - Display last 10 lines of file:
- ```$ echo "Hello world!" > helloworld.txt```
    - Save text to file:
    
### Test
Display contents of file

- ```$ cat filename```

Find _filename_ and only display results that contain _string_

- ```$ find path/to/dir filename | grep string```

Display first 10 lines of file

- ```$ head -n 10 file.xxx```

Display last 10 lines of file

- ```$ tail -n 10 file.xxx```

Save text to file

- ```$ echo "Hello world!" > helloworld.txt```


### Test
- Display contents of file
 - ```$ cat filename```

- Find _filename_ and only display results that contain _string_
 - ```$ find path/to/dir filename | grep string```

- Display first 10 lines of file
 - ```$ head -n 10 file.xxx```

- Display last 10 lines of file
 - ```$ tail -n 10 file.xxx```

- Save text to file
 - ```$ echo "Hello world!" > helloworld.txt```


### Directories
- Make directory: `$ mkdir dir_name`
- Remove directory: `$ rm -rf dir_name`

## Git/GitHub

List of basic and commonly used Git commands. Also, tips and tricks.

### Basics
- Usual git flow:
    - `$ git add . // use git add -A to include deleted files`
    - `$ git commit -m "message"`
    - `$ git push origin branchname`

- Dispay status: `$ git status`
- Pull from remote branch: `$ git pull origin branchname`
- Display difference since last commit: `$ git diff`

### Branching

#### General
- Show all branches including remote: `$ git branch -a`
- Merge current branch with branchname: `$ git merge branchname`

#### Checkout
Note: [git stash](#gitstash) might be helpful when switching branches.

- Checkout to existing branch: `$ git checkout branchname`
- Create branch: `$ git branch branchname`
- Create and checkout to new branch: `$ git checkout -b branchname`
- Create local clone of remote branch then checkout into it: `$ git checkout -b new_branch_name remote_branch_name`

#### Delete
- Delete branch: `$ git branch -d branchname`
- Delete branch without completing merge, i.e. force delete: `$ git branch -D branchname`

#### Push
-  Push local branch to GitHub: `$ git push origin branch_name`
-  Delete remote branch: `$ git push --delete branch_name`
-  Delete remote branch: `$ git push origin :branch_name`

### Tips and tricks
Add all AND commit in one command:

```$ git commit -a -m "message"```

A cleaner more compact git log:

```$ git log --oneline```

Limit to last 5 logs:

```$ git log -5`, `$git log --oneline -5```

A cleaner more compact git status:

```$ git status -s```

Remove file from index:

```$ git rm --cached filename.xxx```

Undo changes then revert this file to last commit version:

```$ git checkout --path/to/file.xxx```
