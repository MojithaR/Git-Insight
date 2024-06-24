# Git-Insight
Comprehensive guide to mastering essential Git commands.

# GitInsight Cheat Sheet 🚀

## 1. Configuration 🔧
```sh
# Set your username
git config --global user.name "Your Name"

# Verify your username
git config --global user.name

# Set your email
git config --global user.email "you@example.com"

# Verify your email
git config --global user.email
```

## 2. Creating and Adding a Project to Git 🗂️
```sh
# Initialize a new Git repository
git init

# Check the status of the repository
git status

# Add all files to the staging area
git add .

# Commit the files with a message
git commit -m "Initial commit"

# Add a remote repository URL
git remote add origin http://your.git.repo.url/repository.git

# Push changes to the remote repository
git push -u origin master
```

## 3. Fork and Merge 🍴🔀
- **Forking a Repository**
  1. Login to GitLab.
  2. Navigate to your project.
  3. Click on the **Fork** button.
  - Forking allows making changes without affecting the original project.

## 4. GitLab Runner 🏃‍♂️
- **Used in GitLab CI for Continuous Integration**

| Step | Description                           | Command/Link                      |
|------|---------------------------------------|-----------------------------------|
| 1    | Install GitLab Runner                 | [GitLab Runner Install Guide](https://docs.gitlab.com/runner/install/) |
| 2    | Register GitLab Runner                | `gitlab-runner.exe register`      |
| 3    | Start GitLab Runner                   | `gitlab-runner.exe start`         |
| 4    | Check runner is started in the project | Verify in GitLab UI               |

## 5. Basic Git Commands 📋
### Initializing a Repository
```sh
git init
```

### Staging Files 📥
```sh
# Stage a single file
git add file1.js

# Stage multiple files
git add file1.js file2.js

# Stage with a pattern
git add *.js

# Stage the current directory and all its content
git add .
```

### Viewing Status 🔍
```sh
# Full status
git status

# Short status
git status -s
```

### Committing the Staged Files 📝
```sh
# Commit with a one-line message
git commit -m "Message"

# Open the default editor to type a long message
git commit
```

### Skipping the Staging Area 🚀
```sh
git commit -am "Message"
```

## 6. Working with Files 🗃️
### Removing Files 🗑️
```sh
# Remove from working directory and staging area
git rm file1.js

# Remove from staging area only
git rm --cached file1.js
```

### Renaming/Moving Files 📂
```sh
git mv file1.js file1.txt
```

## 7. Viewing Changes 🔄
### Viewing Staged/Unstaged Changes
```sh
# Shows unstaged changes
git diff

# Shows staged changes
git diff --staged
```

### Viewing History 📜
```sh
# Full history
git log

# Summary
git log --oneline

# Lists the commits from the oldest to the newest
git log --reverse
```

### Viewing a Specific Commit 🔍
```sh
# Shows the given commit
git show 921a2ff

# Shows the last commit
git show HEAD
```

## 8. Undoing Changes 🕒
### Unstaging Files
```sh
# Copies the last version of file.js from repo to index
git restore --staged file.js
```

### Discarding Local Changes
```sh
# Copies file.js from index to working directory
git restore file.js

# Restores multiple files in working directory
git restore file1.js file2.js

# Discards all local changes (except untracked files)
git restore .

# Removes all untracked files
git clean -fd
```

## 9. Restoring Earlier Versions 📅
### Restoring File to an Earlier Version
```sh
git restore --source=HEAD~2 file.js
```

## 10. Browsing History 🔍
### Viewing Commit History
```sh
# Shows the list of modified files
git log --stat

# Shows the actual changes (patches)
git log --patch
```

### Filtering History
```sh
# Shows the last 3 entries
git log -3

# Shows commits by a specific author
git log --author="Author Name"

# Shows commits before a specific date
git log --before="2020-08-17"

# Shows commits after a specific date
git log --after="one week ago"

# Shows commits with specific message
git log --grep="GUI"

# Shows commits with specific changes
git log -S"GUI"

# Shows range of commits
git log hash1..hash2

# Shows commits that touched file.txt
git log file.txt
```

### Formatting Log Output
```sh
git log --pretty=format:"%an committed %H"
```

## 11. Aliases 🔤
### Creating an Alias
```sh
git config --global alias.lg "log --oneline"
```

## 12. Comparing Commits 🔄
### Comparing Different Commits
```sh
# Shows the changes between two commits
git diff HEAD~2 HEAD

# Shows changes to file.txt only
git diff HEAD~2 HEAD file.txt
```

## 13. Checking Out Commits 🔎
### Checking Out a Commit
```sh
# Checks out the given commit
git checkout dad47ed

# Checks out the master branch
git checkout master
```

## 14. Finding Contributors 🌟
### Viewing Shortlog
```sh
git shortlog
```

## 15. Tagging 🏷️
### Creating and Managing Tags
```sh
# Tags the last commit as v1.0
git tag v1.0

# Tags an earlier commit
git tag v1.0 5e7a828

# Lists all the tags
git tag

# Deletes the given tag
git tag -d v1.0
```

## 16. Branching & Merging 🌿🔀
### Managing Branches
```sh
# Creates a new branch called bugfix
git branch bugfix

# Switches to the bugfix branch
git checkout bugfix

# Same as the above
git switch bugfix

# Creates and switches to a new branch
git switch -C bugfix

# Deletes the bugfix branch
git branch -d bugfix
```

### Comparing Branches
```sh
# Lists the commits in the bugfix branch not in master
git log master..bugfix

# Shows the summary of changes
git diff master..bugfix
```

### Stashing Changes 💾
```sh
# Creates a new stash
git stash push -m "Message"

# Lists all the stashes
git stash list

# Shows the given stash
git stash show stash@{1}

# Shortcut for stash@{1}
git stash show 1

# Applies the given stash to the working directory
git stash apply 1

# Deletes the given stash
git stash drop 1

# Deletes all the stashes
git stash clear
```

### Merging Branches
```sh
# Merges the bugfix branch into the current branch
git merge bugfix

# Creates a merge commit even if FF is possible
git merge --no-ff bugfix

# Performs a squash merge
git merge --squash bugfix

# Aborts the merge
git merge --abort
```

## 17. Rebasing & Cherry Picking 🔄🍒
### Rebasing
```sh
# Changes the base of the current branch
git rebase master
```

### Cherry Picking
```sh
# Applies the given commit on the current branch
git cherry-pick dad47ed
```

## 18. Collaboration 🤝
### Cloning a Repository
```sh
git clone url
```

### Syncing with Remotes
```sh
# Fetches master from origin
git fetch origin master

# Fetches all objects from origin
git fetch origin

# Shortcut for `git fetch origin`
git fetch

# Fetch + merge
git pull

# Pushes master to origin
git push origin master

# Shortcut for `git push origin master`
git push
```

### Sharing Tags and Branches
```sh
# Pushes tag v1.0 to origin
git push origin v1.0

# Shows remote tracking branches
git branch -r

# Shows local & remote tracking branches
git branch -vv

# Pushes bugfix to origin
git push -u origin bugfix

# Removes bugfix from origin
git push -d origin bugfix
```

### Managing Remotes
```sh
# Shows remote repositories
git remote

# Adds a new remote called upstream
git remote add upstream url

# Removes upstream
git remote rm upstream
```

## 19. Rewriting History 📜

### Undoing Commits

#### Removes the last commit, keeps changes staged
```sh
git reset --soft HEAD^
```
#### Unstages the changes as well
```sh
git reset --mixed HEAD^
```
#### Discards local changes
```sh
git reset --hard HEAD^
```

### Reverting Commits ↩️

#### Reverts the given commit
```sh
git revert 72856ea
```
#### Reverts the last three commits
```sh
git revert HEAD~3..
```
#### Reverts the changes without creating a commit
```sh
git revert --no-commit HEAD~3..
```

### Recovering Lost Commits 🔄

#### Viewing Reflog

##### Shows the history of HEAD
```sh
git reflog
```

##### Shows the history of bugfix pointer
```sh
git reflog show bugfix
```

### Amending Commits 📝

#### Amending the Last Commit

##### Amend the last commit with new changes
```sh
git commit --amend
```

### Interactive Rebasing 🔄

#### Rebase interactively to edit commit history
```sh
git rebase -i HEAD~5
```
