# 10. Git Troubleshooting

## Common Issues and Solutions 🛠️

Git can sometimes present challenges when working on projects. Here are some common issues you might encounter and their solutions:

### Common Git Issues and Solutions

| Issue                                      | Solution                                                      |
|--------------------------------------------|---------------------------------------------------------------|
| **Merge Conflict**                         | Resolve conflicts by editing conflicting files and committing changes. |
| **Forgot to Add Files Before Committing**   | Add missed files using `git add` and amend your commit with `git commit --amend`. |
| **Detached HEAD State**                    | Reattach HEAD to a branch using `git checkout -b new-branch HEAD`. |
| **Accidental Commit to Wrong Branch**       | Cherry-pick commits to the correct branch using `git cherry-pick` or reset using `git reset`. |
| **Forgot to Push Changes**                  | Push commits to remote using `git push`.                        |
| **Untracked Files**                        | Add untracked files to `.gitignore` or stage them using `git add`. |

### Example Troubleshooting

1. **Merge Conflict:**
   ```sh
   # Edit conflicting files
   git add .
   git commit -m "Resolve merge conflict"
   ```

2. **Detached HEAD State:**
   ```sh
   git checkout -b new-branch HEAD
   ```

### Summary Table

| Issue                                 | Solution                                                         |
|---------------------------------------|------------------------------------------------------------------|
| Merge Conflict                        | Resolve conflicts by editing conflicting files and committing changes. |
| Forgot to Add Files Before Committing  | Use `git add` to stage missed files and `git commit --amend` to amend commit. |
| Detached HEAD State                   | Reattach HEAD to a branch using `git checkout -b new-branch HEAD`. |
| Accidental Commit to Wrong Branch      | Cherry-pick commits or reset using `git cherry-pick` or `git reset`. |
| Forgot to Push Changes                 | Push commits to remote using `git push`.                          |
| Untracked Files                       | Add files to `.gitignore` or stage them using `git add`.          |

Addressing these common Git issues effectively keeps your workflow smooth and productive.

## Debugging Tools 🛠️🔍

Git provides several tools to help debug issues and understand what’s happening in your repository.

### Useful Debugging Tools

1. **git log:**
   - View commit history, changes, and authors.
   ```sh
   git log
   ```

2. **git reflog:**
   - View a detailed history of all Git actions, including resets and rebases.
   ```sh
   git reflog
   ```

3. **git diff:**
   - Compare changes between commits, branches, or files.
   ```sh
   git diff HEAD~1..HEAD
   ```

### Example Usage

1. **View Commit History:**
   ```sh
   git log
   ```

2. **View Detailed History:**
   ```sh
   git reflog
   ```

3. **Compare Changes:**
   ```sh
   git diff main..feature-branch
   ```

### Summary Table

| Tool                                  | Description                                                      |
|---------------------------------------|------------------------------------------------------------------|
| git log                               | View commit history, changes, and authors.                       |
| git reflog                            | View detailed history of all Git actions.                        |
| git diff                              | Compare changes between commits, branches, or files.             |

Using Git’s debugging tools helps diagnose issues, understand changes, and maintain a clear project history.

---
