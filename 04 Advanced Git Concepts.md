# 4. Advanced Git Concepts

## Rebasing 🔄

Rebasing is a way to integrate changes from one branch into another. It allows you to maintain a clean, linear project history by moving your branch to the tip of another branch.

### How to Rebase

1. **Switch to the Branch You Want to Rebase:**
   ```sh
   git checkout your-branch
   ```
2. **Rebase onto Another Branch:**
   ```sh
   git rebase main
   ```
   This command takes the commits from `your-branch` and re-applies them on top of `main`.

### Example Workflow

1. **Checkout Feature Branch:**
   ```sh
   git checkout feature-branch
   ```
2. **Rebase onto Main:**
   ```sh
   git rebase main
   ```
3. **Resolve Conflicts (if any):**
   Follow Git's instructions to resolve conflicts and continue rebasing:
   ```sh
   git add .
   git rebase --continue
   ```

### Summary Table

| Command                       | Description                                           |
|-------------------------------|-------------------------------------------------------|
| `git checkout your-branch`    | Switch to the branch you want to rebase               |
| `git rebase main`             | Rebase your branch onto another branch (e.g., main)   |
| `git rebase --continue`       | Continue rebasing after resolving conflicts           |

Rebasing helps keep your commit history clean and makes it easier to follow the project's development.

## Cherry-picking 🍒

Cherry-picking allows you to apply specific commits from one branch onto another branch. This is useful when you want to incorporate specific changes without merging entire branches.

### How to Cherry-pick

1. **Find the Commit Hash:** Use `git log` to find the commit hash you want to cherry-pick.
2. **Cherry-pick the Commit:**
   ```sh
   git cherry-pick commit-hash
   ```

### Example Workflow

1. **Find the Commit Hash:**
   ```sh
   git log
   ```
   Copy the hash of the commit you want to cherry-pick.
2. **Cherry-pick the Commit:**
   ```sh
   git cherry-pick a1b2c3d4
   ```

### Summary Table

| Command                          | Description                         |
|----------------------------------|-------------------------------------|
| `git log`                        | View commit history                 |
| `git cherry-pick commit-hash`    | Apply a specific commit to your branch|

Cherry-picking is powerful for selectively applying changes and can be a lifesaver when you need to quickly fix a bug or backport features.

## Stashing 📦

Stashing allows you to save your current work without committing it. You can then switch branches or work on something else, and come back to your stashed changes later.

### How to Stash Changes

1. **Stash Your Changes:**
   ```sh
   git stash
   ```
   This saves your changes and cleans your working directory.
2. **Apply Stashed Changes:**
   ```sh
   git stash apply
   ```
   This reapplies the stashed changes to your working directory.

### Example Workflow

1. **Make Changes:** Edit your files.
2. **Stash Changes:**
   ```sh
   git stash
   ```
3. **Switch Branches:**
   ```sh
   git checkout another-branch
   ```
4. **Apply Stashed Changes:**
   ```sh
   git checkout your-original-branch
   git stash apply
   ```

### Summary Table

| Command                | Description                            |
|------------------------|----------------------------------------|
| `git stash`            | Save your changes without committing   |
| `git stash apply`      | Apply the stashed changes              |
| `git stash list`       | List all stashes                       |
| `git stash drop`       | Delete a specific stash                |

Stashing is incredibly useful for temporarily setting aside changes, allowing you to switch tasks without losing your work.

---
