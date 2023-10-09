---
title: "Version Control System..."
seoTitle: "version control system"
seoDescription: "Through my post my folks get to know about version control system in depth manner. Types of versioning of source code."
datePublished: Fri Feb 24 2023 09:32:39 GMT+0000 (Coordinated Universal Time)
cuid: cleic4lds056jddnv3ipa408o
slug: version-control-system
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1677225256819/49d04657-d72d-415b-a619-7b932085c286.webp
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1677230454028/8664b27b-1580-4c0d-b5af-48e46bda209e.webp
tags: github, version-control, versioning, github-actions-1, source-control

---

git architecture

# What is a version Control System?

version control is also known as a source control system and it is used to **track and manage** changes to software code. version control systems are software tools that help software teams manage changes to source code over time(<mark>recorder's changes within one or more files over time</mark>).

There are <mark>three</mark> types of version control systems:-

1. Local version control system
    
2. Centralized Version control system
    
3. Distributed version control system
    

so let's discuss all types of version control one by one.

### **Local Version Control System**

A local version control system is **<mark>a local database located on your local computer, in which every file change is stored as a patch</mark>**. Every patch set contains only the changes made to the file since its last version.

The main problem with this is that everything is stored locally. If anything were to happen to the local database, all the patches would be lost. If anything were to happen to a single version, all the changes made after that version would be lost.

Also, collaborating with other developers or a team is very hard or nearly impossible.

![](https://cdn.shortpixel.ai/spai/w_658+q_glossy+ret_img+to_webp/https://serengetitech.com/wp-content/uploads/2020/12/local-version-control.png align="left")

### **Centralized Version Control System**

**centralized version control system has a single server that contains all the file versions. This enables multiple clients to simultaneously access files on the server, pull them to their local computer or push them onto the server from their local computer**. This way, everyone usually knows what everyone else on the project is doing. Administrators have control over who can do what.

The biggest issue with this structure is that everything is stored on the centralized server. If something were to happen to that server, nobody can save their versioned changes, pull files or collaborate at all.

Similar to Local Version Control, if the central database became corrupted, and backups haven't been kept, you lose the entire history of the project except whatever single snapshots people happen to have on their local machines.

The most well-known examples of centralized version control systems are Microsoft Team Foundation Server (TFS) and SVN.

![Picture](https://www.htown-tech.com/uploads/6/9/4/9/69493533/centralized-vs-distributed-version-control-system-2_orig.jpg align="left")

### **Distributed Version Control System**

In DVCS, **there is no need to store the entire data in our local repository. Instead, we can have a clone of the remote repository to the local. We can also have a full snapshot of the project history**.

The User needs to update for the changes to be reflected in the local repository. Then the user can push the changes to the central repository. If other users want to check the changes, they will pull the updated central repository to their local repository, and then they update their local copy.

![dvcs](https://media.geeksforgeeks.org/wp-content/uploads/20190624140226/distvcs.png align="left")

### **Why do we need Version Control System?**

When multiple team members work on the same project, it is essential to have version control for the program. <mark>The version control system helps&nbsp;the team to share changes and merge changes made to&nbsp;artifacts&nbsp;seamlessly and efficiently.&nbsp;</mark> 

In DevOps, other than keeping track of changes, VCS also helps in developing and shipping the products faster.

VCS improves the following factors:

* Collaboration
    
* Storing Versions
    
* Backup
    
* Improves visibility
    
* Accelerate product delivery
    

**Please, feel free to drop any questions in the comments below. I would be happy to answer them.**

**If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**

**\_ Thank you for reading**

**\_sandhya kumari**