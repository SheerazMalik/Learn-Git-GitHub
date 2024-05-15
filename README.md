# Learn-Git-GitHub
Complete Git and GitHub (Author: Sheraz Ahmad)
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

Also, if you want to pull and push changes in a single command, you can use `git pull --rebase origin <branch name>` and then `git push origin <branch name>`. This will pull the changes from the remote repository, rebase your local changes on top of the pulled changes, and then push the updated changes to the remote repository.




