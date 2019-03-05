# Git Basics
&nbsp;
&nbsp;
## Config
&nbsp;
### Allow ssh
```git
git config --global http.sslVerify false
```

### Username and email
```git 
git config —global user.name “username”
git config —global user.email “email@email.com”
```

### Check config settings
```git 
git config --global -e
git config —global —list
```

### Alias
```git 
git config —global alias.name_of_the_alias “full command name”
```

### Diff
```git 
git config —global diff.tool p4merge
git config —global difftool.p4merge.path /Applications/p4merge.app/Contents/MacOS/p4merge
git config —global difftool.prompt false
```

### Merge
```git 
git config —global merge.tool p4merge
git config —global mergetool.p4merge.path /Applications/p4merge.app/Contents/MacOS/p4merge
git config —global mergetool.prompt false
```
&nbsp;
&nbsp;
## Commands
&nbsp;
### Log
```git 
git log
git log —oneline —decorate
```

### List tracked files
```git 
git ls-files
```

### Move files
```git 
git mv file1.txt file2.txt
git add -A file1.txt // Add file after move from system
```

### Update the index
```git 
git add -u
```

### Delete tracked file
```git 
git rm file.txt
```

### Diff
```git 
git diff HEAD
git difftool HEAD
git diff —staged HEAD
git difftool —staged HEAD
git diff — README.md
git difftool README.md
git diff HEAD HEAD^
git difftool HEAD HEAD^
git diff commit-id-1 commit-id-2
git diff master origin/master
```
&nbsp;
&nbsp;
## Branches
&nbsp;
### Basic
```git 
git branch -a
git branch mybranch
git checkout mybranch
```

### Rename
```git 
git checkout master
git branch -m mybranch newbranch
```

### Delete
```git 
git branch -d newbranch
```

### Create and checkout
```git 
git checkout -b newbranch2
```

### Compare branches
```git 
git diff master newbranch2
```

### Merge Branches
```git 
git merge newbranch2
```

### No fast forward
```git 
git merge newbranch2 —no-ff
git branch -d newnranch2
git merge newbranch2 -m “merging branches...”
```

### Resolving Conflicts
```git 
git mergetool
git commit
```
&nbsp;
&nbsp;
## Rebase
&nbsp;
### Rebase basics
```git 
git checkout newbranch
git log --oneline --decorate --all --graph
git rebase master
git checkout master
git rebase abort
```
Fix conflicts and
```git 
git rebase --continue
```
### Rebase conflicts (remote and local) 
```git 
git fetch origin master
git pull --rebase origin master
```

&nbsp;
&nbsp;
## Reset
&nbsp;
### Reset basics
```git 
git reset HEAD^1
git reset "commit id"
```

### Reflog
```git 
check git reset log
```
&nbsp;
&nbsp;
## Stash
To be tracked after file edit
&nbsp;
### Stash basics
```git 
git stash
git stash apply
git stash list
git stash drop
```
Include untracked files
```git 
git stash -u 
```
Apply and drop
```git 
git stash pop
```

### Multiple stashes
```git 
git stash save "comment"
git stash list
git stash show stash@{#}
git stash apply stash@{#}
git stash drop stash@{#}
```

### Stash into branch
```git 
git stash branch newbranch
git checkout master
git merge newbranch
git branch -d newbranch
```
