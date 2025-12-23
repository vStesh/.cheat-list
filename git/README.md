# Cheat list - Git

### General

`git clone <repository_link>` - clone repository into folder with repository name

`git clone <repository_link> ./` - clone repository into current folder

`git init` - git project initialize 

`git add .` - add all files to git

`git commit -m "<text comment>"` - create commit with comment

`git push` - push changes into repository

`git push -f` - force push

`git pull` - update local repository from remote

### Branches

`git branch` - look branches locally

`git branch -a`	look branches remotely

`git branch <new_name>` - create new branch

`git branch -d <branch_name>` - remove branch with merge control

`git branch -D <branch_name>` - remove branch locally

`git checkout <branch_name>` - switch out to another branch

`git checkout -b <new_branch_name>` - create new branch and switch out

`git branch -v` - show last commit list for each branch

`git branch -m <new_branch_name>` - rename current branch

`git branch -M main` - rename branch "master" to "main"

### Save and get changes locally

`git stash` - for record the current state of the working directory and the index, but want to go back to a clean working directory

`git stash list` - list the stash entries that you currently have

`git stash drop` - delete the all stash entries what you currently have

`git stash pop` - stash the changes in a dirty working directory away(back to your current branch)

`git cherry-pick <hash-commit>` - copy commit from one branch to another

### Other

`git remote add origin <git_repository_link>` - relate local repository with remote one by the link

`git push -u origin master` - push "master" branch to remote repository (once for each new repository)

`git remote -v` - show remote repository link

`git remote set-url origin <new_remote_link>` - change remote repository link

`git reset --hard <commit_hash>` - back to commit with hash

`git rebase <branch_name>` - rebase current branch from local "branch_name"

`git pull -r origin master` - rebase current branch from remote "master" branch

`git fetch` - get branches current state

`git push origin --delete <branch_name>` - remove branch remotely

`git remote update origin --prune` - update all branches from remote repository actual

### Merge

`git merge <branch_name>` - merge current branch with another branch

`git merge --abort` - cancel merge branches when need continue

### Submodule

`git submodule add <repo_link> <folder>` - add submodule in current project from another repository

### Config

`git config user.name`, `git config user.name <userName>` - get and set userName current repository locally

`git config --global user.name`, `git config --global user.name <userName>` - get and set userName globally

`git config user.email`, `git config user.email <userEmail>` - get and set userEmail current repository locally

`git config --global user.email`, `git config --global user.email <userEmail>` - get and set userEmail globally


## Info
> **Octotree** - Chrome extension for git files visualization

## **.gitignore** - example
```hgignore
.DS_Store
.idea
```

### Revert branch

`git log --oneline --graph -n 10` - see the log to find necessary hash commit

`git revert -m 1 <merge_commit_hash>` - revert commit and save the history

