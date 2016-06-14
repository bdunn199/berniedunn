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

