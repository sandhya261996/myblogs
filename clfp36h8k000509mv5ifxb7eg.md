---
title: "DevOps90DaysChalleneg"
datePublished: Sun Mar 26 2023 07:36:16 GMT+0000 (Coordinated Universal Time)
cuid: clfp36h8k000509mv5ifxb7eg
slug: devops90dayschalleneg
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679816008144/60dd5c76-c62c-474c-bc8b-730a9cd7a9ed.jpeg
tags: docker, python, django, automation, devops

---

# Hi 👋there,

# Now we are on the Day 17 task

# **Docker for DevOps Engineers**

<mark>Checkout the below link for Day 17 task:</mark>

[https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day17/tasks.md](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day17/tasks.md)

For this, you first need an AWS EC2 instance of your own choice.

Here is my blog on creating an AWS EC2 instance :

<mark>Checkout the below link for Provisioning your first EC2 Instance</mark>

[https://progressivecoder.com/step-by-step-process-to-launch-aws-ec2-instance/](https://progressivecoder.com/step-by-step-process-to-launch-aws-ec2-instance/)

Once you are done with creating an EC2 instance you need to SSH into it.

Now you need to install the docker Engine in your server. <mark>Checkout the below link</mark>

[https://www.zehncloud.com/how-to-install-docker-on-amazon-ec2-instance/](https://www.zehncloud.com/how-to-install-docker-on-amazon-ec2-instance/)

Below are the steps that we will be going to perform in the process:

1. Install Git and clone the repo of the react-python Django web application
    
2. Install Docker
    
3. Create and configure a Dockerfile
    
4. Build a Docker image
    
5. Create and run a Docker container
    
6. Access it
    
    # **Install git and Clone the repo of the Python Django application**
    

Open the instance, first, you need to install Git in it so that we can clone the application repository from GitHub(VCS). Use command :

```bash
sudo apt install git
```

```bash
git clone https://github.com/sandhya261996/react_django_demo_app.git
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679812842176/89ab5c03-0084-48cc-bb75-34a7181b8950.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679812894593/3f030351-4b15-4402-adad-7cad82c886d6.png align="center")

# **2\. Install Docker**

Install Docker in the machine using the command :

```bash
sudo apt install docker -y
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679813084744/b167041f-68c2-444d-b01e-5bb9517cd33b.png align="center")

Now check the version of the docker and start the docker and check the status of the docker to know if it is running using the below commands :

```bash
docker -v 
systemctl start docker
systemctl status docker
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679813262165/8928fc92-7713-47b8-9147-c58082bbf283.png align="center")

# **3\. Create and configure a Dockerfile**

Now we will create and configure a docker file as per the requirement of the Node.js application. Change the directory to the cloned project and create Dockerfile there.

```bash
FROM python:3.9
WORKDIR app
COPY . /app
RUN pip install -r requirements.txt
EXPOSE 8000
CMD ["python", "manage.py","runserver","0.0.0.0:8000"]
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679813415312/3b34facb-175a-4b08-9837-4c802736703f.png align="center")

# **4\. Build a Docker image**

Now before starting the build process check if there is any existing container running with the same name.

```bash
sudo docker ps
sudo docker ps -a
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679813731168/5b408dd3-be28-4551-9cec-91a7287512a0.png align="center")

# **5\. Create and run a Docker container**

Using the image that has been built we will create a container out of it and run it:

Use the below commands :

```bash
sudo docker run -d --name python-django-app -p 8000:8000 django_app:latest
```

You can see a container running here that can be accessed on port 8000 as we have done the port mapping on port 8000.

# **6\. Access it**

Now you can take the public IP of the machine and port 8000 to access the application.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679814948244/313620e2-37a6-4bd9-b59e-0c8c8c7dd308.png align="center")

# **7\. Pushing the image on DockerHub**

We have already created a Docker image using the Dockerfile. Check all the images present by using the command.

```bash
sudo docker images
```

Now we will log in in to the DockerHub by adding the command:

```bash
sudo Docker login
```

Put your username and password here. If the login is successful, then you will get a message like **Login Succeeded**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679815303161/4d68babb-3fec-4cfe-9698-f1494ef1e87a.png align="center")

Now tag the locally created image to the docker hub. This means we have to tag the image with the docker hub username.

```bash
sudo docker tag django_app:latest sandhyakumari1996/django_app:latest
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679815194985/8f6cb282-9b7c-4441-a2d9-f724476edbf5.png align="center")

Now push the image to the Docker hub using the push command.

```bash
sudo docker push sandhyakumari1996/djnago_app:latest
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679815474792/7f9f0d7c-e2f9-434b-8ff4-391d3092bf16.png align="center")

When it is done, you can check in your Docker hub if it is pushed.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679815588563/762a31fd-8bf7-4dc7-8c1c-0c2d14887da8.png align="center")

**Please, feel free to drop any questions in the comments below. I would be happy to answer them.**

**If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**

**\_ Thank you for reading**

**\_sandhya kumari**