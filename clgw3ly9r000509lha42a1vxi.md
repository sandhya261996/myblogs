---
title: "Kubeweek Challenge(Day1)"
datePublished: Tue Apr 25 2023 10:02:24 GMT+0000 (Coordinated Universal Time)
cuid: clgw3ly9r000509lha42a1vxi
slug: kubeweek-challengeday1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682412497978/50f609dd-ec0a-4257-95ab-fef070c8d3d2.png
tags: kubernetes, orchestration, kubernetes-container, kubernetes-architecture, kuberweekchallenge-day1

---

### **K*ubernetes Architecture and Components, Kubernetes Installation and Configuration.***

### **<mark>K</mark>*<mark>ubernetes Architecture and Components</mark>***

Kubernetes architecture is designed as a distributed system that spans across multiple nodes, where each node is an instance of the Kubernetes cluster. The architecture can be divided into two main components: the control plane and the worker nodes.

1. <mark>Control Plane Components:</mark>
    

a. API Server: It provides a RESTful API for communication with the Kubernetes cluster. The API server is responsible for validating and processing requests and updating the state of the Kubernetes cluster.

b. etcd: It is a distributed key-value store that stores the configuration data and the state of the Kubernetes cluster. It is used as the backend data store for Kubernetes.

c. Controller Manager: It is responsible for managing various controllers that are responsible for maintaining the desired state of the Kubernetes cluster. It detects changes in the cluster and takes corrective actions to bring the cluster back to the desired state.

d. Scheduler: It is responsible for scheduling pods on the worker nodes based on resource availability, constraints, and other policies. It ensures that pods are scheduled to the right nodes.

1. <mark>Worker Nodes:</mark>
    

a. Kubelet: It is responsible for managing the lifecycle of pods on a node. It communicates with the API server to get the configuration of the pods assigned to the node and ensures that the pods are running as expected.

b. Container Runtime: It is responsible for running the containers inside the pods. Kubernetes supports several container runtimes, including Docker, containers, and CRI-O.

c. kube-proxy: It is responsible for providing networking services to the pods running on the node. It forwards traffic to the appropriate pod based on the IP address and port number.

d. Pod: A pod is the smallest unit of deployment in Kubernetes. It is a logical host for one or more containers and can be scheduled on a worker node. A pod can share network, storage, and other resources with other pods running on the same node.

Overall, the architecture of Kubernetes is designed to be highly scalable, fault-tolerant, and flexible. It allows users to deploy and manage containerized applications on a large scale while providing a simple and consistent interface to the developers.

### **<mark>Kubernetes Installation and Configuration.</mark>**

Here are the steps to install and configure Kubernetes on an EC2 instance:

Step 1: Launch EC2 Instance

a.) First, launch an EC2 instance. You can use the Amazon Linux AMI or any other Linux distribution that you prefer.

* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676358475865/a508b76f-f05e-4c61-b1e8-f3334e98a17c.png?auto=compress,format&format=webp align="left")
    

b.) Make sure that the instance has at least 2GB of RAM and 2 CPUs.(t2.medium)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676358498146/6adadf87-e5f7-460e-b2ff-ef1d1013591d.png?auto=compress,format&format=webp align="left")

sudo yum update

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676359628528/6adb7f2d-eaf2-43a6-8a0c-a2a68ab8c2d7.png?auto=compress,format&format=webp align="left")

Step 2: Install Docker

* Install Docker on the EC2 instance using the following command: `sudo yum install -y docker`
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676359734576/61815e37-1e47-4474-81b0-01480f926cbc.png?auto=compress,format&format=webp align="left")
    

Step 3: Install Kubernetes

* Add the Kubernetes repository to the EC2 instance using the following command: `sudo vi /etc/yum.repos.d/kubernetes.repo`
    
* Add the following lines to the file:
    
* Install Kubernetes using the following command: `sudo yum install -y kubelet kubeadm kubectl`
    
* Start the Kubernetes services using the following command: `sudo systemctl enable kubelet && sudo systemctl start kubelet`
    

Step 4: Configure Kubernetes

* Initialize the Kubernetes cluster using the following command: `sudo kubeadm init`
    
* Copy the kubeconfig file to your home directory using the following command: `mkdir -p $HOME/.kube && sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config && sudo chown $(id -u):$(id -g) $HOME/.kube/config`
    
* Install the Kubernetes network add-on using the following command: `sudo kubectl apply -f` [`https://docs.projectcalico.org/v3.8/manifests/calico.yaml`](https://docs.projectcalico.org/v3.8/manifests/calico.yaml)
    

Step 5: Join Nodes in the Cluster

* If you want to join additional nodes to the Kubernetes cluster, run the join command that was provided by the Kubeadm init command on each node.
    

That's it! You now have a Kubernetes cluster running on your EC2 instance.

### ***Installation and Configuration minikube.***

step: 1 `curl -LO` [`https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64`](https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64) `sudo install minikube-linux-amd64 /usr/local/bin/minikube`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676360752436/f00d6e42-3d92-4cf6-a281-f14c9e14d2d8.png?auto=compress,format&format=webp align="left")

step: 2 Use minikube start --driver=docker

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676361111276/32d288fb-3d0f-46ce-8929-032060e25f0c.png?auto=compress,format&format=webp align="left")

sudo usermod -aG docker $USER && newgrp docker

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676361325728/640cfa4d-5d53-4a60-959e-ae269f839fb7.png?auto=compress,format&format=webp align="left")

minikube ssh

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676361706979/c36694f3-3ee1-43e5-befa-45e98024dbba.png?auto=compress,format&format=webp align="left")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676361798213/2d06268d-09f7-4233-9fb6-b2e0a7f5c935.png?auto=compress,format&format=webp align="left")

sudo snap install kubectl --classic

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676361854502/aaab9007-8706-4e22-9a29-a719b9f19936.png?auto=compress,format&format=webp align="left")

**Please, feel free to drop any questions in the comments below. I would be happy to answer them.**

**If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**

**\_ Thank you for reading**

**\_sandhya kumari**