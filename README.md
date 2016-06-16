# Configuration 

Global configuration stored under ~/.gitconfig. Local configuration store$ 

```bash 
git config --global user.name "Tyson Whitehead"   
git config --global user.email "twhitehead@gmail.com" 
```
```bash
git config --global color.ui auto
```
```bash 
git config --global core.editor nano
```

# Initialization 

Creates the .git directory. To undo `rm -r .git`. 

```bash 
mkdir $folder
cd $folder
git init
```
# Creating the next version

First view the status to see where things are at

```bash
git status
```

Add the changes you want in the next version (the `-p` option asks you 
change by change and is not required to just add everything)

```bash
git add -p $file
```

If you want to remove a file

```bash
git rm $file
```

# Save the next version

To save the next version run

```bash
git commit
```

For a log message, describe why you made the change, not what change you 
made as the computer can tell you the latter but not the former. Make 
the first line a brief oneline overview.

# Viewing changes

You can view all the log messages going back to the start with (the 
`--graph` options draws a pretty graph and `--oneline` just displays the 
first line of each message)

```bash
git log
```

You can view the changes that aren't staged yet with (you can specify a 
file to just see the changes in that file)

```bash
git diff
 ```

You can view the changes that aren't staged yet 
with (you can specify a file to just see the changes in that file)

```bash
git diff
```

You can view how the next version (the staged version) differs from the 
previous version with

```bash
git diff --staged
```
View changes between Folder/Working tree and master

```bash
git diff master
```

View changes between two commits (see following section for overview on specifying commits)

```bash
git diff 3b12245 def106f
```

# Specifying commits

Commits can be specified by

* number: `def106f`
* branch name: `master`
* going back n steps: `master~$n` (replace `$n` with the number)
* taking the nth branch: `master^$n`  (replace `$n` with the number)

# Branching

Create branch named history, then switch branch and verify (will display a `*` beside the current branch)

```bash
git branch 
```

Create a new branch called `history`

```bash
git branch history
```

Switch to a different branch (may overwrite files)

```bash
git checkout history
```
To merge in the changes in another branch called history into the current branch

```
git merge history
```

To read the manual - git and branch options.....q to quit
```bash
man -k git

man git-branch
```

To see the different ways of specifying commits (and groups of commits for things like log to show)

```bash
man gitrevisions
```bash

#Git online

#To read about the licenses when you create a new project
creativecommons.org/licenses

git remote add github https://github.com/yourusername/GitNotes.git 
git remote -v

https://github.com/WikiSteve/gitnotes.git

Erika   https://github.com/ErikaMunozTorres/GitNotes.git

twhitehead - https://github.com/twhitehead/gitnotes.git
Els: https://github.com/els1/gitnotes.git
(Gordon) canadacoder - https://github.com/canadacoder/gitnotes.git

# Send master branch (from your pc) to github online repository......you need your git-username and password
```bash
git push github master
```bash

(Gordon) canadacoder - twhitehead
els1 - WikiSteve
