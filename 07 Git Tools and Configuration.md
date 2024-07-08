# 7. Git Tools and Configuration

## Git Config ⚙️

Git Config is used to set your Git configuration at three levels: system, global, and local. This allows you to customize your Git environment.

### How to Use Git Config

1. **Set Your Name:**
   ```sh
   git config --global user.name "Your Name"
   ```

2. **Set Your Email:**
   ```sh
   git config --global user.email "your.email@example.com"
   ```

3. **View All Configurations:**
   ```sh
   git config --list
   ```

### Example Workflow

1. **Set Name:**
   ```sh
   git config --global user.name "Your Name"
   ```

2. **Set Email:**
   ```sh
   git config --global user.email "your.email@example.com"
   ```

3. **View Configurations:**
   ```sh
   git config --list
   ```

### Summary Table

| Command                                   | Description                               |
|-------------------------------------------|-------------------------------------------|
| `git config --global user.name "Your Name"` | Set your global Git username             |
| `git config --global user.email "your.email@example.com"` | Set your global Git email                |
| `git config --list`                       | View all Git configurations               |

Configuring Git with your name and email ensures that your commits are properly attributed to you.

## Git Aliases 🧩

Git Aliases are shortcuts that save you time by shortening long Git commands. You can create your own custom aliases to speed up your workflow.

### How to Create Git Aliases

1. **Create a Simple Alias:**
   ```sh
   git config --global alias.co checkout
   ```

2. **Create an Alias with Multiple Commands:**
   ```sh
   git config --global alias.s "status -s"
   ```

### Example Workflow

1. **Create a Checkout Alias:**
   ```sh
   git config --global alias.co checkout
   ```

2. **Create a Status Alias:**
   ```sh
   git config --global alias.s "status -s"
   ```

3. **Use Aliases:**
   ```sh
   git co main
   git s
   ```

### Summary Table

| Command                                | Description                             |
|----------------------------------------|-----------------------------------------|
| `git config --global alias.co checkout` | Create an alias for `checkout`          |
| `git config --global alias.s "status -s"` | Create an alias for `status -s`         |
| `git co main`                          | Use the `checkout` alias                |
| `git s`                                | Use the `status -s` alias               |

Using aliases helps speed up your workflow by reducing the amount of typing needed for common commands.

## Git Hooks 🔗

Git Hooks are scripts that run automatically in response to certain events in a Git repository. They can automate tasks like pre-commit checks, post-commit notifications, and more.

### How to Use Git Hooks

1. **Navigate to Hooks Directory:**
   ```sh
   cd .git/hooks
   ```

2. **Create or Edit a Hook Script:**
   ```sh
   nano pre-commit
   ```

3. **Make the Script Executable:**
   ```sh
   chmod +x pre-commit
   ```

### Example Workflow

1. **Navigate to Hooks Directory:**
   ```sh
   cd .git/hooks
   ```

2. **Create a Pre-commit Hook:**
   ```sh
   echo -e "#!/bin/sh\n\n# Check for forbidden files\nforbidden_files=(passwords.txt secrets.yml)\n\nfor file in \"\${forbidden_files[@]}\"; do\n  if [ -f \$file ]; then\n    echo \"Error: \$file exists. Remove it before committing.\"\n    exit 1\n  fi\ndone\n" > pre-commit
   ```

3. **Make the Hook Executable:**
   ```sh
   chmod +x pre-commit
   ```

### Summary Table

| Step                                    | Description                             |
|-----------------------------------------|-----------------------------------------|
| `cd .git/hooks`                         | Navigate to the Git hooks directory     |
| `nano pre-commit`                       | Create or edit a pre-commit hook script |
| `chmod +x pre-commit`                   | Make the hook script executable         |

Git Hooks automate various tasks and enforce project standards, ensuring that certain conditions are met before changes are committed or pushed.

---
