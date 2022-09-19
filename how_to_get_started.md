---
layout: default
title: How to get started
link: /how_to_get_started.html
---

## VSCode-based git operations

### How to get started

The first thing you have to do is to install [git](https://git-scm.com/download). 

Then, if you don’t have one already, create a GitHub account. Simply go to the [GitHub website](https://github.com/) and click on “Sign up for GitHub”. For a more detailed explanation have a look at the [GitHub documentation](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account). 

Now that you have your own account, click on the invitation link for the GitHub classroom assignment made available by your teacher and accept the invitation. The link looks something like this: [https://classroom.github.com/a/CfsmLMjf](https://classroom.github.com/a/CfsmLMjf)

![accepting.PNG](../assets/images/img-github-classroom.webp)

You will get redirected to GitHub Classroom and will see this screen:

![accepted.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6d776b00-c999-459f-b489-0e16f34a171f/accepted.png)

Refresh the page.. and there we go:

![accept.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e2ace1f2-1874-4009-b99b-299a3802421a/accept.png)

Now you can either click on the URL to get to your assignment on GitHub. Or you click on the “Open in Visual Studio Code” button. This will open your assignment on your computer in VSCode.  

The first time you click on the VSCode button of the GitHub Assignment, VSCode is going to be installed on your computer in case it isn’t already. If a warning message like this one:

![warning.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9d730f7e-b895-4dfd-9d7b-799085b1d528/warning.png)

pops up, you can safely ignore it and click on open. You also want to install the [GitHub Pull Requests and Issues extension](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github) for VSCode. If VScode doesn’t directly ask if you want to install the extension, go to the link and install it manually. Go to the GitHub section by clicking on the GitHub logo of the taskbar on the left. Click on sign in. 

![sign.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/88a7c282-32d3-437d-9328-88030e397cad/sign.png)

You will be asked to log in with your GitHub account. Then click on “Authorize Visual Studio Code”. 

![auth.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/55514b3f-e71d-465a-9a78-4092ba89ec68/auth.png)

After that VSCode will try to connect with your GitHub account. In the GitHub section now go to the “CLASSROOMS” list. Here you find another sign in button.

![calssroom.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/03387606-f267-4043-8fa7-8b52c49570bc/calssroom.png)

As you may have guessed, you should sign in there as well. If you signed in but you can’t find your GHCR assignment, close VSCode and reopen it with clicking on the VSCode button in GHCR. Chances are that VSCode just has to be reloaded. 

VSCode might ask you about a pull request:

![PR.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/caaca077-c258-4906-9620-23be980b8ba4/PR.png)

choose the “Ignore Pull Request” option.

Now that you’re all set with VSCode you can start with your actual assignment. And don’t worry, the next time you’re opening an assignment with the VSCode button, you don’t have to go through all this steps again. VScode will directly open in the directory of your assignment and your good to go.

## How to submit your work

If you are done with the exercises and want to submit or “push” your answers to GitHub you can do so by using the VScode interface. First, make sure you saved the changes in your files (you can use CTRL + s to do so). In the taskbar on the left are various buttons. One is called “source control”, click on it. 

![vscode_git_sourcecontrol.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b5088d73-f4c1-40e4-b477-58a2fa40d568/vscode_git_sourcecontrol.png)

Then enter a commit message in the field over the “commit” button. The message should contain a short description of what you have changed in the files, e.g. “solved exercise 1”.

You have three options when you use the commit button. If you just click on the commit button without choosing one of the other two options. Your changes in the files are going to be commited but not yet pushed to your git repository. So if you actually want to see the changes in your files in your git repository you have to choose the option “Commit & Push”. The third option “Commit & Sync” first pulls any changes of your git repository to your cloned local repository and then commits and pushes changes that you have made to the git repository.

## How to find your GHCR assignment without the invitation link

You can find your GHCR assignment when signing in to your account and going to the GitHub organization of your GHCR assignment. There you will find a list of repositories, the one with your GitHub account name at the end is yours. To not always have to go to the organization first to get to your assignment, you can mark your assignment/ repository with a star. Then when clicking on your profile logo you can directly go to your starred repositories and find it there.

# Terminal-based git operations

VSCode is a nice way to use git without having to know too much about git commands themselves. For anyone interested in how git works with terminal-based commands, this section is for you!

It’s easiest to interact with git via “Bash” the Linux terminal. For windows users there is a Windows Subsystem for Linux (WSL) with which you can install a Linux distribution, e.g. Ubuntu. The WSL enables you to use Linunx tools like Bash. For details on how to install Linux on Windows see the [Windows documentation](https://docs.microsoft.com/en-us/windows/wsl/install).

You can use bash via VSCode. In VSCode go on the “terminal” tab and click on the arrow next to the plus sign. A list of various terminals will open, select “Git Bash”.

![terminal.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7d1fb4f7-51ff-4899-ac30-920ce8515e5b/terminal.png)

Great! Now we can start with the actual git commands.

You want to start with cloning your GitHub repository to your computer. Cloning means nothing else then creating a copy of that repository. To do so you need to have the repository’s URL or SSH key (to use the SSH option you first have to set up a SSH key for your GitHub account). You find these options when clicking on the “Code” button in your GitHub repository. 

![code.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6411c560-a8b4-4060-9395-ebdbd7817ad0/code.png)

The git command for cloning is: `git clone URL` (for “URL” enter the copied HTTPS link from your GH repository.)

The repository is being cloned into your current working directory when entering the git command. So make sure you’re in the desired directory when cloning your repository.

After you have worked on your assignment you want to “push” your changes made to the GH repository. For that you have to enter three git commands: `git add`, `git commit` and `git push` . Here is why: Git has a “staging area” ****in which it stores files with changes you want to save that haven't been saved yet. Putting files in the staging area is like putting things in a box, while “committing” those changes is like putting that box in the mail: you can add more things to the box or take things out as often as you want, but once you put it in the mail, you can't make further changes. You commit changes to a git repository in two steps: (1) add one or more files to the staging area, (2) commit everything in the staging area.

Git command to add a single file: `git add filename` (replace “filename” with the acual name of the file + extension(“.txt”, “.py”, …)

Git command to add all files that have been changed: `git add .` 

To save the changes in the staging area, you use the command `git commit` . It saves everything that is in the staging area as one unit. When you commit changes, git requires you to enter a log message. This serves the same purpose as a comment in a program: it tells the next person to examine the repository why you made a change. By default, Git launches a text editor to let you write this message. To write a short single line message you can use the command:

`git commit -m “short message”` 

If you run `git commit` on it’s own a text editor will open in a new tab in VSCode. You enter your commit message, save it and close the tab by clicking on “x”.

Now that you have staged and committed the changes. You can “push” them to your git repository. 

The git command is: `git push remote-name branch-name` (the “remote-name” is usually “origin” and the “branch-name” is usually “main”) do the command would look like: `git push origin main`

It pushes the changes you made on your current branch (main) to the remote GitHub repository (origin). Note: as you cloned your repository, the remote “origin” was automatically added so git knows where to push to. If you would have created a new git repository without cloning, you would have to set up the remote yourself.

To get an overview on what’s going on in your repository you can use the `git status` command. It will show you which files have been changed but are not yet staged; which files are staged but have not yet been committed; and if you added new files also if a file is not yet tracked by git and has to be added to the staging area.

Suppose something has changed in your GitHub repository and you want to get those changes to your local repository. So instead of “pushing” to the GitHub repository you want to “pull” from it. The git command is: `git pull remote-name branch-name` This command gets everything in branch in the remote repository you’re pulling from and merges it into the current branch of your local repository. E.g. if the remote-name is “origin” and you want to get changes from the branch “main” of the remote repository, the command would be: `git pull origin main`