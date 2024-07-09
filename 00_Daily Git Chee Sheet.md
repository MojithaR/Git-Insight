# GitLab Daily Cheat Sheet 🚀

## 1. Configuration 🔧
```sh
# Set your username and email
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

# Verify settings
git config --global user.name
git config --global user.email
```

## 2. Initializing and Adding Project 🗂️
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

## 3. Creating and Switching Branches 🌿
```sh
# Create and switch to a new branch
git checkout -b new-feature

# Switch to an existing branch
git checkout branch-name
```

## 4. Pushing Changes 🚀
```sh
# Add and commit changes
git add .
git commit -m "Your commit message"

# Push changes to the current branch
git push origin branch-name
```

## 5. Handling Errors ⚠️
### Common Errors and Solutions
#### Error: `fatal: not a git repository (or any of the parent directories): .git`
- **Solution**: Ensure you are in the correct directory or initialize a Git repository.
  ```sh
  git init
  ```

#### Error: `error: failed to push some refs`
- **Solution**: Pull the latest changes and resolve conflicts before pushing.
  ```sh
  git pull origin branch-name --rebase
  git push origin branch-name
  ```

#### Error: `merge conflict in file`
- **Solution**: Manually resolve the conflicts in the file, then add and commit the resolved file.
  ```sh
  git add conflict-file
  git commit -m "Resolved merge conflict in file"
  ```

#### Error: `detached HEAD`
- **Solution**: Switch back to a branch.
  ```sh
  git checkout branch-name
  ```

#### Error: `error: Your local changes to the following files would be overwritten by merge`
- **Solution**: Stash your changes, pull the latest updates, then apply the stash.
  ```sh
  git stash
  git pull origin branch-name
  git stash apply
  ```

## 6. Best Practices 📝
- **Always create a new branch for new features or fixes**:
  ```sh
  git checkout -b feature-name
  ```
- **Commit frequently with clear messages**:
  ```sh
  git commit -m "Add feature X"
  ```
- **Pull latest changes before pushing**:
  ```sh
  git pull origin branch-name
  ```
- **Push to remote frequently**:
  ```sh
  git push origin branch-name
  ```

---
