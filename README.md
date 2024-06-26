# Learn-Git-GitHub
Complete Git and GitHub **(Author: Sheraz Ahmad)**</br></br></br></br>
Git and GitHub are two related but distinct concepts:

**Git**:

* A local version control system that runs on a developer's machine.
* Helps manage code and track changes locally.
* Allows developers to create a local repository to store and manage their code.

**GitHub**:

* A web-based platform that provides a remote repository for storing and managing code.
* A website that allows developers to store and share their Git repositories online.
* Provides a collaborative platform for developers to work together on projects, track changes, and manage different versions of their code.

In summary, Git is a local tool for managing code, while GitHub is a web-based platform for storing and sharing Git repositories, facilitating collaboration and version control.
</br> </br> </br> </br>
**How to Config git**


1. Set up your username and email address:
```
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```
2. Configure your Git settings:
```
git config -l
```
This will list all your Git settings.

3. Set up your default editor:
```
git config --global core.editor "your_editor"
```
Replace "your_editor" with your preferred editor, such as Notepad or Visual Studio Code.

4. Check your Git configuration:
```
git config -l
```
This will display your current Git configuration settings.

Additionally, the tutorial mentions setting up your Git configuration at a global level using the `--global` flag, and at a local level using the `--local` flag.

For example, to set up your username and email address at a global level:
```
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```
And to set up your username and email address at a local level (for a specific repository):
```
git config --local user.name "Your Name"
git config --local user.email "your_email@example.com"
```
It's also important to note that you can configure Git using a Git configuration file, usually located at `~/.gitconfig` on Linux and macOS, or `C:\Users\<YourUsername>\.gitconfig` on Windows. </br> </br> </br> 
**Here are the explanations for "clone" and "status" in the context of Git**:

**Clone:**
The `clone` command is used to create a local copy of a remote Git repository. It allows you to download a project from GitHub or another Git repository to your local machine. When you clone a repository, you are essentially creating a duplicate of the original project, which you can then modify and work on locally.

**Status:**
The `status` command is used to check the status of your local Git repository. It shows you the current state of your project, including any changes you've made, files that are staged or unstaged, and any conflicts or issues that need to be resolved. The `status` command helps you keep track of your changes and ensures that you're aware of any modifications that need to be committed or pushed to the remote repository.

In summary, `clone` is used to download a remote repository to your local machine, while `status` is used to check the current state of your local repository.
</br></br></br></br>

**4 Stages of files**

In Git, files in your repository can be in one of four states:

1. **Untracked**: A file that is not being tracked by Git. It's a new file that you've created or downloaded, but you haven't told Git to track it yet. Git doesn't know about this file, and it won't be included in your next commit.

2. **Modified**: A file that has been changed since the last commit. You've made some changes to the file, but you haven't committed those changes yet. Git knows about the file and has seen the changes, but it's waiting for you to commit them.

3. **Staged**: A file that has been modified and is ready to be committed. You've made changes to the file, and you've told Git to include those changes in your next commit. The file is now in the staging area, waiting to be committed.

4. **Unmodified**: A file that hasn't been changed since the last commit. The file is exactly the same as it was in the last commit, and Git doesn't need to do anything with it.

These states are important because they help you manage your changes and decide what to commit and what not to commit.
</br></br></br></br>
**How to pull any changes full process**
Here is the full process of pulling and pushing changes in a file using Git:

**Step 1: Make changes to your local file**

* Open your file in a text editor and make the necessary changes.
* Save the file.

**Step 2: Add the changes to the staging area**

* Open a terminal or command prompt and navigate to your local Git repository.
* Use the command `git add <file name>` to add the changes to the staging area.
* Replace `<file name>` with the actual name of your file.

Example: `git add index.html`

**Step 3: Commit the changes**

* Use the command `git commit -m "<commit message>"` to commit the changes.
* Replace `<commit message>` with a brief description of the changes you made.

Example: `git commit -m "Updated index.html file"`

**Step 4: Push the changes to the remote repository**

* Use the command `git push origin <branch name>` to push the changes to the remote repository.
* Replace `<branch name>` with the actual name of your branch (e.g. "main", "master", etc.).

Example: `git push origin main`

**Step 5: Pull changes from the remote repository (if necessary)**

* If someone else has made changes to the remote repository, you may need to pull those changes to your local repository.
* Use the command `git pull origin <branch name>` to pull the changes.

Example: `git pull origin main`

Here's the full process with commands:
```
# Make changes to your local file
#...

# Add the changes to the staging area
git add index.html

# Commit the changes
git commit -m "Updated index.html file"

# Push the changes to the remote repository
git push origin main

# Pull changes from the remote repository (if necessary)
git pull origin main
```
Note: Make sure to replace `<file name>` and `<branch name>` with the actual names of your file and branch.

Also, if you want to pull and push changes in a single command, you can use `git pull --rebase origin <branch name>` and then `git push origin <branch name>`. This will pull the changes from the remote repository, rebase your local changes on top of the pulled changes, and then push the updated changes to the remote repository.</br></br>

**How To Clone Repo in Local from GitHub**</br></br>
According to the tutorial, to clone a repository in your local system, you can use the `git clone` command followed by the URL of the repository you want to clone.

The syntax is:
```
git clone <repository_url>
```
For example:
```
git clone https://github.com/user/repository_name.git
```
This will create a local copy of the repository in your current working directory.

Additionally, the tutorial mentions that you can also clone a repository using the GitHub desktop application or by downloading a ZIP file of the repository and extracting it to your local system.
</br></br></br>

**Branch Commands**
</br></br>
The branch command in Git is used to create, list, rename, and delete branches in a repository. Here are some common use cases of the branch command:

1. To create a new branch:
   ```
   git branch <branch_name>
   ```

2. To list all branches in the repository:
   ```
   git branch
   ```

3. To rename a branch:
   ```
   git branch -m <old_branch_name> <new_branch_name>
   ```

4. To delete a branch:
   ```
   git branch -d <branch_name>
   ```

These commands help in managing different lines of development within a Git repository.

**Git Pull Command**</br></br>
The command `git pull origin main` is used to fetch the changes from the remote repository named "origin" and merge them into the local branch "main". 

Here's a breakdown of the command:
- `git pull`: This command combines the `git fetch` command (to retrieve changes from the remote repository) and the `git merge` command (to integrate those changes into the current branch).
- `origin`: This is the name of the remote repository from which you want to fetch changes.
- `main`: This specifies the branch in the remote repository that you want to pull changes from and merge into your current local branch.
</br></br></br>

**Basic Commands used in git** </br></br>
Here is a brief explanation of the Git commands mentioned in the tutorial:

1. **Clone**: This command is used to create a copy of a remote repository on your local machine. It is typically used when you want to start working on an existing project.

   Command: `git clone <repository-url>`

2. **Status**: This command shows the current status of your working directory and staging area. It displays information about untracked files, modified files, and staged files.

   Command: `git status`

3. **Add**: This command is used to add changes from the working directory to the staging area. It prepares the changes to be included in the next commit.

   Command: `git add <file-name>`

4. **Commit**: This command is used to record the changes in the repository. It creates a snapshot of the changes that have been staged.

   Command: `git commit -m "Commit message"`

5. **Push**: This command is used to upload local repository content to a remote repository. It is used to share your changes with others.

   Command: `git push <remote-name> <branch-name>`

6. **Reset**: This command is used to undo changes in the working directory and staging area. It can be used to unstage files or reset changes to a previous commit.

   Command: `git reset <file-name>` or `git reset --hard <commit-hash>`

These commands are fundamental to working with Git and are commonly used in version control workflows.












