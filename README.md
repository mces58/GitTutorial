![git&github](github.jpeg)

<div align="center">
<h1>Git & Github</h1>
</div>

> **<u>Git</u>** is a software used as a distributed version control system (VCS). It is utilized to track changes in software projects, manage different versions, and collaborate effectively. Git operates swiftly, flexibly, and reliably.

> **<u>GitHub</u>** is a cloud-based platform built upon Git. It allows you to host, share, and collaborate on projects.

---

:bulb:**Before diving into Git usage, let's take a look at some essential terminal commands.**

#### Here are some basic terminal commands:

- `ls`: It lists the files and folders in the current directory.

- `ls -la`: It lists the files and folders in the current directory in detail, showing permissions, owners, and other attributes of the files.

- `cd [directory]`: It changes the directory to the specified one.

- `cd ..`: It allows the user to move up one directory level from the current directory, effectively navigating to the parent directory.

- `mkdir [folder name]`: It creates a new folder.

- `rmdir`: It is used to delete the specified folder (directory). However, the folder must be empty. If there are files or subfolders inside the folder, the `rmdir` command will not work. If files or subfolders need to be deleted as well, the `rm -rf` command should be used.

- `touch [file name]`: It creates a new file.

- `rm [file name]`: It deletes the specified file.

- `cp [source] [destination]`: It copies the source file to the destination location.

- `mv [source] [destination]`: It moves the source file to the destination location.

- `cat [file name]`: It prints the content of the file to the terminal.

- `grep [word] [file name]`: It finds the lines containing the specified word.

- `chmod [permissions] [file name]`: It changes the permissions of the file.

- `pwd`: It shows the current working directory. You can use this command to find out in which directory you are located.

- `echo 'message' > [file name]`: Writes a "message" containing text or a string of characters to the specified file.

- `nano [file name]`: Used to open and edit a file.

##### These commands will suffice for basic terminal usage.

---

&#128073; **Now that we have covered the basic terminal commands, we can move on to Git commands.**

| Command                         | Description                                                                                                                                                  |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [`git config`](#git_config)     | It is used to configure or view Git configuration settings.                                                                                                  |
| [`git init`](#git_init)         | It is used to initialize an existing directory as an empty Git repository.                                                                                   |
| [`git clone`](#git_clone)       | It is used to create a local copy from a remote Git repository.                                                                                              |
| [`git add`](#git_add)           | It prepares the changes in the working directory to be tracked by Git.                                                                                       |
| [`git commit`](#git_commit)     | It saves the changes staged in the working directory to a local Git repository.                                                                              |
| [`git diff`](#git_diff)         | It shows the differences between the working directory and the index, or between the index and the last commit.                                              |
| [`git reset`](#git_reset)       | It is used to undo changes made in Git or to edit the index.                                                                                                 |
| [`git revert`](#git_revert)     | Instead of reverting the changes of the previous commit, it allows creating a new commit to undo those changes.                                              |
| [`git restore`](#git_restore)   | It is used to revert the contents of the working directory or specific files to their previous commit state or to change them.                               |
| [`git status`](#git_status)     | It shows which files have been modified in the working directory, which ones are staged in the index, and which ones are awaiting commit.                    |
| [`git rm`](#git_rm)             | It is used to remove a file or directory from the Git repository.                                                                                            |
| [`git log`](#git_log)           | It is used to view the commit history in a Git repository.                                                                                                   |
| [`git show`](#git_show)         | It is used to display the changes and commit details of a specific commit detail.                                                                            |
| [`git tag`](#git_tag)           | It is used to add changes in the working directory to the index for Git to track.                                                                            |
| [`git branch`](#git_branch)     | It is used to list the existing branches in the current Git repository or to create a new branch.                                                            |
| [`git checkout`](#git_checkout) | It is used to switch between branches in a Git repository, navigate to a specific commit, or create a new branch.                                            |
| [`git switch`](#git_switch)     | It is a command used in Git version 2.23 and later. This command is used to switch between branches in Git repositories.                                     |
| [`git merge`](#git_merge)       | It is used to merge changes from different branches.                                                                                                         |
| [`git remote`](#git_remote)     | It is used to manage remote Git repositories and interact with them.                                                                                         |
| [`git push`](#git_push)         | It is used to push local commits to a remote Git repository.                                                                                                 |
| [`git fetch`](#git_fetch)       | It is used to fetch new information from a remote Git repository to the local repository, but it does not make any changes to the current working directory. |
| [`git pull`](#git_pull)         | It is used to pull the latest information from a remote Git repository and apply these updates to your local working directory and current branch.           |
| [`git stash`](#git_stash)       | It is used to temporarily store changes you are working on but haven't committed yet, and to clean your working directory.                                   |
