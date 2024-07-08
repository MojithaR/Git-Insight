# 2. Basic Git Concepts

## Repositories 📦

A **repository** (or **repo**) is essentially a directory that stores your project's files and the entire revision history of the files. This allows you to track changes, revert to previous states, and collaborate with others on the same project.

### Types of Repositories

#### Local Repository
A **local repository** is stored on your computer. It allows you to work on your project without an internet connection. All changes you make are saved locally until you decide to share them.

#### Remote Repository
A **remote repository** is stored on a server and can be accessed by others. GitHub, GitLab, and Bitbucket are popular platforms for hosting remote repositories. By using remote repositories, multiple people can work on the same project simultaneously, pulling updates, and pushing their changes.

### Creating a Repository

#### Local Repository
To create a local repository, navigate to your project's directory and initialize it with Git:
```sh
git init
```
This command sets up all the necessary files for Git to start tracking your project.

#### Remote Repository
To create a remote repository, you can use a service like GitHub. After creating a new repository on GitHub, link it to your local repository:
```sh
git remote add origin https://github.com/yourusername/your-repo.git
```
Push your initial commit:
```sh
git push -u origin main
```

### Summary Table

| Type   | Description                                                      |
|--------|------------------------------------------------------------------|
| Local  | Stored on your computer. Allows offline work.                    |
| Remote | Stored on a server. Enables collaboration and backups.           |

Repositories are fundamental in Git, serving as the cornerstone for version control, enabling efficient project management and collaboration.

---

## Commits 📝

A **commit** in Git is a record of changes made to the repository. Each commit serves as a snapshot of your project at a particular point in time, allowing you to track changes, revert to previous states, and understand the history of the project.

### Creating a Commit

1. **Stage Changes:** Before committing, you need to stage the files that have changed. This adds them to the staging area.
   ```sh
   git add filename
   ```
   To stage all changes, use:
   ```sh
   git add .
   ```
2. **Commit Changes:** Once the files are staged, you can commit them with a descriptive message.
   ```sh
   git commit -m "Your commit message"
   ```

### Best Practices for Commit Messages

- **Be Descriptive:** Use clear, concise messages that describe the changes.
  ```sh
  git commit -m "Fix typo in README"
  ```
- **Use Present Tense:** Write messages as if you are giving instructions, not narrating.
  ```sh
  git commit -m "Add user login functionality"
  ```
- **Keep It Short:** Aim for 50 characters or less for the summary line.

### Example Workflow

1. **Stage Changes:**
   ```sh
   git add .
   ```
2. **Commit Changes:**
   ```sh
   git commit -m "Initial commit with project structure"
   ```

### Viewing Commit History

To see the commit history, use:
```sh
git log
```
This command shows a list of commits, including the commit ID, author, date, and message.

### Summary Table

| Command            | Description                           |
|--------------------|---------------------------------------|
| `git add filename` | Stage specific file                   |
| `git add .`        | Stage all changes                     |
| `git commit -m`    | Commit with a message                 |
| `git log`          | View commit history                   |

Commits are the building blocks of Git history, capturing the evolution of your project and facilitating collaboration and change tracking.

---

## Branches 🌿

A **branch** in Git allows you to diverge from the main line of development and continue to work without affecting the main project. This is especially useful for working on features, fixing bugs, or experimenting.

### Creating and Switching Branches

#### Create a New Branch
To create a new branch, use:
```sh
git branch branch-name
```
This creates a new branch named `branch-name`.

#### Switch to a Branch
To switch to the newly created branch, use:
```sh
git checkout branch-name
```

#### Create and Switch to a New Branch
Combine the creation and switch commands:
```sh
git checkout -b branch-name
```
This creates and switches to `branch-name` in one step.

### Working with Branches

When you create a new branch, you can make changes without affecting the `main` branch. Once your changes are ready, you can merge the branch back into `main`.

#### Merge a Branch
Switch to the `main` branch:
```sh
git checkout main
```
Merge the feature branch:
```sh
git merge branch-name
```

### Resolving Conflicts

Sometimes, changes in different branches conflict. Git will prompt you to resolve these conflicts manually.

### Example Workflow

1. **Create and Switch to a New Branch:**
   ```sh
   git checkout -b feature-branch
   ```
2. **Make Changes and Commit:**
   ```sh
   git add .
   git commit -m "Add new feature"
   ```
3. **Merge Changes to Main:**
   ```sh
   git checkout main
   git merge feature-branch
   ```

### Summary Table

| Command                      | Description                          |
|------------------------------|--------------------------------------|
| `git branch branch-name`     | Create a new branch                  |
| `git checkout branch-name`   | Switch to a branch                   |
| `git checkout -b branch-name`| Create and switch to a new branch    |
| `git merge branch-name`      | Merge a branch into the current branch|

Branches are powerful tools in Git, allowing for isolated development and seamless integration, enhancing productivity and collaboration.

---
