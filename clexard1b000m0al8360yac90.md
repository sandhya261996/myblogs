---
title: "DevOps90DaysChallenge"
datePublished: Mon Mar 06 2023 20:50:55 GMT+0000 (Coordinated Universal Time)
cuid: clexard1b000m0al8360yac90
slug: devops90dayschallenge-1package-manager
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678135600914/d47bb22d-d6e0-41ee-a4c2-764a0d921e45.png
tags: docker, package, jenkins, package-manager, package-managers

---

### Hi 👋there, Now we are on the Day 7 task

### Understanding package manager and systemctl .

<mark>Checkout the below link for Day 7 task:</mark>

[https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day07/tasks.md](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day07/tasks.md)

# **1.)What Package and package manager in Linux?**

<mark>A </mark> ***<mark>package management system or package manager</mark>*** is a group of software tools. It automates the installation process, upgrading process, configuration process, and removal process of the computer programs for an operating system of the computer in an efficient manner.

In simpler words, a package manager is a tool that allows users to install, remove, upgrade, configure and manage software packages on an operating system. The package manager can be a graphical application like a software centre or a command lines tool like <mark>apt-get, YUM or Pacman.</mark>

A package is usually referred to as an application but it could be a GUI application, command line tool or a software library (required by other software programs). A package is essentially an archive file containing the binary executable, configuration file and sometimes information about the dependencies.

In the older days, [software used to installed from its source code](https://itsfoss.com/install-software-from-source-code/). You would refer to a file (usually named readme) and see what software components it needs, and the location of binaries. A configure script or makefile is often included. You will have to compile the software on your own along with handling all the dependencies (some software require installation of other software) on your own.

To get rid of this complexity, Linux distributions created their own packaging format to provide the end users with ready-to-use binary files (precompiled software) for installing software along with some [metadata](https://www.computerhope.com/jargon/m/metadata.htm?ref=its-foss) (version number, description) and dependencies.

It is like baking a cake versus buying a cake.

# **2.)Different kinds of package managers?**

Package Managers differ based on the packaging system but the same packaging system may have more than one package manager.

For example, RPM has Yum and DNF, package managers. For DEB, you have apt-get, aptitude command line-based package managers.

## **Task :**

## **You have to install docker and Jenkins in your system from your terminal using package managers.**

![What Are Docker Image Layers?](https://www.howtogeek.com/wp-content/uploads/2022/05/Docker-New.jpeg?height=200p&trim=2,2,2,2&crop=16:9 align="left")

# **How to Install Docker on Ubuntu: A Step-By-Step Guide**

1\. Open the terminal on Ubuntu.

2\. Remove any [Docker files](https://www.simplilearn.com/tutorials/docker-tutorial/what-is-dockerfile) that are running in the system, using the following command:

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>$ sudo apt-get remove docker docker-engine </strong><a target="_blank" rel="noopener noreferrer nofollow" href="http://docker.io" style="pointer-events: none"><strong>docker.io</strong></a></p></td></tr></tbody></table>

After entering the above command, you will need to enter the password of the root and press enter.

3\. Check if the system is up-to-date using the following command:

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>$ sudo apt-get update</strong></p></td></tr></tbody></table>

4\. Install Docker using the following command:

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>$ sudo apt install </strong><a target="_blank" rel="noopener noreferrer nofollow" href="http://docker.io" style="pointer-events: none"><strong>docker.io</strong></a></p></td></tr></tbody></table>

You’ll then get a prompt asking you to choose between y/n - choose ***y***

5\. Install all the dependency packages using the following command:

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>$ sudo snap install docker</strong></p></td></tr></tbody></table>

6\. Before testing Docker, check the version installed using the following command:

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>$ docker --version</strong></p></td></tr></tbody></table>

7\. Pull an image from the Docker hub using the following command:

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>$ sudo docker run hello-world</strong></p></td></tr></tbody></table>

Here, ***hello-world*** is the docker image present on the Docker hub.

8\. Check if the docker image has been pulled and is present in your system using the following command:

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>$ sudo docker images</strong></p></td></tr></tbody></table>

9\. To display all the containers pulled, use the following command:

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>$ sudo docker ps -a</strong></p></td></tr></tbody></table>

10\. To check for containers in a running state, use the following command:

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>$ sudo docker ps</strong></p></td></tr></tbody></table>

You’ve just successfully installed Docker on Ubuntu!

# **How to Install Jenkins on Ubuntu: A Step-By-Step Guide**

![Linux, Cloud & Windows tutorials for beginners : How to install Jenkins on  Ubuntu 16.04.](https://2.bp.blogspot.com/-2HkykW4sBuI/W5ycOUa3mFI/AAAAAAAAETk/N25MoH9AsyULAujenqGc2IueuiUywkIEwCLcBGAs/s1600/Jenkins-Linux.jpg align="left")

## **Step 1: Install Java**

Jenkins requires the Java Runtime Environment (JRE). This guide uses OpenJDK for the Java environment. OpenJDK is a Development Kit and includes the Java Runtime Environment.

Follow the steps below to install Java on Ubuntu:

1\. [Check if you already have Java](https://phoenixnap.com/kb/check-java-version-linux) installed on your Ubuntu system:

<mark>java --version</mark>

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678110949991/fa1cab58-99c2-4918-85ce-fc68f27d1619.png align="center")

Since Java is not installed on our system, we will install it using OpenJDK.

2\. First, open a terminal and update the system package repository by running:

<mark>sudo apt update</mark>

3\. Depending on which Java version you want to install, Java 8 or 11, run one of the following commands:

To install OpenJDK 11, run:

<mark>sudo apt install openjdk-11-jdk -y</mark>

We install OpenJDK version 11 on our system:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678126505651/a10345be-5df5-40d9-91e9-f55af20a8339.png align="center")

### **Step 2: Add Jenkins Repository**

1\. Start by importing the GPG key. The GPG key verifies package integrity but there is no output. Run:

<mark>curl -fsSL </mark> [<mark>https://pkg.jenkins.io/debian-stable/jenkins.io.key</mark>](https://pkg.jenkins.io/debian-stable/jenkins.io.key) <mark>| sudo tee /usr/share/keyrings/jenkins-keyring.asc &gt; /dev/null</mark>

2\. Add the Jenkins software repository to the source list and provide the authentication key:

<mark>echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] </mark> [<mark>https://pkg.jenkins.io/debian-stable</mark>](https://pkg.jenkins.io/debian-stable) <mark>binary/ | sudo tee /etc/apt/sources.list.d/Jenkins.list &gt; /dev/null</mark>

The command adds the Long Term Support (LTS) stable release to the sources list, but there is no output.

## **Step 3: Install Jenkins**

After setting up the prerequisites, follow the steps below to install Jenkins on Ubuntu:

1\. Update the system repository one more time. Updating refreshes the cache and makes the system aware of the new Jenkins repository.

<mark>sudo apt update</mark>

2\. Install Jenkins by running:

<mark>sudo apt install Jenkins -y</mark>

Wait for the download and installation to complete.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678129305010/949d5a41-5420-4efd-be6d-c166a40c56e6.png align="center")

3\. To check if Jenkins is installed and running, run the following command:

<mark>sudo systemctl status Jenkins</mark>

A bright green entry labelled `active (running)` should appear in the output, indicating that the service is running.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678130842307/3dc084b8-c369-4f1c-a6c7-b0525abbf46a.png align="center")

4\. Exit the status screen by pressing **Ctrl**+**Z**.

# **What are systemctl and systemd?**

The <mark>systemctl</mark> command is a utility that is responsible for examining and controlling the systemd system and service manager. It is a collection of system management libraries, utilities and daemons that function as a successor to the System V init daemon.

The new systemctl commands have proven quite useful in managing a servers services. It provides detailed information about specific systemd services, and others that have server-wide utilization.

It provides various commands to start, stop, restart, enable, and disable services, as well as other functionalities such as inspecting the status of services, displaying log messages, and managing system-level settings and configurations.

<mark>systemd</mark> is a Linux init system and system manager that is widely used in modern Linux distributions as the default init system. It provides a way to manage and control the various services that run on a Linux system, as well as other system-level functionality.

Here are a few examples of common tasks that can be performed using `systemctl`:

* Start a service: `systemctl start <service-name>`
    
* Stop a service: `systemctl stop <service-name>`
    
* Restart a service: `systemctl restart <service-name>`
    
* Enable a service to start automatically at boot: `systemctl enable <service-name>`
    
* Disable a service from starting automatically at boot: `systemctl disable <service-name>`
    
* Check the status of a service: `systemctl status <service-name>`
    

Overall, `systemd` and `systemctl` provide a centralized and standardized way to manage services and other system-level components on Linux, making it easier to configure and maintain a Linux system.

**1.)check the status of docker service in your system (make sure you completed above tasks, else docker won’t be installed)**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678133435351/1196311c-fbcb-44cb-be61-ad4ec1eaac41.png align="center")

**2\. stop the service jenkins and post before and after screenshots**

Before :

<mark>systemctl status jenkins</mark>

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678133507332/3eac4169-83c6-4116-a243-a2c5408e8c25.png align="center")

After:

<mark>systemctl stop jenkins</mark>

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678133643209/cb190016-2c39-413b-a14d-feb5cd2f6f68.png align="center")

3\. Read about the commands systemctl vs service

`systemctl` and `service` are both tools used to manage and control services on a Linux system. However, they have some differences:

1. `systemctl` is the newer tool and is used on systems that use the systemd init system, which is now widely adopted as the default init system for many popular Linux distributions, including Fedora, Red Hat Enterprise Linux, and Ubuntu.
    
2. `service` is the older tool and is used on systems that use the System V init system, which was the previous standard init system used in many popular Linux distributions.
    
3. `systemctl` provides more advanced features compared to `service`, such as the ability to manage units, which are the basic building blocks of Systemd. This allows you to manage not just services, but also other system components, such as sockets, devices, and mount points, with a unified interface.
    
4. `service` is limited to managing services only, and its syntax and options are not as advanced as those of `systemctl`.
    

**service commands :**

* `service <service-name> start`
    
* `service <service-name> status`
    
* `service <service-name> stop`
    
* `service <service-name> restart`
    

**systemctl commands :**

* `systemctl start <service-name>`
    
* `systemctl stop <service-name>`
    
* `systemctl restart <service-name>`
    
* `systemctl enable <service-name>`
    
* `systemctl disable <service-name>`
    
* `systemctl status <service-name>`
    

**Please, feel free to drop any questions in the comments below. I would be happy to answer them.**

**If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**

**\_ Thank you for reading**

**\_sandhya kumari**