---
title: "DevOps90DaysChallenge"
datePublished: Thu Mar 23 2023 20:36:58 GMT+0000 (Coordinated Universal Time)
cuid: clflkqwwv00040albhcq14ihm
slug: devops90dayschallenge-1-1-1-1-1-1-1-1-1-1-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679303528343/b8eb31bd-122d-4d9a-a4d5-f4506e3ebfa5.png
tags: docker, cloud-computing, devops, containers, docker-compose

---

# Hi 👋there,

# Now we are on the Day 16 task

# **Docker for DevOps Engineers**

<mark>Checkout the below link for Day 16 task:</mark>

[https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day16/tasks.md](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day16/tasks.md)

![30,000 Feet Overview of Docker](https://cdn-images-1.medium.com/max/1400/1*qYowu9hq5jWzQWU6G8n16w.gif align="left")

# **Docker**

Docker is a software platform that allows you to build, test, and deploy applications quickly. Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime. Using Docker, you can quickly deploy and scale applications into any environment and know your code will run.

# **Tasks**

Install Docker on your server first.

<mark>Checkout the below link for docker installation:</mark>

[https://docs.docker.com/engine/install/ubuntu/](https://docs.docker.com/engine/install/ubuntu/)

### some Docker Commands:

**1.) Use the** `docker pull` **command to pull the image from the docker hub.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679601482394/5fea5783-d76d-4017-99b0-1bd24bf8db65.png align="center")

Then we used the docker run command to run a container in detached mode using the pulled image.

2.)To create a container with a container name:

* 1.)without a port map
    
    command — docker run -d — name &lt;container-name&gt; &lt;image-name&gt;
    
* 2.)with a port map
    
    command — docker run -p — name &lt;container-name&gt; &lt;image-name&gt;
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679601790724/590692f2-cd50-4732-ba90-a22b7157afbb.png align="center")
    
    * **3.) Use the** `docker inspect` **command to view detailed information about a container or image.**
        
    
    ![Docker: Find the network for a container | Mark Needham](https://www.markhneedham.com/blog//uploads/2019/05/docker_inspect.png align="left")
    
* **4.) Use the** `docker port` **command to list the port mappings for a container.**
    
    `docker port` is a Docker command that displays the public-facing port(s) of a running container.
    

docker port &lt;container name&gt;

![Docker Ports Mapping - YouTube](https://i.ytimg.com/vi/KA0PwypqY9k/maxresdefault.jpg align="left")

* * **5.)Use the** `docker stats` **command to view resource usage statistics for one or more containers.**
        
        `docker stats` is a Docker command that displays real-time usage statistics for running containers.
        
        ```bash
        docker stats [OPTIONS] [CONTAINER...]
        ```
        
        Options:
        
        * — no-stream: Disable streaming stats and only pull the first result
            
        * — no-trunc: Do not truncate output
            
        * — all , -a: Show all containers (default shows just running)
            
        * — format: Pretty print images using a Go template
            
        * **6.) Use the** `docker top` **command to view the processes running inside a container.**
            
        
        `docker top` is a Docker command that shows the processes running inside a container.
        
        The output of the `docker top` command includes the process ID, user, CPU usage, memory usage, and command that is being executed by each process.
        
        ```bash
        docker top <container name>
        ```
        
        ![](https://miro.medium.com/v2/resize:fit:700/1*6MjSplJ2fa6KFLJJKiD8JQ.png align="left")
        
        * **7.)Use the** `docker load` **command to load an image from a tar archive.**
            
        
        `docker load` is a Docker command that loads one or more Docker images from a tar archive.
        
        ```bash
        docker load [OPTIONS] < myimages.tar
        ```
        
        ![Export your Docker images and run them remotely - Technology from Tukwila](https://tuktech.com/wp-content/uploads/2020/03/load-docker-image-1024x462.png align="left")
        
        * **Use the** `docker save` **command to save an image to a tar archive.**
            
        
        `docker save` is a Docker command that saves one or more Docker images to a tar archive.
        
        ```bash
        docker save [OPTIONS] IMAGE [IMAGE…]
        ```
        
        ![docker save image as tar, Docker 4: Container and Saving | by Sik-Ho Tsang  | Medium - vertaistaiteilijat.fi](https://global.discourse-cdn.com/docker/original/3X/6/2/6293e55b8c9fa0a322d538b8899658b8a85875af.png align="left")
        

**Please, feel free to drop any questions in the comments below. I would be happy to answer them.**

**If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**

**\_ Thank you for reading**

**\_sandhya kumari**