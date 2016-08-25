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

## Terminal

A collection of useful UNIX command line stuff I've learned over time.

*For more, check out [commandlinefu](http://commandlinefu.com)!*

### General

- Display manual for terminal commands: `$ man command` (e.g. `$ man cd`)
- Perform last command: `$ !!`
- Perform last command with sudo: `$ sudo !!`
- Go back to previous dir: `$ cd -`

### Files
- Display contents of file: `$ cat filename`
- Find `filename` and only display results that contain `string`: `$ find path/to/dir filename | grep string`
- Display first 10 lines of file: `$ head -n 10 file.xxx`
- Display last 10 lines of file: `$ tail -n 10 file.xxx`
- Save text to file: `$ echo "Hello world!" > helloworld.txt`

### Directories
- Make directory: `$ mkdir dir_name`
- Remove directory: `$ rm -rf dir_name`

## Git/GitHub

List of basic and commonly used Git commands. Also, tips and tricks.

### Basics
- Usual git flow:
    - `$ git add . // use git add -A to include deleted files`
    - `$ git commit -m "message"`
    - `$ git push origin <branchname>`
- Display status: `$ git status`
- Pull from remote branch: `$ git pull origin <branchname>`
- Display difference since last commit: `$ git diff`

### Undoing

- Undo a `git add <file>`: `$ git reset <file>`
- Undo a `git add .`: `$ git reset`
- Remove file from index: `$ git rm --cached <file>`
- Undo changes then revert this file to last commit version: `$ git checkout -- path/to/file`
- If you want to add a file you forgot to add in a commit you just committed, or if you simply want to edit the commit message: `$ git commit --amend`
- To push an amended commit to remote repo, use `$ git push -f origin <branchname>`. However, this is **_strongly discouraged_** unless you're absolutely sure only you are going to use the repository.

_Read more about [Undoing Things in Git](https://git-scm.com/book/en/v2/Git-Basics-Undoing-Things) and [Pushing amended commits to remote repo](http://stackoverflow.com/questions/253055/how-do-i-push-amended-commit-to-the-remote-git-repo)._

### Branching

#### General
- Show all branches including remote: `$ git branch -a`
- Merge current branch with <branchname>: `$ git merge <branchname>`
- Save your dirty changes in a "stash": `$ git stash`
- Reapply the stashed changes: `$ git stash apply`
- List all stashed changes: `$ git stash list`
- Clear stash list: `$ git stash clear`

#### Checkout
Note: `git stash` might be helpful when switching branches.

- Checkout to existing branch: `$ git checkout <branchname>`
- Create branch: `$ git branch <branchname>`
- Create and checkout to new branch: `$ git checkout -b <branchname>`
- Create local clone of remote branch then checkout into it: `$ git checkout -b new_branch_name remote_branch_name`

##### Sample flow when working with branches:
```
// Display your current dirty state with uncommited changes
$ git status

// Stash changes, now it's safe to switch branches
$ git stash

// Checkout to a different branch
$ git checkout <new-branch>

// Make changes to files, commit, push etc.
// ...

// Return to original branch
$ git checkout <original-branch>

// Reapply stashed changes
$ git stash apply
```

#### Delete
- Delete branch: `$ git branch -d <branchname>`
- Delete branch without completing merge, i.e. force delete: `$ git branch -D <branchname>`

#### Push
-  Push local branch to GitHub: `$ git push origin <branchname>`
-  Delete remote branch: `$ git push --delete <branchname>`
-  Delete remote branch: `$ git push origin :<branchname>`

### Tips and tricks
- Add all + commit in one command: `$ git commit -a -m "message"`
- A cleaner more compact git log: `$ git log --oneline`
- Limit to last 5 logs: `$ git log -5`, `$git log --oneline -5`
- A cleaner more compact git status: `$ git status -s`
- Fuck you DS_Stores `$ echo "**/.DS_Store" >> .gitignore && rm -rf **/.DS_Store`

## VIM

### Tips and tricks

- Save file if vim was not run with sudo: `:w !sudo tee %`
- Run a terminal command while in VIM: `:! [command]`
- Add a dot after : to write output to VIM editor: `:.! date`
- "Delete in" commands:
	- `diw` – delete current word
	- `di(` – delete text inside current parens
	- `di"` – delete text inside current quotes
