---
layout: default
title: Terminal-based Git operations
permalink: /terminal_git_operations.html
---
## Installing Bash

It’s easiest to interact with Git via “Bash” the Linux terminal. For windows users there is a Windows Subsystem for Linux (WSL) with which you can install a Linux distribution, e.g. Ubuntu. The WSL enables you to use Linunx tools like Bash. For details on how to install Linux on Windows see the [Windows documentation](https://docs.microsoft.com/en-us/windows/wsl/install).

You can use bash via VSCode. In VSCode go on the “terminal” tab and click on the arrow next to the plus sign. A list of various terminals will open, select “Git Bash”.

![terminal.PNG](..\assets\images\terminal.PNG)

Great! Now we can start with the actual git commands.

## Git commands

### git clone

You want to start with cloning your GitHub repository to your computer. Cloning means nothing else then creating a copy of that repository. To do so you need to have the repository’s URL or SSH key (to use the SSH option you first have to set up a SSH key for your GitHub account). You find these options when clicking on the “Code” button in your GitHub repository. 

![code.PNG](assets\images\code.PNG)

The git command for cloning is: `git clone URL` (for “URL” enter the copied HTTPS link from your GH repository.)

The repository is being cloned into your current working directory when entering the git command. So make sure you’re in the desired directory when cloning your repository.

### Push changes

After you have worked in your cloned repository you want to “push” your changes made to the GH repository. For that you have to enter three git commands: `git add`, `git commit` and `git push` 

Here is why: Git has a “staging area” in which it stores files with changes you want to save that haven't been saved yet. Putting files in the staging area is like putting things in a box, while “committing” those changes is like putting that box in the mail: you can add more things to the box or take things out as often as you want, but once you put it in the mail, you can't make further changes. You commit changes to a git repository in two steps: (1) add one or more files to the staging area, (2) commit everything in the staging area.

### git add

Git command to add a single file: `git add filename` (replace “filename” with the acual name of the file + extension(“.txt”, “.py”, …)

Git command to add all files that have been changed: `git add .` 

### git commit

To save the changes in the staging area, you use the command `git commit` . It saves everything that is in the staging area as one unit. When you commit changes, git requires you to enter a log message. This serves the same purpose as a comment in a program: it tells the next person to examine the repository why you made a change. By default, Git launches a text editor to let you write this message. To write a short single line message you can use the command:

`git commit -m “short message”` 

If you run `git commit` on it’s own a text editor will open in a new tab in VSCode. You enter your commit message, save it and close the tab by clicking on “x”.

Now that you have staged and committed the changes. You can “push” them to your git repository. 

### git push

The git command is: `git push remote-name branch-name` (the “remote-name” is usually “origin” and the “branch-name” is usually “main”) do the command would look like: `git push origin main`

It pushes the changes you made on your current branch (main) to the remote GitHub repository (origin). Note: as you cloned your repository, the remote “origin” was automatically added so git knows where to push to. If you would have created a new git repository without cloning, you would have to set up the remote yourself.

### git status

To get an overview on what’s going on in your repository you can use the `git status` command. It will show you which files have been changed but are not yet staged; which files are staged but have not yet been committed; and if you added new files also if a file is not yet tracked by git and has to be added to the staging area.

### git pull

Suppose something has changed in your GitHub repository and you want to get those changes to your local repository. So instead of “pushing” to the GitHub repository you want to “pull” from it. The git command is: `git pull remote-name branch-name` This command gets everything in branch in the remote repository you’re pulling from and merges it into the current branch of your local repository. E.g. if the remote-name is “origin” and you want to get changes from the branch “main” of the remote repository, the command would be: `git pull origin main`