---
layout: default
title: How your students submit their assignments
permalink: /submit_assignments.html
---

After finishing the creation of an assignment, you have to share the invitation link of the assignment with your students. Simply copy the URL and provide it to your students via the Canvas page. After students have accepted the invitation to the classroom via mail, they can then directly accept the GitHub assignment through Canvas. 

Your students then have to clone the repository before they can start working on it. Once they are done they have to add, commit and push their assignments to the GitHub Classroom assignment repository. If you want the students to submit the assignment via Canvas, set the submission type for the Canvas assignment to "website". This way, students can enter the URL of their G itHub repository and submit their work in Canvas. Also, students do not have to resubmit their assignments in Canvas. When they submit the link to their repositories, any changes they make in their repositories will be submitted directly with them.

## Student workflow when using VScode as integrated IDE

Click on the invitation link for the GitHub classroom assignment made available by your teacher and accept the invitation. The link looks something like this: **[https://classroom.github.com/a/CfsmLMjf](https://classroom.github.com/a/CfsmLMjf)**

<!-- <img src="assets\images\accepting.PNG" width=400px center> -->

You will get redirected to GitHub Classroom and will see this screen:

<img src="assets\images\accepted.PNG" width=400px center>

Refresh the page.. and there we go:

<img src="assets\images\accept.PNG" width=400px center>

Now you can either click on the URL to get to your assignment on GitHub. Or you click on the “Open in Visual Studio Code” button. This will open your assignment on your computer in VSCode.  

The first time you click on the VSCode button of the GitHub Assignment, VSCode is going to be installed on your computer in case it isn’t already. If a warning message like this one:

<img src="assets\images\warning.PNG" width=400px center>

pops up, you can safely ignore it and click on open. You also want to install the [GitHub Pull Requests and Issues extension](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github) for VSCode. If VScode doesn’t directly ask if you want to install the extension, go to the link and install it manually. Go to the GitHub section by clicking on the GitHub logo of the taskbar on the left. Click on sign in. 

<img src="assets\images\sign.PNG" width=300px center>

You will be asked to log in with your GitHub account. Then click on “Authorize Visual Studio Code”. 

<!-- <img src="assets\images\auth.PNG" width=300px center> -->

After that VSCode will try to connect with your GitHub account. In the GitHub section now go to the “CLASSROOMS” list. Here you find another sign in button.

<img src="assets\images\calssroom.PNG" width=300px center>

As you may have guessed, you should sign in there as well. If you signed in but you can’t find your GHCR assignment, close VSCode and reopen it with clicking on the VSCode button in GHCR. Chances are that VSCode just has to be reloaded. 

VSCode might ask you about a pull request:
<img src="assets\images\PR.PNG" width=400px center>

choose the “Ignore Pull Request” option.

Now that you’re all set with VSCode you can start with your actual assignment. And don’t worry, the next time you’re opening an assignment with the VSCode button, you don’t have to go through all this steps again. VScode will directly open in the directory of your assignment and your good to go.

### How they submit the assignment

When they are done with the exercises and want to submit or “push” your answers to GitHub you can do so by using the VScode interface. First, make sure you saved the changes in your files (you can use CTRL + s to do so). In the taskbar on the left are various buttons. One is called “source control”, click on it. 

<img src="assets\images\vscode_git_sourcecontrol.PNG" width=300px center>


Then enter a commit message in the field over the “commit” button. The message should contain a short description of what you have changed in the files, e.g. “solved exercise 1”.

You have three options when you use the commit button. If you just click on the commit button without choosing one of the other two options. Your changes in the files are going to be commited but not yet pushed to your git repository. So if you actually want to see the changes in your files in your git repository you have to choose the option “Commit & Push”. The third option “Commit & Sync” first pulls any changes of your git repository to your cloned local repository and then commits and pushes changes that you have made to the git repository.