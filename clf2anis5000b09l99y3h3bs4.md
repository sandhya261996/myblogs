---
title: "DevOps90DaysChallenge"
datePublished: Fri Mar 10 2023 08:46:46 GMT+0000 (Coordinated Universal Time)
cuid: clf2anis5000b09l99y3h3bs4
slug: devops90dayschallenge-1-1-1-1-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678376062554/bc6fae12-bd96-4036-93d8-00674bbadbe4.png
tags: github, git, github-actions-1, git-branch, git-rebase

---

# Hi 👋there,

# Now we are on the Day 10 task

# **Advance Git & GitHub(Rebase, Merege,Revert, Branching)**.

<mark>Checkout the below link for Day 10 task:</mark>

[https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day10/tasks.md](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day10/tasks.md)

# **Git Branching**

Git branching is a feature in the Git version control system that allows developers to create multiple independent branches of their codebase, enabling them to work on different features or fixes simultaneously without affecting the main codebase.

Changes made to a branch can be merged back into the main codebase once they are complete and have been reviewed. Git branching is a powerful tool that allows developers to manage code changes more efficiently and collaboratively.

# **Git Revert and Reset**

Git revert undoes a specific commit by creating a new commit that undoes the changes made by the original commit. This is a safe way to undo changes, as it does not change the commit history and allows you to easily undo the undo if needed.

Git reset, on the other hand, allows you to move the current branch to a specific commit, which can potentially change the commit history. It’s important to use reset with caution, as it can cause data loss and make it difficult to undo changes.

# **What Is Git Rebase?**

Git rebase is a command that allows you to apply the changes from one branch to another. This can be useful for keeping your branch up-to-date with changes made in a separate branch or for creating a linear history before merging your changes into the main branch.

# **What Is Git Merge?**

Git merge is a command that allows you to combine the changes from two or more branches into a single branch. When you run `git merge`, Git will automatically try to merge the changes made in the source branch into the target branch.

If there are no conflicts between the changes, Git will create a new commit that includes all the changes from the merged branch. If there are conflicts, Git will prompt you to manually resolve them before the merge can be completed.

Merging is a common way to integrate changes from other branches into your working branch. It creates a new commit that represents the combination of changes.

## **TASK 1 :**

Add a text file called version01.txt inside the Devops/Git/ with “This is the first feature of our application” written inside. This should be in a branch coming from `master`, \[hint try `git checkout -b dev`\], switch to the `dev` branch ( Make sure your commit message will reflect as "Added new feature"). \[Hint use your knowledge of creating branches and Git commit command\]

* version01.txt should reflect at the local repo first followed by the Remote repo for review. \[Hint use your knowledge of Git push and git pull commands here\]
    

Add a new commit in `dev` branch after adding the below-mentioned content in Devops/Git/version01.txt: While writing the file make sure you write these lines

* 1st line&gt;&gt; This is the bug fix in the development branch
    
* Commit this with the message “ Added feature2 in development branch”
    
* 2nd line&gt;&gt; This is gadbad code
    
* Commit this with the message “ Added feature3 in the development branch
    
* 3rd line&gt;&gt; This feature will gadbad everything from now.
    
* Commit with the message “ Added feature4 in the development branch
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678387444835/76ea55e1-3acb-4f44-8576-c90dfeed8f14.png align="center")
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678387578418/d6a87f6d-1065-4803-8512-2021d5f595fc.png align="center")
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678388839133/a78a36a6-968c-4688-afe2-fbe4ec448152.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678388743095/3ed52681-9ca0-4a8c-b89d-a96172fa43d8.png align="center")

2\. Create a new Branch “dev” and commit the changes

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678437867190/0115e461-82f5-4f90-85f0-2199baf7b1f0.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678427334817/d00d98e0-2c9d-4999-882e-8975d6df55d7.png align="center")

3\. Use the git reset command to go back to the correct file. And after that switch to the main branch

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678429693006/93ff5e7f-9474-4982-bc14-838f60a798f3.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678429761861/6603f09f-30f5-45b2-b375-c870673258f1.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678430418689/06f4fd4b-aae3-4644-9899-00509635d9ab.png align="center")

4\. Merge the dev branch to the main branch and push the changes to the remote Repository

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678431471856/f21404e8-972c-4eee-882a-b81c97369d04.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678431658183/eee1ee4b-d7cf-4100-b83a-623cb7c25395.png align="center")

5\. Changes are Updated on Remote Repository

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678432297786/efa81c15-04b2-49c4-bf79-30fe34b16052.png align="center")

# **Task 2:**

* Demonstrate the concept of branches with 2 or more branches with a screenshot.
    
* add some changes to `dev` branch and merge that branch in `master`
    
* as a practice try git rebase too, and see what difference you get.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678436698179/bd4bf88f-dbbb-498d-afca-4f71f109afc3.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678437151016/3372d251-0ea3-4732-87cb-f0dba051b610.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678436288346/abef04e4-92b1-4ac8-8f9e-ac59bbfc104d.png align="center")

* **Please, feel free to drop any questions in the comments below. I would be happy to answer them.**
    
* **If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**
    
* **\_ Thank you for reading**
    
* **\_sandhya kumari**