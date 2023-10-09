---
title: "DevOps90DaysChallenge"
datePublished: Fri Mar 03 2023 19:04:29 GMT+0000 (Coordinated Universal Time)
cuid: cleswmxj1000p08la7nnm5tbl
slug: devops90dayschallenge-1-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1677840461166/e3702622-d547-4274-b791-ff2df5ba6629.png
tags: linux, devops, shell, shell-script, devops-articles

---

# Hi 👋there,

# Now we are on the Day 6 task **File Permissions and Access Control Lists**.

<mark>Checkout the below link for Day 5 task:</mark>

[https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day06/tasks.md](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day06/tasks.md)

### 1.) Create a simple file **Change the user permissions of the file** and do `ls -ltr` to see the details of the files

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677859288229/c9acfaac-d5e5-4885-9c8d-9a0c1668a03d.png align="center")

Here you can see in the first point the file test1 has permission 777 which means it has all the read, write and execute permissions.

And below in the second point, I have changed the permission to 734 which means it has the <mark>read, write and execute for the user,</mark> <mark>write and execute for the group</mark> and <mark>read-only for others.</mark>

**2.)Write an article about File Permissions based on your understanding from the notes.**

In Linux, file permissions determine who can read, write, and execute a file. Each file and directory has a set of permissions that specify which users or groups can perform certain actions. These permissions are represented by a combination of letters and symbols, such as <mark>(-rwxrw-r — )</mark> that indicate the owner, group, and others’ permissions for a file or directory.

All three owners (user owner, group, others) in the Linux system have three types of permissions defined. Nine characters denote the three types of permissions.

1. **Read (r):** The read permission allows you to open and read the content of a file. But you can't do any editing or modification in the file.
    
2. **Write (w):** The write permission allows you to edit, remove or rename a file. For instance, if a file is present in a directory, and write permission is set on the file but not on the directory, then you can edit the content of the file but can't remove, or rename it.
    
3. **Execute (x):** In Unix type system, you can't run or execute a program unless execute permission is set. But in Windows, there is no such permission available.
    

![r/linux - chmod Cheatsheet](https://i.redd.it/vkxuqbatopk21.png align="left")

Each file and directory also has an owner, which is the user who created it, and a group, which is a set of users with similar permissions. The permissions can be set or changed using the chmod command, and the owner can be set or changed using the chown command.

When you are the **User owner**, then the user owner permission applies to you. Other permissions are not relevant to you.

When you are in the **Group** then the group permission applies to you. Other permissions are not relevant to you.

When you are the **Other,** then the other permission applies to you. User and group permissions are not relevant to you.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677860741352/403510fb-1f10-4326-97f2-8df026ce0762.png align="center")

example of file permission

### 3.)Read about ACL and try out the commands `getfacl` and `setfacl`

Access control list (ACL) provides an additional, more flexible permission mechanism for file systems. It is designed to assist with UNIX file permissions. ACL allows you to give permissions for any user or group to any disc resource.

Access control lists (ACLs) provide a finer-grained access control mechanism than these traditional Linux access permissions.

`getfacl` and `setfacl` are command line utilities in Linux that are used to view and modify the access control lists (ACLs) of files and directories.

`getfacl` command is used to display the access control list (ACL) of a file or directory. It shows the permissions for the owner, group owner, and all other users, as well as any additional users or groups that have been granted specific permissions.

`setfacl` command is used to set or modify the access control list (ACL) of a file or directory. This command is used to add, modify, or delete specific permissions for a user or group. The `setfacl` command can also be used to set the default ACL for a directory, which will be applied to all new files and directories created within that directory.

For example, the command `getfacl /home/ubuntu/test.txt` will display the permissions and acls of the file /home/user/example.txt and `setfacl -m u:user1:rwx /home/ubuntu/example.txt` will give user1 read, write and execute permissions on the file /home/user/example.txt.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677869821183/5b4681b8-0ae3-49e7-ab7b-ac024f2f5204.png align="center")

**Please, feel free to drop any questions in the comments below. I would be happy to answer them.**

**If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**

**\_ Thank you for reading**

**\_sandhya kumari**