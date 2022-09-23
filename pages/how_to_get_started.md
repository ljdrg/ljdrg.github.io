---
layout: default
title: How to get started with GitHub Classroom
permalink: /getting_started_with_GHCR.html
---

## Prerequisits

First of all, you need a GitHub account. If you don’t have one already just go on the website of [GitHub](https://github.com/) and sign up for one.

## First time creating a Classroom

Watch this video or read the text below:
{% include youtube.html id="xVVeqIDgCvM" %}

Go to [GitHub Classroom](https://classroom.github.com/) and sign in with you GitHub account. The first time using GitHub Classroom you have to authorize Classroom for your GitHub account, click “authorize GitHub”. 

Then you are asked to “create your first classroom”. You can then either create an organization or grant access to an existing organization 

The organization you choose for your classroom is the place where all of your student’s assignment repositories will live. Each student will have their own assignment repository where they will do their work.

### Creating a new organization

The organization you choose for your classroom is the place where all of your student’s assignment repositories will live. For every assignment you create in GitHub Classroom new repositories are added to this organization, one for every student accepting an assginment. So let’s say you have 5 students and 2 assignments in your GitHub classroom and all 5 students have accepted these two assignments. That means that in your GitHub organization you have 10 repositories.

When creating a new organization you have to give it a name (e.g. course name) and choose if you want to connect it with a personal or a business account. Choose the personal account option. After clicking “Next” you come back to the GitHub Classroom site. You have now created a new existing organization

### Grant access to an existing organization

Now go on “Go grant access”. This will open the GitHub website where you now have to click on the “grant” button for your newly created organization under “Organization access”. If you are prompted to enter a password at this step use your GitHub account password. Refresh the page of GitHub Classroom and you should now see your newly created organization. 

### Create a classroom

Select an organization. Next you are asked to name your classroom (e.g. course_name_Fall_2017). 

### Adding TAs

You have the opportunity to add TAs in GitHub Classroom. Unfortunately, to use this option directly via GitHub Classroom you have to make those accounts also “owners” of the classroom. As this is an unnecessary risk (owners have the power to modify and delete items in the repository) it is advised to add TAs through the GitHub organization directly. 

You set the organization permissions to read only and add the TAs as members. That way TAs will still be able to review all student repositories but do only have reading rights (→ [how to cahnge base permissions](https://docs.github.com/en/organizations/managing-access-to-your-organizations-repositories/setting-base-permissions-for-an-organization)).

### Adding a student roster

Watch this video or read the text below: 
{% include youtube.html id="DTzrKduaHj8" %}

There are three ways to add your student roster:

1. Import students from Canvas
You can configure GitHub Classroom as an external app for Canvas to import roster data into your classroom. For more information go to the following website: [connect Canvas to GitHub](https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/connect-a-learning-management-system-to-github-classroom)    
2. Upload a csv or text file with student identifiers (either student IDs, email addresses, names,..)
3. Directly type student identifiers into the text field

Once students have been imported you can update them as needed. Further students can be added by sinking them with Canvas, uploading another csv file or manually adding students via the text field. 

When students accept an assignment they are prompted to link their GitHub account to the roster themselves. If a student chooses the wrong identifier you can unlink the GitHub account from that identifier.

### Creating an assignment

When creating an assignment you have various options to choose from. You can set a deadline, specify wether it's supposed to be an individual or group assignment, set the repository visibility to private or public...

For more detailed information go to this website: [Creating assignments](https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/create-an-individual-assignment)

If you want to use autograding make sure that you follow all of the steps in: [How to set up autograding](/autograding.html)

In general, you want to enable the “feedback pull request” option. This will automatically open a pull request when the student accepts an assignment and allows you to give direct feedback, line by line, on the students code.

### Structuring your courses in GitHub Classroom

1. Create a GitHub organization for the course
    
   ![organizations_gh.PNG](../assets/images/organizations_gh.PNG)
    <!-- <img src="../assets/images/organizations_gh.PNG" alt="drawing" style="width:500px;"/> -->
    
2. Set up a GitHub classroom in the course organization for the semester’s class roster
    
    ![classrooms_gh.PNG](../assets/images/classrooms_gh.PNG)
    
3. Create assignments with the lesson content
4. Use template repositories to reuse a course structure you have created before