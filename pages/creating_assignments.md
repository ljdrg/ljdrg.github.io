---
layout: default
title: Creating Assignments
permalink: /creating_assignments.html
---

When creating an assignment you have various options to choose from. You can set a deadline, specify wether it's supposed to be an individual or group assignment, set the repository visibility to private or public...

For more detailed information go to this website: [Creating assignments](https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/create-an-individual-assignment)

If you want to use autograding make sure that you follow all of the steps in: [How to set up autograding](/autograding.html)

## Generally Recommended Settings

* Set the repository visibility to private. That way students only have access to their own repositories.
* Don't grant students admin access to their repository. They usually won't need that kind of rights so it's better not to enable it to avoid unwanted changes in the repositories.
* Select a template repository. Otherwise you have to push the course content separately to each student assignments. Although possible, using template repositories means a lot less effort.
* Add VScode as supported editor. This is especially helpful if your students have little coding experience or no prior knowledge of Git.
* Enable the “feedback pull request” option. This will automatically open a pull request when the student accepts an assignment and allows you to give direct feedback, line by line, on the students code.

## VScode as Preconfigured IDE for Assignments

When you chose VScode as integrated IDE the assignments will contain an "Open in VScode" badge. This badge handles installing VS Code, the Classroom extension pack, and opening to the active assignment with one click. Git is not automatically installed, students have to do that themselves.

VScode is the easiest way to interact with GitHub Classroom as it handles pulling and pushing with the use of buttons instead of having to use a terminal or command prompt. For more details see: [GitHub Classroom with VScode](https://docs.github.com/en/education/manage-coursework-with-github-classroom/integrate-github-classroom-with-an-ide/about-using-visual-studio-code-with-github-classroom)
