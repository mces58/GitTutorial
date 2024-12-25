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

<details>
  <summary><code id="git_commit">git commit</code></summary>
    <ol>
      <blockquote>
        The <code>git commit</code> command is used to permanently save changes in your working directory. Here are the basic uses and some examples 
        of the <code>git commit</code> command:
      </blockquote>
      <li><h4>Basic Commit Process:</h4></li>
<pre><code># git commit -m "Commit Description"
git commit -m "Update homepage design"</code></pre>
      <small>The <code>git commit</code> command allows you to permanently save changes that are staged (in the Staging Area).</small>
      <small>When used with the <code>-m</code> parameter, you can add a commit message. The message is important for describing the changes you have made.</small>
      <li><h4>Committing All Files in the Staging Area:</h4></li>
<pre><code>git commit -a -m "Update all files"</code></pre>
    <small>If you want to commit all changes in the Staging Area, you can use the <code>-a</code> (all) parameter. This commits all changes 
    to tracked files without needing to explicitly stage them.</small>
    <small>However, be cautious when using this method, as it does not include untracked new files in the commit.</small>
    <li><h4>Editing Changes:</h4></li>
<pre><code>git commit --amend -m "fix: Commit Description"</code></pre>
    <small>If you notice an error in your last commit or need to change the commit message, you can use the <code>--amend</code> parameter.</small>
    <small>This command updates your most recent commit.</small>
   </ol>
</details>

<details>
  <summary><code id="git_rm">git rm [file]</code></summary>
    <ol>
      <blockquote>
        The <code>git rm</code> command removes a file or directory from version control in a repository. The removed file or directory will 
        no longer be tracked, and this change will take effect in the next commit. However, the file or directory is not physically deleted; it is only untracked.
      </blockquote>
      <li><h4>Stop Tracking the File:</h4></li>
<pre><code># git rm file_name
git rm myFile.txt</code></pre>
      <small>This command stops tracking the <code>myfile.txt</code> file, and the change will take effect in the next commit.</small>
      <li><h4>Stop Tracking and Remove the File:</h4></li>
<pre><code># git rm -f file_name
git rm -f myFile.txt</code></pre>
    <small>This command both stops tracking the <code>myfile.txt</code> file and physically deletes it. The <code>-f</code> option forces the 
    deletion, even if the file has been modified.</small>
  </ol>
</details>

---

<h3><ins>04 Storing Your Work</ins></h3>

<details>
  <summary><code id="git_stash">git stash</code></summary>
    <ol>
      <blockquote>
        The <code>git stash</code> command is used to temporarily save changes in the current branch. This is useful when you want to save your 
        work without committing it, allowing you to switch branches or work on something else without losing progress. 
        Here are the basics of <code>git stash</code> usage and examples:
      </blockquote>
      <li><h4>Saving Changes:</h4></li>
<pre><code>git stash</code></pre>
      <small><code>git stash</code> saves all changes in the working directory to a temporary storage location called a stash. 
      This allows you to return your current branch to a clean state while keeping your changes safe for later use.</small>
      <li><h4>Viewing the Stash List:</h4></li>
<pre><code>git stash list</code></pre>
    <small>This command displays the stash list and shows each stash named with an index number.</small>
    <li><h4>Applying a Specific Stash:</h4></li>
<pre><code># git stash apply stash_index_number
git stash apply 0</code></pre>
    <small>This applies the first stash in the stash list. The <code>apply</code> command applies the stash but does not delete it. 
    If you want to apply and delete the stash simultaneously, you can use <code>git stash pop</code>.</small>
    <li><h4>Applies and deletes the stash:</h4></li>
<pre><code># git stash pop stash_index_number
git stash pop 0</code></pre>
    <small>This command applies the first stash from the stash list and deletes it.</small>
    <li><h4>Inspecting a Specific Stash:</h4></li>
<pre><code># git stash show stash_index_number
git stash show 0</code></pre>
    <small>This command shows the changes of the first stash in the stash list.</small>
    <li><h4>Deleting All Stashes:</h4></li>
<pre><code>git stash clear</code></pre>
    <small>This command completely clears the stash list.</small>
  </ol>
</details>

---

<h3><ins>05 Git Branching Model</ins></h3>

<details>
  <summary><code id="git_branch">git branch</code></summary>
    <ol>
      <blockquote>
        The <code>git branch</code> command is used to list branches, create new branches, switch between branches, and delete branches in a Git repository. 
        Here are the basic usages and some examples of the <code>git branch</code> command:
      </blockquote>
      <li><h4>Listing Branches:</h4></li>
<pre><code>git branch</code></pre>
      <small>This command lists the current branches and shows which branch you are on. The active branch is indicated with an asterisk (*) symbol.</small>
      <li><h4>Creating a New Branch:</h4></li>
<pre><code># git branch new_branch_name
git branch feature-xyz</code></pre>
    <small>This command creates a new branch named <code>feature-xyz</code> but does not automatically switch to it. You continue working on the current branch.</small>
    <li><h4>Change Branch (Checkout):</h4></li>
<pre><code># git checkout target_branch_name
git checkout feature-xyz
<br />
# Alternatively, in Git 2.23 and later
# The following command can also be used:
# git switch target_branch_name
git switch feature-xyz</code></pre>
    <small><code>git checkout</code> and <code>git switch</code> commands allow you to leave the current branch and switch to another branch.</small>
    <li><h4>Creating a New Branch and Switching:</h4></li>
<pre><code># git checkout -b new_branch_name
git checkout -b feature-abc</code></pre>
    <small>This command creates a new branch named <code>feature-abc</code> and automatically switches to that branch.</small>
    <li><h4>Deleting Branch:</h4></li>
<pre><code># git branch -d branch_name_to_delete
git branch -d feature-xyz</code></pre>
    <small>This command deletes the branch named <code>feature-xyz</code>. However, if there are unmerged changes in this branch, the deletion 
    will not proceed. You can forcefully delete the branch using <code>git branch -D</code>, but you should be cautious in this case.</small>
  </ol>
</details>

<details>
  <summary><code id="git_merge">git merge</code></summary>
    <ol>
      <blockquote>
        <code>git merge</code> command is used to combine different branches. It is typically used when you want to add changes made on a feature branch 
        to the <code>master</code> branch or merge changes from different branches. Here is the basic usage of the <code>git merge</code> command along with examples:
      </blockquote>
      <li><h4>Merging a Specific Branch into the Current Branch:</h4></li>
<pre><code>git checkout master # switch to the branch to be merged
git merge feature-xyz # merge feature-xyz branch into master branch
<br />
# or use with switch command
git switch master
git merge feature-xyz</code></pre>
      <small>These commands merge the <code>feature-xyz</code> branch into the current branch.</small>
      <li><h4>Fast Forward Merge:</h4></li>
      <p>If the changes on a branch were made after the latest commit on the target branch (the branch to be merged), Git performs a 
      'Fast Forward' merge. In this case, no separate commit is created.</p>
<pre><code>git checkout master
git merge feature-xyz</code></pre>
    <small>This command merges the <code>master</code> branch into the <code>feature-xyz</code> branch. If a Fast Forward merge occurs, you will see that the <code>master</code> 
    branch now points to the same commit as the <code>feature-xyz</code> branch's latest commit.</small>
    <li><h4>Non-Fast Forward Merge:</h4></li>
    <p>If there are changes made between the branch being merged and the target branch, and Fast Forward merge is not possible, 
    Git will create a new commit to complete the merge.</p>
<pre><code>git checkout master
git merge --no-ff feature-xyz</code></pre>
    <small>The <code>--no-ff</code> parameter forces a non-fast-forward merge, creating a new commit even if a fast-forward merge is possible.</small>
    <li><h4>Handling Conflicting Changes:</h4></li>
    <p>If there are conflicting changes during the merge process, Git will not be able to complete the merge automatically. In this case, manual intervention may be required.</p>
<pre><code>git checkout master
git merge feature-xyz</code></pre>
    <small>If there are conflicts, Git will show you the conflicting files and ask you to resolve the conflicts by editing them. 
    After resolving the conflicts, you can mark the files as resolved and proceed with the commit.</small>
    <li><h4>Merge with a Specific Commit:</h4></li>
<pre><code># git merge commit_id
git merge abc123</code></pre>
    <small>This merges the current branch with a specific commit.</small>
  </ol>
</details>

---

<h3><ins>06 Inspect History</ins></h3>

<details>
  <summary><code id="git_log">git log</code></summary>
    <ol>
      <blockquote>
        <code>git log</code> command is used to view the commit history of a Git repository. This command provides a list containing details such as commit 
        IDs, authors, dates, and commit messages. Here are the basic usages and some examples of the <code>git log</code> command:
      </blockquote>
      <li><h4>Basic Usage:</h4></li>
<pre><code>git log</code></pre>
      <small>This command displays a series of information for each commit. Each commit's unique identifier (hash), author, date, and commit message are listed.</small>
      <li><h4>Shortening Commit Information:</h4></li>
<pre><code>git log --oneline</code></pre>
    <small>This command displays only a shortened commit ID and the commit message for each commit.</small>
    <li><h4>Graphical Representation:</h4></li>
<pre><code>git log --oneline --graph</code></pre>
    <small>This displays commits in a graphical format, showing branches and merges.</small>
    <li><h4>Displaying Commit History for a Specific Directory or File:</h4></li>
<pre><code># git log file_name
git log index.html</code></pre>
    <small>This command displays the commit history exclusively for the <code>index.html</code> file.</small>
    <li><h4>Displaying Commits Up to a Specific Date:</h4></li>
<pre><code>git log --until=2025-01-01</code></pre>
    <small>This command lists the commits up to the specified date.</small>
    <li><h4>Displaying the commits made by a specific author:</h4></li>
<pre><code># git log --author="author_name"
git log --author="mces58"</code></pre>
  </ol>
</details>

<details>
  <summary><code id="git_show">git show</code></summary>
    <ol>
      <blockquote>
        <code>git show</code> command provides detailed information about a specific commit, branch, or tag in Git. This command displays the changes 
        made in a commit, the commit message, and details about modified files. Below are the basic uses and examples of the <code>git show</code> command:
      </blockquote>
      <li><h4>Displaying a Specific Commit:</h4></li>
<pre><code># git show commit_id
git show abc123</code></pre>
      <small>This command displays detailed information about the commit with the ID <code>abc123</code>, including the changes, commit message, and other details.</small>
      <li><h4>Display the Last Commit:</h4></li>
<pre><code>git show</code></pre>
    <small>This command displays the details of the most recent commit. If you are working on HEAD, it shows the latest commit.</small>
    <li><h4>Showing a Specific Branch or Tag:</h4></li>
<pre><code># git show branch_name
git show main
# git show v1.0.0</code></pre>
    <small>This command shows the details of the latest commit on the main branch. It can also be used for tags.</small>
    <li><h4>Show changes for a specific file:</h4></li>
<pre><code># git show commit_id file_name
git show abc123 index.html</code></pre>
    <small>This command shows the changes made to the <code>index.html</code> file in a specific commit.</small>
    <li><h4>Show changes in color:</h4></li>
<pre><code>git show --color commit_id</code></pre>
    <small>This command displays the changes in color, making it easier to read.</small>
    <li><h4>Line-by-Line Comparison of Changes:</h4></li>
<pre><code>git show -v commit_id</code></pre>
    <small>This command shows the changes in a specific commit, comparing them line by line.</small>
  </ol>
</details>

---

<h3><ins>07 Tagging Commits</ins></h3>

<details>
  <summary><code id="git_tag">git tag</code></summary>
    <ol>
      <blockquote>
        The <code>git tag</code> command is used to add a tag to a specific commit or manage existing tags in a Git repository. Tags typically represent 
        the name, version number, or description of a specific release or significant point in the repository's history. Here are the basic 
        uses of the <code>git tag</code> command with examples:
      </blockquote>
      <li><h4>Creating a Tag:</h4></li>
<pre><code># git tag tag_name
git tag v1.0.0</code></pre>
      <small>This command adds a tag named <code>v1.0.0</code> to the current HEAD commit.</small>
      <li><h4>Adding a Tag to a Specific Commit:</h4></li>
<pre><code># git tag tag_name commit_id
git tag v1.0.0 abc123</code></pre>
    <small>This command adds a tag named <code>v1.0.0</code> to a specific commit (here represented as <code>abc123</code>).</small>
    <li><h4>Creating Annotated Tags:</h4></li>
<pre><code># git tag -a tag_name -m "Tag Description"
git tag -a v1.0.0 -m "Stable version"</code></pre>
    <small>This command creates a tag named <code>v1.0.0</code> with a description.</small>
    <li><h4>Listing Tags:</h4></li>
<pre><code>git tag</code></pre>
    <small>This command lists available tags.</small>
    <li><h4>Showing a Specific Label Version:</h4></li>
<pre><code># git show tag_name
git show v1.0.0</code></pre>
    <small>This command shows the details of the tag named <code>v1.0.0</code>.</small>
    <li><h4>Deleting a Specific Tag:</h4></li>
<pre><code># git tag -d tag_name
git tag -d v1.0.0</code></pre>
    <small>This command deletes the tag named <code>v1.0.0</code> locally.</small>
    <li><h4>Push Tag to Remote Repository:</h4></li>
<pre><code># git push remote_repo tag_name
git push origin v1.0.0</code></pre>
    <small>This command pushes a specific tag to the remote repository.</small>
    <li><h4>Push All Tags to Remote Repository:</h4></li>
<pre><code># git push remote_repo --tags
git git push origin --tags</code></pre>
    <small>This command sends all tags to the remote repository.</small>
  </ol>
</details>

---

<h3><ins>08 Reverting Changes</ins></h3>

<details>
  <summary><code id="git_reset">git reset [&lt;path&gt;...]</code></summary>
    <ol>
      <blockquote>
        The <code>git reset</code> command is used to modify the commit history of a branch and revert files in the working directory. 
        This command should be used carefully, as it changes history and is generally not recommended on shared branches. 
        Here are the basic uses and examples of the <code>git reset</code> command:
      </blockquote>
      <li><h4>Reverting Commits:</h4></li>
<pre><code># git reset commit_id
git reset abc123</code></pre>
      <small>This command reverts commits up to the <code>abc123</code> commit ID. By default, <code>git reset</code> performs a 'soft reset,' meaning it 
      reverts commits without modifying files in the working directory.</small>
      <li><h4>Reverting Files:</h4></li>
<pre><code># git reset --hard commit_id
git reset --hard abc123</code></pre>
    <small>This command reverts commits up to the specified commit and also modifies the files in the working directory. 
    This operation is irreversible, so it should be used with caution.</small>
    <li><h4>Reverting Commits with a Soft Reset:</h4></li>
<pre><code># git reset --soft commit_id
git reset --soft abc123</code></pre>
    <small>This command reverts commits without altering the files in the working directory. It's useful when you want to undo commits but retain the changes in your files.</small>
    <li><h4>Mixed Reset to Revert Commits and Staging Area (Default):</h4></li>
<pre><code># git reset --mixed commit_id
git reset abc123</code></pre>
    <small>This command reverts the commits and modifies the files but clears the Staging Area.</small>
    <li><h4>Reverting to the Previous Commit:</h4></li>
<pre><code>git reset --hard HEAD^</code></pre>
    <small>This command reverts to the previous commit.</small>
  </ol>
</details>
