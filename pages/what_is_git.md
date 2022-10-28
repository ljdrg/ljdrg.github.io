---
layout: default
title: What is Git?
permalink: /what_is_git.html
---

## Version control system

Git is an open-source version control system which helps you keep your work well-structured and safe. It notices conflicts between changes made by different people and synchronizes files between different computers.  It allows you to revert selected files back to a previous state, revert the entire project back to a previous state, compare changes over time, see who last modified something that might be causing a problem, who introduced an issue and when, and more. Using a VCS also generally means that if you screw things up or lose files, you can easily recover.

You can either use Git by typing commands in the terminal or you can use a graphical user interface (GUI) such as Sourcetree or GitKraken.

If you choose the terminal, you will have to look up which Git commands you will need.
If you choose to use a GUI, then the various actions you need to take will be displayed in a more visual manner.

For the rest of this documentation, we will share examples using Git in the terminal.

Git commands follow the style of `git [...]`. The most common git commands you will need are: `git status`, `git add`, `git commit -m"..."`, `git push`, `git pull`, `git status`.

To turn an existing project into a Git repository you have to set this project as your working directory and enter the command `git init` in the terminal. Now there should be a new hidden folder '.git' in your directory. You can test this with entering `ls -a` in your terminal.

## Repositories

Git works with repositories. A repository consists of two parts: (1) your project, meaning your files and directories that you create and edit directly; and (2) the extra information that Git records about the project’s history.

The repository is the '.git' folder inside our project folder. It will track all the changes made to the files in our project and record that history over time.

If another developer wants to collaborate with us on our project then they can clone (or in other words download) the remote repository from the hosting service (GitHub) you uploaded it to their computer. This allows them to have the project on their computer as well. The project on their computer is then also referred to as a local repository. In a project with multiple developers, each one has a local repository on their computer. And there is one remote repository that they all contribute to and they use it to share their work.

With GitHub Classroom each of your students will get their own repository without affecting the repositories of other students.

In order to save different versions of our project in Git we will make commits. A commit is a version of your project. It represents a standalone version of your project and has a reference to all the files and folders that are a part of that version.

In order to understand how we make a commit we need to learn about two spaces inside Git — the staging area, and commit history.

The staging area and commit history are part of our repository.

The staging area is sort of like a rough draft space. It is where we can add updated versions of files or remove files in order to choose what we want to include in our next commit (version of our project). In the '.git' folder the staging area is represented by a file called index.

And finally the commit history is basically where our commits live after they’ve been made. In the '.git' folder the commit history is represented by a folder called objects.

## Template Repositories

You can make an existing repository a template, so you and others can generate new repositories with the same directory structure, branches, and files. Template repositories are an easy way to reuse your course material for another semester. 
For more information on GitHub Template Repositories and how to create one see: [Template Repositories](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-template-repository).

> Is this the student-specific part? Because this is quite specific functionality (for GitHub Classroom for example) and not that commonly used. 
> I found it worth mentioning as when setting up your classroom, template repositories are very helpful. So it's not aimed towards the students but for lecturers on how to set up their classrooms. But if you think it's not necessary to mention I'll delete it. 

## GitHub

[GitHub](https://www.github.com/) is a cloud-based hosting service for Git repositories. There are also other hosting services such as GitLab and Bitbucket. 

Anyone can sign up and create a GitHub account for free. You can create private and public repositories, create organizations or become a member in one. When we push (in other words upload) our local repository to one of these services, then the repository that resides in these service in the cloud is referred to as the remote repository.

## GitHub organization

A GitHub organization is an umbrella account on GitHub where you can store all your repositories. The organization you choose for your classroom is the place where all of your student’s assignment repositories will live. Each student will have their own assignment repository. You can learn more about GitHub organizations [here](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/about-organizations).

