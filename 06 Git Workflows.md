# 6. Git Workflows

## Feature Branch Workflow 🌟

The Feature Branch Workflow involves creating a new branch for each feature or bug fix. This allows for isolated development and easier integration.

### How to Use Feature Branch Workflow

1. **Create a New Branch:**
   ```sh
   git checkout -b feature-branch
   ```
   This creates and switches to a new branch called `feature-branch`.

2. **Make Changes and Commit:**
   ```sh
   git add .
   git commit -m "Add new feature"
   ```

3. **Push the Branch to Remote:**
   ```sh
   git push origin feature-branch
   ```

4. **Create a Pull Request:** Go to GitHub, create a pull request from `feature-branch` to `main`.

### Example Workflow

1. **Create Branch:**
   ```sh
   git checkout -b feature-branch
   ```

2. **Make Changes:**
   ```sh
   git add .
   git commit -m "Implement feature"
   ```

3. **Push Changes:**
   ```sh
   git push origin feature-branch
   ```

4. **Create Pull Request:** Open a pull request on GitHub.

### Summary Table

| Step                                | Description                            |
|-------------------------------------|----------------------------------------|
| `git checkout -b feature-branch`    | Create and switch to a new feature branch |
| `git add .`                         | Stage your changes                     |
| `git commit -m "Implement feature"` | Commit your changes                    |
| `git push origin feature-branch`    | Push the feature branch to remote      |
| Create Pull Request                 | Propose changes to be merged           |

Feature Branch Workflow helps keep the main branch stable and ensures new features are properly reviewed before merging.

## Gitflow Workflow 🚀

The Gitflow Workflow is a set of guidelines that define a strict branching model designed around the project release cycle. It includes feature branches, develop and main branches, and release and hotfix branches.

### How to Use Gitflow Workflow

1. **Initialize Gitflow:**
   ```sh
   git flow init
   ```

2. **Create a Feature Branch:**
   ```sh
   git flow feature start feature-name
   ```

3. **Finish a Feature:**
   ```sh
   git flow feature finish feature-name
   ```

4. **Create a Release Branch:**
   ```sh
   git flow release start release-version
   ```

5. **Finish a Release:**
   ```sh
   git flow release finish release-version
   ```

6. **Create a Hotfix Branch:**
   ```sh
   git flow hotfix start hotfix-name
   ```

7. **Finish a Hotfix:**
   ```sh
   git flow hotfix finish hotfix-name
   ```

### Example Workflow

1. **Start Feature:**
   ```sh
   git flow feature start new-feature
   ```

2. **Make Changes and Commit:**
   ```sh
   git add .
   git commit -m "Implement new feature"
   ```

3. **Finish Feature:**
   ```sh
   git flow feature finish new-feature
   ```

### Summary Table

| Step                                     | Description                                   |
|------------------------------------------|-----------------------------------------------|
| `git flow init`                          | Initialize Gitflow                            |
| `git flow feature start feature-name`    | Start a new feature branch                    |
| `git flow feature finish feature-name`   | Finish and merge the feature branch           |
| `git flow release start release-version` | Start a new release branch                    |
| `git flow release finish release-version`| Finish and merge the release branch           |
| `git flow hotfix start hotfix-name`      | Start a new hotfix branch                     |
| `git flow hotfix finish hotfix-name`     | Finish and merge the hotfix branch            |

Gitflow Workflow provides a robust framework for managing larger projects and ensuring smooth releases.

## Forking Workflow 🍴

The Forking Workflow is commonly used in open-source projects. It involves forking a repository, making changes in your fork, and then submitting a pull request to the original repository.

### How to Use Forking Workflow

1. **Fork the Repository:** Click the "Fork" button on the repository's GitHub page.

2. **Clone Your Fork:**
   ```sh
   git clone https://github.com/yourusername/repository.git
   ```

3. **Create a Feature Branch:**
   ```sh
   git checkout -b feature-branch
   ```

4. **Make Changes and Commit:**
   ```sh
   git add .
   git commit -m "Implement feature"
   ```

5. **Push the Branch to Your Fork:**
   ```sh
   git push origin feature-branch
   ```

6. **Create a Pull Request:** Go to the original repository and open a pull request from your forked repository.

### Example Workflow

1. **Fork and Clone:**
   ```sh
   git clone https://github.com/yourusername/repository.git
   cd repository
   git checkout -b feature-branch
   ```

2. **Make Changes and Commit:**
   ```sh
   git add .
   git commit -m "Implement feature"
   ```

3. **Push Changes:**
   ```sh
   git push origin feature-branch
   ```

4. **Create Pull Request:** Open a pull request on the original repository.

### Summary Table

| Step                                  | Description                                  |
|---------------------------------------|----------------------------------------------|
| Fork on GitHub                        | Create a personal copy of the repository     |
| `git clone URL`                       | Clone your fork to your local machine        |
| `git checkout -b feature-branch`      | Create a feature branch                      |
| `git add .`                           | Stage your changes                           |
| `git commit -m "Implement feature"`   | Commit your changes                          |
| `git push origin feature-branch`      | Push the feature branch to your fork         |
| Create Pull Request                   | Propose your changes to the original repository|

The Forking Workflow is ideal for contributing to open-source projects, allowing you to make changes without affecting the original codebase.
