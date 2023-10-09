---
title: "DevOps90DaysChallenge"
datePublished: Mon Mar 13 2023 11:20:20 GMT+0000 (Coordinated Universal Time)
cuid: clf6qgjnj000109lb6rkl4vah
slug: devops90dayschallenge-1-1-1-1-1-1-1-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678441320563/d1b8f78e-3a9d-4421-9d81-3989da44f917.png
tags: github, git, devops, github-actions-1, gitcommands

---

# Hi 👋there,

# Now we are on the Day 11 task

# Advance Git & GitHub\*\*(**Git Stash,Cherry-pick,Resolving Conflicts**)\*\*

<mark>Checkout the below link for Day 12 task:</mark>

[https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day11/tasks.md](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day11/tasks.md)

# **Git Stash:**

Git stash is a command that allows you to temporarily save changes you have made in your working directory, without committing them. This is useful when you need to switch to a different branch to work on something else, but you don’t want to commit the changes you’ve made in your current branch yet.

![Git #SourceTree | Git stash - Save changes away for later use. #Stashing -  YouTube](https://i.ytimg.com/vi/wpHEjqIjJGQ/maxresdefault.jpg align="left")

To use Git stash, you first create a new branch and make some changes to it. Then you can use the command git stash to save those changes. This will remove the changes from your working directory and record them in a new stash. You can apply these changes later. git stash list command shows the list of stashed changes.

You can also use git stash drop to delete a stash and git stash clear to delete all the stashes.

# **Cherry-pick:**

Git cherry-pick is a command that allows you to select specific commits from one branch and apply them to another. This can be useful when you want to selectively apply changes that were made in one branch to another.

![Git Cherry Pick - How to use the "cherry-pick" command in Git | Learn  Version Control with Git](https://www.git-tower.com/learn/media/pages/git/faq/cherry-pick/0da99a2863-1673968486/02-cherry-pick.png align="left")

To use git cherry-pick, you first create two new branches and make some commits to them. Then you use the git cherry-pick &lt;commit\_hash&gt; command to select the specific commits from one branch and apply them to the other.

# **Resolving Conflicts:**

Conflicts can occur when you merge or rebase branches that have diverged, and you need to manually resolve the conflicts before it can proceed with the merge/rebase. git status command shows the files that have conflicts, the git diff command shows the difference between the conflicting versions and the git add command is used to add the resolved files.

![How to Resolve Merge Conflicts in Git Tutorial | DataCamp](https://res.cloudinary.com/dyd911kmh/image/upload/v1652028749/image1_d21db326e6.png align="left")

# **Task-01**

1. Create a new branch and make some changes to it.
    
2. Use git stash to save the changes without committing them.
    
3. Switch to a different branch, make some changes and commit them.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678466911284/e896530e-8d98-4c2a-ac32-ac9e990357e7.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678467464086/352c591c-edd4-4090-82f0-4dd993853794.png align="center")

# **Task-02**

* In version01.txt of development, the branch adds the below lines after <mark>“This is the bug fix in development branch”</mark> that you added in Day10 and reverted to this commit.
    
* Line2&gt;&gt; After bug fixing, this is the new feature with minor alterations”
    
* Commit this with the message “ Added feature2.1 in development branch”
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678703588619/13cac9f9-1f1c-4e6d-aba0-152d14730b60.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678703641596/3e7415c7-489f-4420-855f-01bf6dd4a889.png align="center")

* Line3&gt;&gt; This is the advancement of the previous feature
    
* Commit this with the message “ Added feature2.2 in development branch”
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678704431962/155778f8-9b47-4f06-a70b-5c0326ab2afc.png align="center")
    
    * Line4&gt;&gt; Feature 2 is completed and ready for release
        
    * Commit this with the message “ Feature2 completed”
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678704922527/d4722142-184c-48de-9129-a7e3c343fa13.png align="center")
        
        * All these commits messages should be reflected in the Production branch too which will come out from the Master branch (Hint: try to rebase).
            
            ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678705272129/c50ec051-9722-465b-b995-4cf01d99c838.png align="center")
            
            Task-03
            
        * • In Production branch Cherry pick Commit “Added feature2.2 in development branch” and added below lines in it:
            
            • Line to be added after Line3&gt;&gt; This is the advancement of previous feature
            
            • Line4&gt;&gt;Added few more changes to make it more optimized.
            
            • Commit: Optimized the feature
            
        * ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678705503693/d91c065d-318a-4469-ad0e-330b06dd366b.png align="center")
            
            ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678705647187/d8ea64df-8cad-46ae-bfd5-5f16adf90d59.png align="center")
            
            ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678705933613/dc526f7f-d5c0-46cb-9cc6-1c722f455365.png align="left")
            
            After committing in main branch, switch to the different branch And run the cherry-pick command git cherry-pick
            
        * ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678706108322/848c4dcb-5750-419c-b8d5-99b8e6d791e8.png align="center")
            
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678706295815/e373b77c-0321-47df-95b7-5c1936f8bfb8.png align="center")
    
* **Please, feel free to drop any questions in the comments below. I would be happy to answer them.**
    
* **If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**
    
* **\_ Thank you for reading**
    
    **\_sandhya kumari**