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
It's also important to note that you can configure Git using a Git configuration file, usually located at `~/.gitconfig` on Linux and macOS, or `C:\Users\<YourUsername>\.gitconfig` on Windows.


