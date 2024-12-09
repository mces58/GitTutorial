![git&github](github.jpeg)

<div align="center">
<h1>Git & Github</h1>
</div>

> **<u>Git</u>** is a software used as a distributed version control system (VCS). It is utilized to track changes in software projects, manage different versions, and collaborate effectively. Git operates swiftly, flexibly, and reliably.

> **<u>GitHub</u>** is a cloud-based platform built upon Git. It allows you to host, share, and collaborate on projects.

---

&#128161;_**Before diving into Git usage, let's take a look at some essential terminal commands.**_

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

&#128073; _**Now that we have covered the basic terminal commands, we can move on to Git commands.**_

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

---

&#128064; _**Now let's look at the commands in more detail.**_

<h3 id="git_config"><ins>01 Git Configuration</ins></h3>

<details>
  <summary><code>git help</code></summary>
    <ul>
      <blockquote>
        This command typically opens the help documentation related to Git commands. Additionally, you can use <code>git help -a</code> to 
        display an alphabetical list of all Git commands. This provides a quick overview of all Git commands.
      </blockquote>
    </ul>
</details>

<details>
  <summary><code>git config --global user.name "your name"</code></summary>
    <ul>
      <blockquote>
        It is used to configure Git settings. This command is used to set the username and is typically defined as a global setting, meaning 
        the username applies to all Git projects on the system.
      </blockquote>
      <blockquote>
        This setting is important for specifying which user made the changes, especially during commit operations.
      </blockquote>
    </ul>
</details>

<details>
  <summary><code>git config --global user.email "your-email@example.com"</code></summary>
    <ul>
      <blockquote>
        It is used to configure Git settings. This command is used to set the user's email address and is typically defined as a global setting, meaning 
        the email address applies to all Git projects on the system.
      </blockquote>
      <blockquote>
        This setting is important for specifying which user made the changes, especially during commit operations.
      </blockquote>
    </ul>
</details>

<details>
  <summary><code>git config --global core.editor "code -w"</code></summary>
    <ul>
      <blockquote>
        This is used to set the user-defined text editor for Git. In this example, it specifies the use of Visual Studio Code (<code>code</code>), 
        and the <code>-w</code> option ensures that Git waits for the editor to close before proceeding. This means you can continue with commit messages 
        or other editing tasks without waiting for Visual Studio Code to close.
      </blockquote>
    </ul>
</details>

<details>
  <summary><code>git config --list(-l)</code></summary>
    <ul>
      <blockquote>
        Used to list Git configuration settings. This command displays the configuration settings and values used by Git.
      </blockquote>
      <blockquote>
        For example, you can use this command to view the username, email address, color preferences, and other settings defined in the Git configuration. 
        The output is typically in <code>key=value</code> format and includes the configured settings for Git.
      </blockquote>
    </ul>
</details>

---

<h3><ins>02 Starting a Project</ins></h3>

<details>
  <summary><code id="git_init">git init [project name]</code></summary>
    <ul>
      <blockquote>
        Used to initialize an existing directory as a Git repository. If [project name] is specified, a folder with this name is created, 
        and the Git repository is initialized within this folder.
      </blockquote>
<pre><code>mkdir my_project
cd my_project</code></pre>
     <li>
        Now, let's initialize this directory as a Git repository using the <code>git init</code> command:
     </li>
<pre><code>git init</code></pre>
    <li>
        This process turns the current directory into an empty Git repository. You can now track files in this directory, commit changes, and 
        use Git's version control features. If you use <code>git init my_project</code>, a folder named <code>my_project</code> will be created, and 
        the Git repository will be initialized inside that folder.
    </li>
    <li>
        When the <code>git init</code> command is executed, Git initializes the current directory as a Git repository and adds a subdirectory 
        named <code>.git</code>. This subdirectory contains all the information and configuration settings for the Git repository. Therefore, running 
        the <code>git init</code> command creates a Git repository and generates the <code>.git</code> directory that holds all the related information.
    </li>
    <li>
        However, if you want to undo this process and delete the Git repository, simply deleting the <code>.git</code> directory is enough. 
        However, this action is irreversible, and you will lose all history, commit information, branch structures, and other related data. 
        Therefore, you should proceed with caution when deleting the directory.
    </li>
    <li>
        For example, after creating a Git repository, you can follow the steps below to delete the repository (use with caution):
    </li>
<pre><code>rm -rf .git</code></pre>
    <li>
        This command completely deletes the <code>.git</code> directory in the current directory.
    </li>
    <li>
        When the <code>-r (recursive)</code> and <code>-f (force)</code> options are included, it deletes the specified directory, along 
        with all files and subdirectories within it, without prompting for confirmation.
    </li>
   </ul>
</details>

<details>
  <summary><code id="git_clone">git clone &lt;project url&gt;</code></summary>
    <ul>
      <blockquote>
        Used to copy a project from a remote Git repository to a local machine. This command downloads the specified Git repository in 
        its entirety and creates a local copy. The <code>&lt;project url&gt;</code> represents the URL of the Git repository to be cloned.
      </blockquote>
      <li>As an example, to clone a GitHub repo:</li>
<pre><code>git clone https://github.com/user/repo-path.git</code></pre>
      <li>
        This command downloads the specified GitHub repository and creates a folder named <code>repository-name</code> in the current directory, 
        copying the contents into it. This allows you to use the entire project on your local machine and make changes to it.
      </li>
   </ul>
</details>

---

<h3><ins>03 Day-to-day Work</ins></h3>

<details>
  <summary><code id="git_status">git status</code></summary>
    <ul>
      <blockquote>
        Displays the status of files in the working directory and index of a Git repository. This command is used to see which files have 
        been modified, which are staged in the index, and which are waiting to be committed. Here are some example usages of the <code>git status</code> command:
      </blockquote>
      <li>Create a new directory and switch to this directory:</li>
<pre><code>mkdir my_project
cd my_project</code></pre>
      <li>
        Check the directory status using the <code>git status</code> command:
      </li>
<pre><code>git status</code></pre>
      <li>The output will be like this:</li>
<pre><code>fatal: Not a git repository (or any of the parent directories): .git</code></pre>
      <li>
        This output indicates that the directory is not yet a Git repository. Therefore, when the <code>git status</code> command is run, Git reports 
        that no repository has been initialized in the directory and returns an error.
      </li>
      <li>Now, let's create the Git repository:</li>
<pre><code>git init</code></pre>
      <li>Check the directory status using the git status command again:</li>
<pre><code>git status</code></pre>
      <li>The output will be like this:</li>
<pre><code>On branch master
No commits yet
nothing to commit (create/copy files and use "git add" to track)</code></pre>
      <li>This output indicates that the Git repository has been created successfully, but no commits have been made yet and there are no files being tracked.</li>
   </ul>
</details>

<details>
  <summary><code id="git_add">git add [file]</code></summary>
    <ol>
      <blockquote>
        The <code>git add</code> command is used to add changes in the working directory to the staging area for Git to track. Here are some 
        examples of using the <code>git add</code> command:
      </blockquote>
      <li><h4>Staging a Single File:</h4></li>
<pre><code># Create a new file
echo "This is an example file" > file.txt
<br/>
# Add the file to the stage
git add file.txt</code></pre>
      <small>In this example, a file named <code>file.txt</code> was created in the working directory and added to the staging area using the <code>git add</code> command</small>
      <li><h4>Staging Multiple Files:</h4></li>
<pre><code># Create new files
echo "hello world 1" > file1.txt
echo "hello world 2" > file2.txt
<br/>
# Add all files to stage
git add file1.txt file2.txt</code></pre>
    <small>In this example, we added multiple files to the stage at once.</small>
    <li><h4>Staging All Changes:</h4></li>
<pre><code># Add all changes in the working directory to the staging area
git add .</code></pre>
    <small>In this example, the <code>.</code> (dot) represents all changes in the working directory. The <code>git add .</code> command stages all files.</small>
      <li><h4>Staging Files of a Specific Type:</h4></li>
<pre><code># Only add files with .txt extension to stage
git add *.txt</code></pre>
    <small>In this example, we only include files with the <code>.txt</code> extension.</small>
    <li><h4>Unstaging Changes:</h4></li>
<pre><code># Unstage a file from the staging area
git reset file.txt</code></pre>
    <small>In this example, we are unstageing the file <code>file.txt</code> that we previously added to the staging area.</small>
   </ol>
</details>

<details>
  <summary><code id="git_diff">git diff [file]</code></summary>
    <ol>
      <blockquote>
        The <code>git diff [file]</code> command is used to show changes in a Git repository. This command is useful for comparing differences between commits, 
        branches, or file versions. Here are the basic usages and examples of the <code>git diff</code> command:
      </blockquote>
      <li><h4>Showing Differences Between the Working Directory and the Staging Area:</h4></li>
<pre><code>git diff</code></pre>
      <small>This command shows changes that have not yet been added to the Staging Area.</small>
      <li><h4>Showing Differences Between the Staging Area and the Last Commit:</h4></li>
<pre><code>git diff --cached</code></pre>
    <small>This command compares the changes in the Staging Area with the last commit.</small>
    <li><h4>Showing Differences Between Two Specific Commits:</h4></li>
<pre><code># git diff commit_id1 commit_id2
git diff abc def</code></pre>
    <small>This command shows the differences between <code>abc</code> and <code>def</code> commits</small>
      <li><h4>Showing Changes in a Specific File:</h4></li>
<pre><code># git diff file_name
git diff app.js</code></pre>
    <small>This command shows changes in the app.js file.</small>
    <li><h4>Showing Differences Between a Specific Commit and the Current State:</h4></li>
<pre><code># git diff commit_id
git dif abc</code></pre>
    <small>This command shows the differences between the <code>abc</code> commit and the current status.</small>
    <li><h4>Showing Differences Between a Different Branch and the Current State:</h4></li>
<pre><code># git diff other_branch_name
git dif feature-branch</code></pre>
    <small>This command shows the differences between the feature-branch branch and the current state.</small>
   </ol>
</details>

<details>
  <summary><code id="git_checkout">git checkout -- [file]</code></summary>
    <ol>
      <blockquote>
        The <code>git checkout</code> command is used to switch between branches, view commits, create new branches, and revert files in the working 
        directory within a Git repository. However, starting from Git 2.23, the <code>git switch</code> and <code>git restore</code> commands have taken over some 
        of the responsibilities of <code>git checkout</code>. Here are the basic uses of the <code>git checkout</code> command:
      </blockquote>
      <li><h4>Changing Branch:</h4></li>
<pre><code># git checkout branch_name
git checkout main</code></pre>
      <small>This command switches to the <code>main</code> branch.</small>
      <li><h4>Creating a New Branch and Changing:</h4></li>
<pre><code># git checkout -b new_branch_name
git checkout -b feature-xyz</code></pre>
    <small>This command creates a new branch named <code>feature-xyz</code> and automatically switches to this branch.</small>
    <li><h4>Reverting Files to a Specific Commit or Branch State:</h4></li>
<pre><code># git checkout -- file_name
git checkout -- index.html</code></pre>
    <small>This command rolls the <code>index.html</code> file back to its last commit state.</small>
    <li><h4>Going to a Specific Commit:</h4></li>
<pre><code># git checkout commit_id
git checkout abc123</code></pre>
    <small>This command is used to go to the <code>abc123</code> commit id.</small>
    <li><h4>Viewing the State of a Specific Commit on a Specific Branch:</h4></li>
<pre><code># git checkout branch_name -- file_name
git checkout main -- index.html</code></pre>
    <small>This command puts the <code>index.html</code> file of the <code>main</code> branch into a specific commit state.</small>
   </ol>
</details>

<details>
  <summary><code id="git_switch">git switch</code></summary>
    <ol>
      <blockquote>
        The <code>git switch</code> command, introduced in Git version 2.23, is designed for switching between branches. This command allows you to 
        move from the current branch to another branch. It replaces the <code>git checkout</code> command for branch switching, providing a safer and 
        more explicit tool. Here are the basic usages and examples of the <code>git switch</code> command:
      </blockquote>
      <li><h4>Switching to Branch:</h4></li>
<pre><code># git switch branch_name
git switch feature-branch</code></pre>
      <small>This command switches to the branch named <code>feature-branch</code>.</small>
      <li><h4>Creating and Switching to a Branch:</h4></li>
<pre><code># git switch -c new_branch_name
git switch -c new-feature</code></pre>
    <small>This command creates a new branch named <code>new-feature</code> and switches to this branch.</small>
    <li><h4>Match and Switch to a Remote Branch with the Current Branch:</h4></li>
<pre><code># git switch --track remote_repo_name/remote_branch_name
git switch --track origin/main</code></pre>
    <small>This command matches the current branch with a branch in the remote repository and switches to this branch.</small>
    <li><h4>Saving Changes Before Switching Branches:</h4></li>
<pre><code># git switch -c new_branch_name --discard-changes
git switch -c new-feature --discard-changes</code></pre>
    <small>This command creates a new branch named <code>new-feature</code>, but does not save changes to the existing branch.</small>
   </ol>
</details>
