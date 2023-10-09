---
title: "DevOps90DaysChallenge"
datePublished: Tue Mar 07 2023 06:59:39 GMT+0000 (Coordinated Universal Time)
cuid: clexwi70y001t0ajtf6qqflym
slug: devops90dayschallenge-1-1-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678137101998/fec9a901-ab8b-47a2-ac82-e58eafe4edb8.png
tags: github, git, github-actions-1, git-commit, gitcommands

---

# Hi 👋there,

# Now we are on the Day 8 task

# Git and Github.

<mark>Checkout the below link for Day 8 task:</mark>

[https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day08/tasks.md](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day08/tasks.md)

# **What is Git?**

Git is a distributed version control system for software development. Git allows multiple people to collaborate on a project by keeping track of changes made to the codebase, making it easier to merge the changes made by different people and keep a clear history of changes.

With Git, developers can work on the same project from different locations and keep their own copies of the project, which are called “repositories”. When a developer makes changes to the code, they can “commit” the changes to their local repository and “push” the changes to a central repository that is shared by the rest of the team.

This makes it possible for everyone to have access to the latest version of the code at all times.

# **What is GitHub?**

GitHub is a web-based platform that offers version control hosting for software development. It is built on top of Git and provides a user-friendly interface for developers to manage their Git repositories. With GitHub, developers can store their code, track changes, and collaborate with others on projects.

# \*\*

What is Version Control? How many types of version controls do we have?\*\*

Version control is a system that records changes to a file or set of files over time, allowing developers to recall specific versions later. The main purpose of version control is to allow multiple people to work on a project simultaneously and to keep a history of changes that have been made to the codebase. This makes it easier to collaborate on a project, revert to previous versions of the code, and track the history of the development of a project.

There are two main types of version control systems: centralized version control systems and decentralized (or distributed) version control systems.

1. A centralized version control system (CVCS) uses a central server to store all the versions of a project’s files. Developers “check out” files from the central server, make changes, and then “check-in” the updated files. Examples of CVCS include Subversion and Perforce.
    
2. A distributed version control system (DVCS) allows developers to “clone” an entire repository, including the entire version history of the project. This means that they have a complete local copy of the repository, including all branches and past versions. Developers can work independently and then later merge their changes back into the main repository. Examples of DVCS include Git, Mercurial, and Darcs
    
3. # **Why we use distributed version control over centralized version control?**
    
    1. Better collaboration: In a DVCS, every developer has a full copy of the repository, including the entire history of all changes. This makes it easier for developers to work together, as they don’t have to constantly communicate with a central server to commit their changes or to see the changes made by others.
        
    2. Improved speed: Because developers have a local copy of the repository, they can commit their changes and perform other version control actions faster, as they don’t have to communicate with a central server.
        
    3. Greater flexibility: With a DVCS, developers can work offline and commit their changes later when they do have an internet connection. They can also choose to share their changes with only a subset of the team, rather than pushing all of their changes to a central server.
        
    4. Enhanced security: In a DVCS, the repository history is stored on multiple servers and computers, which makes it more resistant to data loss. If the central server in a CVCS goes down or the repository becomes corrupted, it can be difficult to recover the lost data.
        
    
    Overall, the decentralized nature of a DVCS allows for greater collaboration, flexibility, and security, making it a popular choice for many teams.
    

# **Task:**

## **1\. Create a new repository on GitHub and clone it to your local machine**

step 1

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678164545508/80ea8ef4-5c57-4dba-adcd-0d53f6f83a9c.png align="center")

step 2

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678165208282/15a4695c-0828-44b5-8f09-c4c9cd3a5692.png align="center")

step 3

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678165294464/d57858af-dce8-4cf3-a4ce-1da3dff3c20d.png align="center")

step 4

Now we will clone it locally.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678166731585/8c8a5b14-015d-41ff-8bcc-afbb6d53e66b.png align="center")

The clone is successful.

## **2\. Make some changes to a file in the repository and commit them to the repository using Git**

Now check the status of the repo.

<mark>#git status: check the status of the repo.</mark>

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678168063909/9daeaf4c-2e4f-4698-bfe9-5aa66c58c865.png align="center")

Now we will use the below command

<mark>#git add: to bring the file to staging</mark>

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678168853918/cbb4e6d7-e46e-4c84-81b5-a437fe85a903.png align="center")

<mark>#git commit: command to save your changes to the local repository and add a meaningful message.</mark>

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678169204800/7a4d4a65-ef44-44b2-a319-e41874af69b9.png align="center")

<mark>git commit –m “new </mark> [<mark>hello.py</mark>](http://hello.py) <mark> file added”</mark>

## **3\. Push the changes back to the repository on GitHub**

<mark>#git remote –v: command to check available remote URL</mark>

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678169489739/c5b96905-3326-48eb-9fa5-8a4559c8144c.png align="center")

If no available URL is present, then add a remote URL git remote add origin.

<mark>#git remote add origin </mark> [<mark>https://github.com/sandhya261996/devOpschallenge</mark>](https://github.com/sandhya261996/devOpschallenge)[<mark>.git</mark>](https://github.com/rajani103/improved-pancake.git)

Now push the new file to GitHub.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678170409889/bd32bc7d-4c16-4c1c-b68c-0c14e858109d.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678171136977/4b264290-771c-41db-a783-8406ef13d1d6.png align="center")

Deleting the file from the local and restoring the same.

The “git restore” command is used to restore changes in a Git repository to a previous state

<mark>#git restore filename</mark>

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678172174829/2fdb2ceb-e890-4217-9232-47fb15f96526.png align="center")

**Please, feel free to drop any questions in the comments below. I would be happy to answer them.**

**If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**

**\_ Thank you for reading**

**\_sandhya kumari**