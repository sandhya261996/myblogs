---
title: "DevOps90DaysChallenge"
datePublished: Tue Mar 07 2023 07:54:30 GMT+0000 (Coordinated Universal Time)
cuid: clexygqu7001d0al6b2lq2fei
slug: devops90dayschallenge-1-1-1-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678137722611/37eb4027-c49b-4fec-bf45-e8fc15f3d431.png
tags: github, git, devops, github-actions-1, gitcommands

---

# Hi 👋there,

# Now we are on the Day 9 task

# **Deep Dive in Advanced Git & GitHub**.

<mark>Checkout the below link for Day 9 task:</mark>

[https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day09/tasks.md](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day09/tasks.md)

## **What is Git and why is it important?**

Git is a version-control system that is widely used for software development and other version-controlled projects. It is a distributed system, which means that the code and its full history are stored in many different places, so it is very difficult to lose data.

Git is important because it provides a way for multiple people to collaborate on a project and keep track of the changes made to the code over time. This makes it easier to maintain and develop software, especially for large projects. With Git, developers can work independently and submit their changes, which can then be easily merged with the main codebase.

Git also makes it easier to revert to an earlier version of the code if a mistake is made or if you need to return to a previous state for some other reason. Additionally, Git allows for easy experimentation and exploration, as you can switch between different versions of your code to see the impact of different changes.

In summary, Git is a powerful tool that helps software development teams to collaborate and manage changes to their code over time, making it an essential tool for many software projects.

## **What is the difference Between Main Branch and Master Branch?**

In Git, the main branch is the default branch name that is usually used to represent the primary line of development. The “main” branch is intended to serve as the long-lived, stable branch, where the source code of a project is held.

The “master” branch, on the other hand, is a commonly used name for the main branch in many Git projects. The name “master” originated from the days when Git was mostly used for version control of software code, and the “master” branch represented the latest version of the code that was considered production-ready.

So to summarize, both “main” and “master” refer to the primary line of development in a Git repository, but “main” is a more recent term that is used to avoid potentially problematic language.

## **Explain the difference between Git and GitHub?**

| Basis | Git | GitHub |
| --- | --- | --- |
| **Production** | Git was first introduced in April 2005. | GitHub was first introduced in October 2007. The site was later developed in April 2008. |
| **Owned by** | Git is maintained by Linux | Is maintained by Microsoft. |
| **Application** | Git is a Command-Line tool. | GitHub is a Graphical User Interface. |
| **Storage** | Is installed locally in the system for use and does not require the internet. | Can be accessed on the web. It needs an internet connection. |
| **Function** | Majorly focused on version control and code conserving. | Is majorly focused on web hosting and code sharing. |
| **User Preferences** | Lacks user management features | GitHub has built-in user management features. It also provides Organisational and Enterprise level accounts with unlimited public repositories and collaborators. |
| **Integrations** | Provides no external tool configuration. | GitHub provides multiple external tools including third-party tools. |
| **Availability** | Git is an open-source that allows users to modify and share software. | GitHub is inclusive of free-tier and paid-tier versions. However, it is not open source. |
| **Security** | The privacy in Git is too strong | Privacy depends on the settings of the repositories. |
| **Platform** | It is compatible with Windows, macOS, Linux, Solaris, AIX | It is compatible with Windows, macOS, Linux, and all other web browsers. |
| **Competitors** | Although GIT is one of the best version controllers, it fights with Mercurial, IBM, etc. | Major competitors include GitLab, BITBUCKET, etc. |
| **Communication/Issue Management** | There’s no dedicated system to communicate with collaborators. | GitHub provides a specific tab to communicate and resolve issues with collaborators. |

## **How do you create a new repository on GitHub?**

To create a new repository on GitHub, follow these steps:

1. Go to the GitHub website and log in to your account.
    
2. Click the “+” icon in the top right corner of the screen and select “New repository”.
    
3. Enter a name for your repository in the “Repository name” field.
    
4. Optionally, you can add a description of your repository in the “Description” field.
    
5. Select whether you want your repository to be public or private. Public repositories are visible to anyone and can be cloned or forked by anyone, while private repositories are only accessible to you and other people you specifically invite.
    
6. Choose a license for your repository.
    
7. Click the “Create repository” button.
    

Once you have created your repository, you can add files, make changes, and share your code with others. You can also set up a Git repository on your local machine and push your changes to GitHub so that you can keep track of your code and collaborate with others.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678174271516/5155586b-0160-48bd-a1a6-ef01edd53419.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678165208282/15a4695c-0828-44b5-8f09-c4c9cd3a5692.png align="left")

## **What is the difference between local & remote repositories? How to connect locally remotely?**

In Git, a local repository is a copy of a project that is stored on your computer. You can make changes to the code in your local repository, commit those changes, and manage the history of your project without an internet connection.

A remote repository, on the other hand, is a version of your project that is stored on a server and is accessible from anywhere with an internet connection. Remote repositories are typically used for collaboration and sharing code with others.

To connect a local repository to a remote repository, you need to use the “git remote” command. Here are the basic steps to connect a local repository to a remote repository:

1. Initialize a Git repository in your local directory by running the “git init” command.
    
2. Go to GitHub and create a new remote repository for your project.
    
3. Copy the URL of the remote repository to your clipboard.
    
4. In your local repository, run the following command to add the remote repository:
    

```plaintext
git remote add origin <remote repository URL>
```

Replace “&lt;remote repository URL&gt;” with the URL of the remote repository.

5\. To push your local repository to the remote repository, run the following command:

```plaintext
git push -u origin master
```

This command pushes the “master” branch of your local repository to the “origin” remote repository and sets the “origin” remote as the default remote for future pushes.

# **Tasks:**

Create a repository named “Devops” on GitHub

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678174663696/81fce44b-a039-4ca8-a969-a8ed29023847.png align="center")

* Connect your local repository to the repository on GitHub.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678174827790/f803a12b-3619-482c-a9e1-e05441d4458c.png align="center")

* Create a new file in Devops/Git/Day-02.txt & add some content to it
    
* Push your local commits to the repository on GitHub
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678175114856/520dd568-879a-4f82-b67b-cd7073ca15f6.png align="center")
    
* **Please, feel free to drop any questions in the comments below. I would be happy to answer them.**
    
    **If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**
    
    **\_ Thank you for reading**
    
* **\_sandhya kumari**