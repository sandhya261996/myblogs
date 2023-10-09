---
title: "DevOps90DaysChallenge"
datePublished: Sat Apr 01 2023 17:24:07 GMT+0000 (Coordinated Universal Time)
cuid: clfy8tk7q000409l7ajvf5tuv
slug: devops90dayschallenge-1-1-1-1-1-1-1-1-1-1-1-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679821650523/f40a138d-2b6b-4258-b094-fd9db1323618.png
tags: docker, automation, containers, docker-compose, docker-images

---

# **Hi 👋there,**

# Now we are on the Day 18 task

# **Docker-Compose Project for DevOps Engineers**

<mark>Checkout the below link for Day 18 task:</mark>

[https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day18/tasks.md](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day18/tasks.md)

## Docker Compose

* Docker Compose is a tool that was developed to help define and share multi-container applications.
    
* With Compose, we can create a YAML file to define the services and with a single command, can spin everything up or tear it all down.
    
* To learn more about docker-compose [visit here](https://tecadmin.net/tutorial/docker/docker-compose/)
    

## What is YAML?

* YAML is a data serialization language that is often used for writing configuration files. Depending on whom you ask, YAML stands for yet another markup language or YAML ain’t markup language (a recursive acronym), which emphasizes that YAML is for data, not documents.
    
* YAML is a popular programming language because it is human-readable and easy to understand.
    
* YAML files use a .yml or .yaml extension.
    
* Read more about it [here](https://www.redhat.com/en/topics/automation/what-is-yaml)
    

## Task-1

Learn how to use the docker-compose.yml file, to set up the environment, configure the services and links between different containers, and also to use environment variables in the docker-compose.yml file.

# **What is Docker-Compose?**

Docker Compose is a tool for defining and running multi-container Docker applications. It allows you to define your application as a set of services, each with its own container, and specify how these containers should interact with each other.

With Docker Compose, you can define your application’s infrastructure, including databases, message queues, and web servers, in a simple YAML file.

Docker Compose provides a simple way to orchestrate and manage the containers that make up your application, allowing you to start and stop them together, scale them up and down as needed, and manage their network connections.

This makes it easier to develop, test, and deploy complex applications that consist of multiple services.

## **Step 1: Installing Docker-Compose in the server**

![How to Install Docker Compose on Ubuntu 20.04 {Step-by-Step Guide}](https://phoenixnap.com/kb/wp-content/uploads/2021/04/download-latest-docker-compose-version-on-ubuntu-20-04.png align="left")

## **Step 2: Create a docker-compose.yml file**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680367502361/15299b3d-c5bb-4f57-bde2-b315c648c722.jpeg align="center")

So now we will see all the things written in the docker-compose file.

* version: 3.8 denotes that we are using version 3.8 of Docker Compose.
    
* The service informs us about the various containers the compose file is going to create in this case three will be created as we have three services: web, PHP and mysqldb.
    
* The image keyword is used to specify the image from the docker hub for MYSQL containers, Ngnix and Php
    
* For all three services, we are using different ports and using the port keyword to mention the ports that need to expose for those services.
    
* And then, we also specify the environment variables for MySQL which are required to run MySQL.
    

## **Step 3: Running the docker-compose.yml file**

The `docker-compose-up` command is used to start up a set of containers defined in a Docker Compose file.

By default, `docker-compose up` starts containers in the foreground and logs their output to the console. You can use the `-d` flag to start the containers in detached mode, which runs them in the background.

The `docker-compose ps` command is used to display the status of containers defined in a Docker Compose file.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680367831640/704de536-720b-487f-b082-dfd3cd509a09.jpeg align="center")

## **Step 4: Verify that the application is working on the web browser**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680367988092/380d6c48-69aa-4925-a6f4-d9a0909a343f.jpeg align="center")

# **Task-2**

* Pull a pre-existing Docker image from a public repository (e.g. Docker Hub) and run it on your local machine. Make sure you reboot the instance after permitting the user.
    

![](https://miro.medium.com/v2/resize:fit:700/1*cOk1jWJ5Xb7CPNevU1Eo0w.png align="left")

* Run the container as a non-root user (Hint- Use `usermod` command to give the user permission to docker).
    
    ![](https://miro.medium.com/v2/resize:fit:700/1*7HObhEZD52_N61FudJ8-dA.png align="left")
    
* Then reboot the instance after permitting the user.
    
    ![](https://miro.medium.com/v2/resize:fit:620/1*u9CYAmjOGmR-6_hwuvVdRA.png align="left")
    
* Inspect the container’s running processes and exposed ports using the docker inspect command.
    

```bash
docker inspect <container_name or ID>
```

* Use the docker logs command to view the container’s log output.
    

```bash
docker logs <container_name or ID>
```

* Use the docker stop and docker start commands to stop and start the container.
    

```bash
docker stop <container-name or ID>
```

* Use the docker rm command to remove the container when you’re done.
    

```bash
docker start <container-name or ID>
```

**Please, feel free to drop any questions in the comments below. I would be happy to answer them.**

**If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**

**\_ Thank you for reading**

**\_sandhya kumari**