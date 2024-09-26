## 1. GitHub Commands

GitHub commands revolve around the `git` version control system, which allows you to manage changes to your project over time. Below are some basic `git` commands you'll frequently use when working with GitHub.

### 1.1 Basic Git Commands (not needed)
1. **Create/Initialize a Git Repository**
   Before you can use `git` commands, you need to initialize a repository.

   ```bash
   git init
   ```

   This command initializes a new Git repository in your project directory.

2. **Clone a Repository**
   To copy a remote Git repository to your local machine, use:

   ```bash
   git clone <repository-url>
   ```

   This command clones the repository found at `<repository-url>` to your local machine.

### 1.2 Git Commands (usual workflow)

3. **Check Repository Status (VERY USEFUL, EXECUTE IT BEFORE ANY OTHER ACTION)**
   To see the status of your repository, including changes that have been staged, changes that haven’t been staged, and files that aren’t being tracked by Git:

   ```bash
   git status
   ```

4. **Add Changes to the Staging Area**
   To add changes to the staging area so they can be committed, use:

   ```bash
   git add <file>
   ```
   Do not add multiple files (all the files in a folder) at once, this can lead to problems.

5. **Commit Changes**
   To save your staged changes to the repository’s history:

   ```bash
   git commit -m "Your commit message here"
   ```

6. **Push Changes to GitHub**
   To push your committed changes to a remote repository like GitHub:
   ```bash
   git push
   ```
   This command pushes changes to the specified `<branch-name>` of the remote repository named `origin`.
   ```bash
   git push origin <branch-name>
   ```

8. **Pull Changes from GitHub**
   To pull the latest changes from a remote repository:
   ```bash
   git pull
   ```
   This command updates your local repository with changes from the remote `<branch-name>`.
   ```bash
   git pull origin <branch-name>
   ```

### 1.3 Other more advance git commands
9. **Revert a Local Commit**
   If you need to undo a commit you’ve made locally but haven’t pushed to the remote repository yet, you can use:

   ```bash
   git reset --soft HEAD~1
   ```

   This command undoes the last commit but keeps the changes in your working directory.

   To completely remove changes and commits:

   ```bash
   git reset --hard HEAD~1
   ```

   **Warning**: `--hard` will delete all changes permanently.

10. **Create a New Branch**
    To create a new branch from the current branch:

    ```bash
    git checkout -b <new-branch-name>
    ```

11. **Switch to an Existing Branch**
    To switch to an existing branch:

    ```bash
    git checkout <branch-name>
    ```

12. **Delete a Branch**
    To delete a local branch that is no longer needed:

    ```bash
    git branch -d <branch-name>
    ```

    To delete a remote branch:

    ```bash
    git push origin --delete <branch-name>
    ```

13. **Merge Branches**
    To merge another branch into your current branch:

    ```bash
    git merge <branch-name>
    ```

    This command will merge `<branch-name>` into your current branch. Make sure to commit or stash any changes before merging.

14. **Stash Changes**
    If you want to save changes that you’re not ready to commit yet, use:

    ```bash
    git stash
    ```

    To apply the stashed changes later:

    ```bash
    git stash pop
    ```
