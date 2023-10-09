---
title: "Package Management..(Docker)"
datePublished: Thu Mar 16 2023 06:38:58 GMT+0000 (Coordinated Universal Time)
cuid: clfaqq9dm000309la57u2dqpq
slug: package-managementdocker
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1677487955349/2c2486bb-bbf0-4f90-91ea-22d12093dc32.png
tags: docker, developer, devops, docker-compose, devops-articles

---

# Hi 👋there,

# Today we are going to see Docker.

# Agenda of the today's topic is :

1. what is docker?
    
2. Why docker is so popular?
    
3. what is a docker image?
    
4. What is a docker Hub?
    
5. what are containers?
    
6. what is a docker file?
    
7. what is VM(Virtual Machine)?
    
8. when you should not use Docker or containers?
    
9. Extremely Useful Docker Commands?
    

### What is docker?

Docker is a new technology that allows development teams to build, manage, and secure apps anywhere.

Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly.

With Docker, you can manage your infrastructure in the same ways you manage your applications.

By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production.

Docker is lightweight, portable, and self-contained.

Docker containers improve software development, application deployment, and business agility.

### why docker is so popular?

Docker is popular because of the possibilities it opens for software delivery and deployment. Many common problems and inefficiencies are resolved with docker containers.

The six main reasons for Docker’s popularity are:

### **1\. Ease of use**

A large part of Docker’s popularity is how easy it is to use. Docker can be learned quickly, mainly due to the many resources available to learn how to create and manage containers. Docker is open-source, so all you need to get started is a computer with an operating system that supports Virtualbox, Docker for Mac/Windows, or supports containers natively, such as Linux.

### **2\. Faster scaling of systems**

Containers allow much more work to be done with far less computing hardware. In the early days of the Internet, the only way to scale a website was to buy or lease more servers. The cost of popularity was bound, linearly, to the cost of scaling up. Popular sites became victims of their success, shelling out tens of thousands of dollars for new hardware. Containers allow data centre operators to cram far more workloads into less hardware. Shared hardware means lower costs. Operators can bank those profits or pass the savings along to their customers.

### **3\. Better software delivery**

Software delivery using containers can also be more efficient. Containers are *portable.* They are also entirely self-contained. Containers include an isolated disk volume. That volume goes with the container as it is developed and deployed to various environments. The software dependencies (libraries, runtimes, etc.) ship with the container. If a container works on your machine, it will run the same way in a Development, Staging, and Production environment. Containers can eliminate the configuration variance problems common when deploying binaries or raw code.

### **4\. Flexibility**

Operating containerized applications is more flexible and resilient than that non-containerized applications. *Container orchestrators* handle the running and monitoring of hundreds or thousands of containers.

Container orchestrators are very powerful tools for managing large deployments and complex systems. Perhaps the only thing more popular than Docker right now is [Kubernetes](https://kubernetes.io/), currently the most popular container orchestrator.

### **5\. Software-defined networking**

Docker supports *software-defined networking.* The Docker CLI and Engine allow operators to define isolated networks for containers, without having to touch a single router. Developers and operators can design systems with complex network topologies and define the networks in configuration files. This is a security benefit, as well. An application’s containers can run in an isolated virtual network, with tightly-controlled ingress and egress paths.

### **6\. The rise of microservices architecture**

[The rise of microservices](https://raygun.com/blog/what-are-microservices/) has also contributed to the popularity of Docker. Microservices are simple functions, usually accessed via HTTP/HTTPS, that do one thing — and do it well.

Software systems typically start as “monoliths,” in which a single binary supports many different system functions. As they grow, monoliths can become difficult to maintain and deploy. Microservices break a system down into simpler functions that can be deployed independently. Containers are *terrific* hosts for microservices. They are self-contained, easily deployed, and efficient.

### what is a docker image?

![Build a Docker Image just like how you would configure a VM | by Nilesh  Jayanandana | Platformer — A WSO2 Company | Medium](https://miro.medium.com/max/1400/1*p8k1b2DZTQEW_yf0hYniXw.png align="left")

A Docker image is a lightweight, stand-alone, executable package that includes everything needed to run a piece of software, including the application code, libraries, dependencies, and runtime.

Images are created using the `docker build` command and are stored in a Docker registry, such as Docker Hub.

A Docker container is a running instance of a Docker image. You can create a container from an image using the `docker run (image name)`command. When you start a container, Docker creates a new runtime environment, which includes a copy of the files in the image, and runs the application inside the container.

You can create multiple containers from the same image, and they will all contain the same application code and dependencies. Each container is an isolated environment, and the applications running in different containers do not interfere with each other.

This makes it easy to scale up or down the number of containers running an application, depending on demand.

A docker image is a template for creating containers, and a Docker container is a running instance of a Docker image.

### What is a docker hub?

![Creating the first Docker Image and Pushing it to Docker Hub | by yasiru  nilan | Docker Captain | Medium](https://miro.medium.com/max/826/1*ttU6oMoZztKk2kjJid6PuQ.png align="left")

Docker Hub is a cloud-based repository in which Docker users and partners create, test, store and distribute container images.

We can use Docker Hub to find pre-built images that you can use as the basis for your own containerized applications, or you can use it to build, test, and store your custom images.

It is a great resource for quickly and easily deploying containerized applications.

**Docker Hub is a cloud-hosted version of the Docker Registry.**

**To push an image to Docker Hub :**

1. Log into Docker Cloud with the **(docker login)** command.
    
2. Tag the specified image using the **(docker tag)** command\*\*.\*\*
    
3. Push the image to Docker Hub with **(docker push).**
    
4. Check Docker Cloud to ensure the image appears in her repository.
    
5. A user can pull an image from Docker Hub with the **(docker pull)** command.
    

### what is a Docker container?

Containers are a way to package software in a format that can run consistently across different environments.

This makes it easier to develop, test, and deploy applications because it eliminates the need to worry about differences in libraries or system configurations on different machines.

Containers allow you to package an application with all of its dependencies and ship it as a single unit.

This makes it easier to move the containerized application between different computing environments, such as from a developer’s laptop to a staging or production environment.

*<mark>A container is a special type of process that is isolated from other processes. Containers are assigned resources that no other process can access, and they cannot access any resources not explicitly assigned to them.</mark>*

<mark>Processes that are not “containerized” can ask the operating system for access to </mark> *<mark>any</mark>* <mark>file on disk or </mark> *<mark>any</mark>* <mark>network socket.</mark>

Until containers became widely available, there was no reliable, guaranteed way to isolate a process to its own set of resources. A properly functioning container has *no way* to reach outside its resource “sandbox” to touch resources that were not explicitly assigned to it.

For example, two containers running on the same computer might as well be on two completely different computers, miles away from each other. They are entirely and effectively isolated from each other.

This isolation has several advantages:

* Two containerized processes can run side-by-side on the same computer, but they can’t interfere with each other.
    
* They can’t access each other’s data unless explicitly configured to do so.
    
* Two different applications can run containers on the same hardware with confidence that their processes and data are secure.
    
* Shared hardware means less hardware. Gone are the days when a company needs thousands of servers to run applications. That hardware can be shared between different business units or entirely different enterprise clients. The result is massive new economies of scale for private and public cent*re*s alike.
    
* ![What is a Docker container?](https://www.autopi.io/media/django-summernote/2021-08-04/59e5c775-ee08-444a-aef4-3df2190d648e.webp align="left")
    
* ### what is a docker file?
    
* A Dockerfile is a text file that contains instructions for how to build a Docker image.
    
    It is used to automate the process of building a Docker image so that you don’t have to manually specify all the steps required to build the image.
    
    A Dockerfile consists of a series of commands, each of which specifies a step in the process of building the image.
    
    These commands can be used to specify things like the base image to use, the packages to install, the commands to run, and so on.
    
* **Most commonly used tags in a Dockerfile:**
    
    * `FROM`: Specifies the base image to use for the image being built.
        
    * `RUN`: Executes a command during the build process.
        
    * `CMD`: Specifies the default command to run when the container is started.
        
    * `ENV`: Sets an environment variable in the container.
        
    * `COPY`: Copies files or directories from the host file system into the container.
        
    * `EXPOSE`: Exposes a specific port or port to be used by the container.
        
    * `LABEL`: Adds metadata to the image in the form of key-value pairs.
        
    * `USER`: Specifies the user to use when running the container.
        
    * `WORKDIR`: Sets the working directory for the container.
        
    * ### Example of Dockerfile:
        
    * ![Hello World using Docker and Python | by Umangshrestha | FAUN Publication](https://miro.medium.com/max/520/1*D-yumvSHYnKC6OfB6hWxgA.png align="left")
        
* This Dockerfile specifies that it will use the `python:3` image as the base image. The working directory will be /WORK\_REPO.
    
* And it will copy all the files at the current location in the container.
    
    RUN **shell command (mkdir and cd )**.
    
    It sets the default command for the container to `hello_world.py`.
    
    To build an image from a Dockerfile, you can use the `docker build` command.
    

### what is VM(Virtual Machine)?

A virtual machine (VM) is an operating system (OS) or application environment that is installed on software, which imitates dedicated hardware. The end-user has the same experience on a VM as they would on dedicated hardware.

A virtual machine (VM) is a virtual environment that works like a computer within a computer. It runs on an isolated partition of its host computer with its own CPU power, memory, operating system (such as Windows, Linux, macOS), and other resources. End users can run applications on VMs and use them as they normally would on their workstations.

A VM provides an isolated environment for running its OS and applications independently from the underlying host system or from other VMs on that host. The VM's OS is commonly referred to as the *guest OS*, and it can be the same as or different from the host OS or the other VMs. In this way, a single computer [can host multiple VMs](https://searchservervirtualization.techtarget.com/tip/Sizing-server-hardware-for-virtual-machines), all running different OSes and applications, without affecting or interfering with each other. The VM is still dependent on the host's physical resources, but those resources are virtualized and distributed across the VMs and can be reassigned as necessary, making it possible to run different environments simultaneously, as well as accommodate fluctuating workloads.

### when you should not use Docker or containers?

<mark>checkout the below link for more understanding</mark>

[https://www.freecodecamp.org/news/7-cases-when-not-to-use-docker/](https://www.freecodecamp.org/news/7-cases-when-not-to-use-docker/)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678946078040/7ebdb4a2-da0a-49b6-a4cb-a3e49784723c.png align="left")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678945167695/2ec6f94c-7178-4568-beb7-98ef67037b78.png align="left")

### Extremely Useful Docker Commands?

I am going to list such common but essential Docker commands that are extremely useful for day-to-day use by Docker users and admins.

  
<mark>docker logs </mark> \- Displays the logs of a running Docker container.  
<mark>docker inspect</mark> - Returns low-level information on a Docker object (container, image, network, etc.)  
<mark>docker network</mark> - Manages Docker networks.  
<mark>docker volume</mark> - Manages Docker volumes.  
<mark>docker-compose</mark> - Manages multi-container Docker applications.

<mark>docker rmi</mark> - Removes a Docker image.

<mark>docker version </mark> \- Shows the current Docker version installed on the system.  
<mark>docker info</mark> - Displays information about the current Docker installation and configuration.  
<mark>docker run</mark> - Runs a Docker container.  
<mark>docker ps</mark> - Lists the currently running Docker containers.  
<mark>docker images</mark> - Lists the Docker images available on the system.  
<mark>docker pull </mark> \- Downloads a Docker image from a Docker registry.  
<mark>docker push</mark> - Uploads a Docker image to a Docker registry.  
<mark>docker build</mark> - Builds a Docker image from a Dockerfile.  
<mark>docker tag</mark> - Tags a Docker image with a name that can be used for uploading to a Docker registry.  
<mark>docker commit</mark> - Creates a new Docker image from a running container.  
<mark>docker start </mark> \- Starts a stopped Docker container.  
<mark>docker stop</mark> - Stops a running Docker container.  
<mark>docker restart</mark> - Restarts a running Docker container.  
<mark>docker rm</mark> - Removes a stopped Docker container.  

**Please, feel free to drop any questions in the comments below. I would be happy to answer them.**

**If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**

**\_ Thank you for reading**

**\_sandhya kumari**