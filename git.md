## 0 Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

## 1 Create a task branch
With a clean master branch checked out, you can create a task branch by typing:

`git checkout -b task_branch`

where the task_branch is the name of the branch you want to create. By using the -b option it will both create a new branch and check it out.
## 2 Do your work and commit
As your are doing work you can commit regularly, and you must also commit when you are finished with your task. You can commit by typing:

`git commit -am "commit message"`

and you should leave a detailed commit message describing the changes you made.

## 3 Merge your work into master
Now that you've finished your task you need to checkout master and merge your work. To checkout master simply type:

`git checkout master`

and to merge your task branch type:
`git merge task_branch`

where task_branch is the name of your branch.

## 4 Push the master branch
Now that your work is merged, go ahead and push the master branch by typing:

`git push origin master`

Git Commands
============

_A list of my commonly used Git commands_

*If you are interested in my Git aliases, have a look at my `.bash_profile`, found here: https://github.com/joshnh/bash_profile/blob/master/.bash_profile*

--

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git diff [source branch] [target branch]` | Preview changes before merging |

### Reset & Undo it

| Command | Description |
| ------- | ----------- |
| `git reset --hard HEAD` | Reset to the Last Commit |
and Reset to a Specific Older Commit #
| `git log --oneline` | Find the commit hash using this Command | 
| `git reset --hard <commit-hash>` | Reset to a commit (exampe: git reset --hard 9f8e7d6) |
and Undo a Hard Reset (if needed)
| `git reflog` | Undo a Hard Reset |
