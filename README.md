# Git Commands

_A list of commonly used Git commands_

--

### Git configuration

| Command                                     | Description                                       |
| ------------------------------------------- | ------------------------------------------------- |
| `git config --global user.name [user-name]` | Sets user name for every repo in the computer     |
| `git config --global user.email [email]`    | Sets user email for every repo                    |
| `git config user.name [user-name]`          | Sets user email for a single repo in the computer |
| `git config user.email [email]`             | Sets user email for every repo                    |

### Getting & Creating Projects

| Command                                                           | Description                                |
| ----------------------------------------------------------------- | ------------------------------------------ |
| `git init`                                                        | Initialize a local Git repository          |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command                            | Description                                       |
| ---------------------------------- | ------------------------------------------------- |
| `git status`                       | Check status                                      |
| `git add [file-name.txt]`          | Add a file to the staging area                    |
| `git add -A`                       | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes                                    |
| `git rm -r [file-name.txt]`        | Remove a file (or folder)                         |
| `git mv [old name] [new name]`     | Rename a file                                     |

### Branching & Merging

| Command                                              | Description                                                     |
| ---------------------------------------------------- | --------------------------------------------------------------- |
| `git branch`                                         | List branches (the asterisk denotes the current branch)         |
| `git branch -a`                                      | List all branches (local and remote)                            |
| `git branch [branch name]`                           | Create a new branch                                             |
| `git branch -d [branch name]`                        | Delete a branch                                                 |
| `git push origin --delete [branch name]`             | Delete a remote branch                                          |
| `git checkout -b [branch name]`                      | Create a new branch and switch to it                            |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it                          |
| `git checkout [file-name]`                           | Undo the changes in the file                                    |
| `git branch -m [old branch name] [new branch name]`  | Rename a local branch                                           |
| `git checkout [branch name]`                         | Switch to a branch                                              |
| `git checkout -`                                     | Switch to the branch last checked out                           |
| `git checkout -- [file-name.txt]`                    | Discard changes to a file                                       |
| `git merge [branch name]`                            | Merge a branch into the active branch                           |
| `git merge [source branch] [target branch]`          | Merge a branch into a target branch                             |
| `git stash`                                          | Stash changes in a dirty working directory                      |
| `git stash list`                                     | View the list of stashes made at any time                       |
| `git stash apply`                                    | Apply the changes without removing stored files from stash area |
| `git stash pop`                                      | Remove stored files from stash area                             |
| `git stash clear`                                    | Remove all stashed entries                                      |

### Sharing & Updating Projects

| Command                                                                           | Description                                                                      |
| --------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `git push origin [branch name]`                                                   | Push a branch to your remote repository                                          |
| `git push -u origin [branch name]`                                                | Push changes to remote repository (and remember the branch)                      |
| `git push`                                                                        | Push changes to remote repository (remembered branch)                            |
| `git push origin --delete [branch name]`                                          | Delete a remote branch                                                           |
| `git fetch`                                                                       | Downloads commits, files, and refs from a remote repository into your local repo |
| `git pull`                                                                        | Update local repository to the newest commit                                     |
| `git pull origin [branch name]`                                                   | Pull changes from remote repository                                              |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git`     | Add a remote repository                                                          |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH                                          |

### Inspection & Comparison

| Command                                    | Description                                                     |
| ------------------------------------------ | --------------------------------------------------------------- |
| `git log`                                  | View changes                                                    |
| `git log --summary`                        | View changes (detailed)                                         |
| `git log --oneline`                        | View changes (briefly)                                          |
| `git diff [source branch] [target branch]` | Preview changes before merging                                  |
| `git blame`                                | Show what revision and author last modified each line of a file |

### Working with commits

| Command                                | Description                      |
| -------------------------------------- | -------------------------------- |
| `git commit -m [user-message]`         | Commits the staged changes       |
| `git commit --amend -m [user-message]` | Changes the previous commit      |
| `git rebase -i HEAD~[number]`          | squash previous commits into one |
