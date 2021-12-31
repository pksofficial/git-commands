Git Commands
============

_A list of my commonly used Git commands_

### Git configuration

| Command | Description |
| ------- | ----------- |
| `git config --global user.name “Your Name”` | Set the name that will be attached to your commits and tags |
| `git config --global user.email “you@example.com”` | Set the email address that will be attached to your commits and tags |
| `git config --global color.ui auto` | Enable some colorization of Git output |
| `git config --global --alias.[alias-name] [git-command]` | Create shortcut for a Git command. E.g. alias.glog log --graph --oneline will set git glog equivalent to git log --graph --oneline |
| `git config --global --edit` | Open the global configuration file in a text editor for manual editing |
| `git config --system core.editor [editor]` | Set text editor used by commands for all users on the machine. [editor] arg should be the command that launches the desired editor (e.g., vi) |

### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

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
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
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

### Inspect & Compare

| Command | Description |
| ------- | ----------- |
| `git log` | Show the commit history for the currently active branch |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git log --follow [file]` | Show the commits that changed file, even across renames |
| `git log --[limit]` | Limit number of commits by [limit]. E.g. git log -5 will limit to 5 commits |
| `git log -p` | Display the full diff of each commit |
| `git log [branchA] [branchB]` | Show the commits on branchA that are not on branchB |
| `git diff [source branch] [target branch]` | Preview changes before merging(show the diff of what is in branchA that is not in branchB) |
| `git show [SHA]` | Show any object in Git in human-readable format |


### Undo, Revert & Reset

| Command | Description |
| ------- | ----------- |
| `git checkout -- [file-name.txt]` | Undo untrack changes (file by file) |
| `git checkout -- .` | Undo untrack changes (all) |
| `git reset [file-name.txt]` | Undo tracked changes (file by file) |
| `git reset` | Undo tracked changes (all) |
| `git revert [commit]` | Revert commit changes (revert & commit) |
| `git revert -n [commit]` | Revert changes (revert) |
| `git reset [commit]` | Reset changes (revert) |
| `git reset -hard [commit]` | Reset changes (revert) |
