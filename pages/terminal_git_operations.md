---
layout: default
title: Terminal-based Git operations
permalink: /terminal_git_operations.html
---
## Installing Bash

It’s easiest to interact with Git via `Bash`; the Unix command processor. For Windows users there is a Windows Subsystem for Linux (WSL) with which you can install a Linux distribution (e.g., Ubuntu). WSL enables you to use the Linux Operating System of your choice via the command line. For details on how to install Linux on Windows see the [Windows documentation](https://docs.microsoft.com/en-us/windows/wsl/install).

You can use Git directly via your terminal (Bash, Powershell), or an IDE. For example, in [VSCode](https://code.visualstudio.com/Download):

- Navigate to the “terminal” tab (see below),
- click on the arrow next to the plus sign.

A list of various terminals will open, select “Git Bash”.

![terminal.PNG](..\assets\images\terminal.PNG)

> This needs some description of how to set git up in VSCode via a plug-in rather than terminal too.

## Installing Git

If you want to install Git separate from your IDE, go to this website [Git download](https://git-scm.com/downloads) and choose the correct version for your operating system (Linux/Unix if you are using WSL). After the download is completed, open the file and follow the instructions. For a detailed guide on the settings see: [Git installation guide](https://www.geeksforgeeks.org/how-to-install-git-on-windows-command-line/). 

Great! Now we can start with the actual Git commands.

## Git commands

When working with `git`, there are a few operations we would want to do:

- `clone`: Fetch code from a repository (or, not discussed here: mark a directory that git should use as a working directory). These are local files.
- `add`: Add any files that git should be tracking new changes for.
- Edit the files.
- `commit`: Confirm these are the changes we want to be a particular version.
- `push`: Sync local changes with a remote repository (e.g., one on GitHub).
- `pull` : After a while, sync our local repository with changes made by someone else on a remote repository (this might produce conflicts).

These commands will be discussed below.

### git clone

Projects typically start with cloning a remote (GitHub) repository to your computer (you can also make one locally and sync it later, but this is easier). Cloning simply means creating a local copy of that repository with its version control history (this typically gives you the most recent version by default if it's an existing repository). To do so, you need to have the repository’s URL or SSH key (to use the SSH option you first have to set up an SSH key for your GitHub account). You find these options when clicking on the “Code” button in your GitHub repository.

<img src="assets\images\code.PNG" width= 400px>

> We should add info on how to do SSH authentication, because password access is deprecated.

The git command for cloning is: `git clone [URL here]` (replace “[URL here]” with the copied HTTPS link from your GitHub repository), e.g. `git clone https://github.com/tcsai/tcsai.github.io`.

The repository will be cloned into your current working directory when entering the git command. So make sure you’re in the desired directory when cloning your repository.

### git add

Apart from the files that were already in the repository, you might have new files that git doesn't know about. The files being in the directory is not enough! You have to actively tell git to track them. You can do this with `git add`:

- Git command to add a single file: `git add filename` (replace “filename” with the actual name of the file + extension(“.txt”, “.py”, …)
- Git command to add all files that have been changed: `git add .` 

### Make some changes

Git is a versioning system. Your empty repository (usually only has a README, or a few pre-prepared files) is a version. These versions are identified by a unique hash (a serial number). These are typically long (e.g., `4534b009d84a7b3b01782a87ea4680520a5f617c`) but are often abbreviated (here: `4534b00`, the probability of two versions *in the same repository* having the same shortened hash is almost zero). To confirm that a set of changes you made are a version, you '`commit`' to those changes. After you issue this command, Git checks what the differences are between this `commit`, and the previous one (which will typically between a set of insertions and/or deletions). Through this, git can track the history of the project and show you versions at particular times. It is generally good practice to commit often; commits should reflect one particular (working) change or task you completed. Implementing multiple things and then versioning that under one commit makes it less clear to anyone reading the version history.

### git commit

So, when you commit changes, Git requires you to enter a log message. This serves the same purpose as a comment in a program: it tells the next person to examine the repository why you made a change. By default, Git launches a text editor to let you write this message. To write a short single line message you can use the command:

`git commit -m “short message”` 

If you run `git commit` on it’s own a text editor will open. Enter your commit message and then close the text editor.

Committed the changes. You can “push” (i.e., sync) them to your git repository.

### git push

After you have made, and `commit`ed some local changes in your cloned repository (local here meaning on your system, which is now different from the version on GitHub) you want to “push” your changes to the GitHub repository (or elsewhere, if relevant). The git command is: `git push`. If you want to be more specific, you can add `git push remote-name branch-name` (the “remote-name” is usually “origin” and the “branch-name” is usually “main”) so the command would look like this: `git push origin main`. 

It pushes the changes you made on your current branch (main) to the remote GitHub repository (origin). Note: as you cloned your repository, the remote “origin” was automatically added so git knows where to push to. If you would have created a new git repository without cloning, you would have to set up the remote yourself. We won't discuss branches, pull requests, and other more advanced git operations here.

### git pull

Suppose something has changed in your GitHub repository and you want to get those changes to your local repository. Instead of “pushing” to the GitHub repository, you want to “pull” from it. The git command is: `git pull`, or alternatively: `git pull remote-name branch-name` (see `push` for explanation). This command syncs everything from the remote repository associated with the current project; i.e., it merges any changes into your local repository.

## Conflicts

> Need to add more here.

## More advanced operations

### git remote

If your current directory is a git repository you can list the remotes for this repository with `git remote`.

To add a new remote use the command `git remote add remote-name URL`. Replace "remote-name" with the name for the new remote and "URL" with the copied HTTPS link from your GitHub repository.

> Branching might be relevant to add.

### git status

To get an overview on what’s going on in your repository you can use the `git status` command. It will show you which files have been changed but are not yet staged; which files are staged but have not yet been committed; and if you added new files also if a file is not yet tracked by Git and has to be added to the staging area.

## Further Resources

You can find a cheat sheet for Git commands here: [Git Commands](https://education.github.com/git-cheat-sheet-education.pdf)

Crash Course Git & GitHub:
{% include youtube.html id="RGOj5yH7evk" %}

