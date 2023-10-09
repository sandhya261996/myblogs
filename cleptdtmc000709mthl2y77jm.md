---
title: "DevOps90DaysChallenge"
datePublished: Wed Mar 01 2023 15:10:06 GMT+0000 (Coordinated Universal Time)
cuid: cleptdtmc000709mthl2y77jm
slug: devops90dayschallenge-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678134365996/02f2812e-b6e9-46c0-948c-18af68667558.png
tags: linux, devops, shell, script

---

# Hi 👋there,

# Now we are on the Day 5 task of Advanced shell scripting.

<mark>Checkout the below link for Day 5 task:</mark>

[https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day05/tasks.md](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day05/tasks.md)

**1.) Write a bash script** [**createDirectoriess1.sh**](http://createDirectoriess1.sh) **that when the script is executed with three given arguments (one is the directory name and second is the start number of directories and the third is the end number of directories ) it creates a specified number of directories with a dynamic directory name.**

You have to do the same using Shell Script i.e using either Loops or command with start day and end day variables using arguments -

So Write a bash script to [create directories. sh](http://createDirectories.sh) when the script is executed with three given arguments (one is the directory name and the second is the start number of directories and the third is the end number of directories ) it creates a specified number of directories with a dynamic directory name.

Example 1: When the script is executed as

`./`[`createDirectories.sh`](http://createDirectories.sh) `day 1 90`

then it creates 90 directories as `day1 day2 day3 .... day90`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677667486872/432e9697-2835-4b3b-842f-f947a176e54d.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677661500429/e7505fc3-e19b-4ec7-a419-76902899b1af.png align="center")

**2) Create a Script to back up all your work done till now.**

One of the simplest ways to back up a system is using a *shell script*. For example, a script can be used to configure which directories to backup, up and pass those directories as arguments to the tar utility, which creates an archive file. The archive file can then be moved or copied to another location.

![Backup](https://user-images.githubusercontent.com/124788172/218464554-4f5e2a57-89b6-45d1-a8fd-6bbfc31aa5bd.png align="left")

#!/bin/bash

<mark>Set the source and destination directories</mark>

SOURCE\_DIR="/home/user" DESTINATION\_DIR="/mnt/backup"

<mark>Create the destination directory if it doesn't exist</mark>

mkdir -p $DESTINATION\_DIR

<mark>Set the filename and date for the backup</mark>

FILENAME="backup\_$(date +%Y-%m-%d).tar.gz"

<mark>Create the compressed archive of the source directory</mark>

tar -czvf "$DESTINATION\_DIR/$FILENAME" $SOURCE\_DIR

<mark>Print a message when the backup is complete</mark>

echo "Backup complete: $FILENAME"

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677683298758/fb5cb894-61c0-421d-92c3-f42d8dd78b7d.png align="left")

In this example, the script sets the source and destination directories as variables, creates the destination directory if it doesn't exist, generates a filename with the current date, creates a compressed archive of the source directory, and prints a message indicating that the backup is complete.

### **3.) Read About Cron and Crontab, to automate the Script**

Cron is a Linux utility that schedules tasks to run automatically at specified intervals.

Cron is a time-based job scheduler in Linux and Unix-like operating systems that allows you to schedule tasks to run automatically at specified intervals, such as once a day, once an hour, or even every minute.

The tasks are defined in a crontab file, which is a simple text file containing a list of commands meant to be run at specified times. Each line of the file represents a single cron job and follows a particular syntax.

A crontab file is composed of six fields, separated by spaces, that specify the schedule for a task to run. The fields, in order, are:

1. Minute (0–59)
    
2. Hour (0–23)
    
3. Day of the month (1–31)
    
4. Month (1–12)
    
5. Day of the week (0–7, where both 0 and 7 represent Sunday)
    
6. Command to be executed
    

![How to add Crontab Jobs in Linux/Unix - TekkieHead](https://tekkiehead.com/wp-content/uploads/2022/07/image.png align="left")

You can use the command `crontab -e` to edit your crontab file and `crontab -l` to list the current crontab file.

You can also use `crontab -r` to remove your current crontab file, `crontab -d` to delete a specific user crontab and `cron -l -u <username>` to list a specific user crontab.

**4.) Read about User Management**

User management refers to the process of creating, modifying, and deleting user accounts on a computer system or network. It also includes managing user permissions and access to resources.

Some common tasks related to user management are:

1. Creating new user accounts with a unique username and password
    
2. Assigning different levels of privileges or permissions to users, such as access to certain files or directories
    
3. Changing or resetting user passwords
    
4. Disabling or deleting user accounts
    
5. Managing groups of users and assigning group permissions
    
6. Auditing user activity and tracking changes to user accounts
    

On Linux systems, user management can be done using command-line tools such as `useradd`, `usermod`, `userdel`, `password`, and `groupadd`, `group mod`, `group del`.

**5.) Create 2 users and just display their Usernames**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677674113462/f3848fce-e115-4231-85bb-a2f3ec62c303.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677674259566/a57a8c11-4264-4b15-b2d8-2c0148515b90.png align="center")

**Please, feel free to drop any questions in the comments below. I would be happy to answer them.**

**If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**

**\_ Thank you for reading**

**\_sandhya kumari**