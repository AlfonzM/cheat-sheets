# Cheat Sheets
*One cheat sheet to rule them all!*

A collection of cheat sheets for programming stuff because why not.

## Table of Contents
 - [Terminal](#terminal)
 - [Git / GitHub](#git / github)
 - [Sublime Text](#sublimetext)
 - [VIM](#vim)
 - [Symfony](#symfony)

## Terminal

A collection of cool and useful UNIX command line stuff I've learned over time.

*For more, check out [commandlinefu](#)!*

### General
- Perform last command: `$ !!`
- Perform last command with sudo: `$ sudo !!`
- Go back to previous dir: `$ cd -`
- Display manual for terminal commands: `$ man command` (e.g. `$ man cd`)

### Files
- Find _filename_ and only display results that contain _string_: `$ find path/to/dir filename | grep string`
- Display first 10 lines of file: `$ head -n 10 file.xxx`
- Display last 10 lines of file: `$ tail -n 10 file.xxx`
- Display contents of file: `$ cat filename`

### Directories
- Present working directory: `$ pwd`
- Make directory: `$ mkdir dir_name`
- Remove directory: `$ rm -rf dir_name`

## Git/GitHub

List of basic and commonly used Git commands.

### General
- Add all AND commit in one command: `$ git commit -a -m "message"`
- A cleaner more compact git log: `$ git log --oneline`
- Limit to last 5 logs: `$ git log --oneline -5`
- A cleaner more compact git status: `$ git status -s`
- Display changes since last commit: `$ git diff`, `$ git diff --cached`
- Remove file from index: `$ git rm --cached filename.xxx`
- Undo changes then revert this file to last commit version: `$ git checkout --path/to/file.xxx`

### Branching
- ...
