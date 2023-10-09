---
title: "Kubeweek Challenge(Day2)"
datePublished: Tue Apr 25 2023 18:15:34 GMT+0000 (Coordinated Universal Time)
cuid: clgwl86kj000609l2atuz7xpu
slug: kubeweek-challengeday2
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682446405288/9ae2a4e6-f30d-4f69-8118-25e6ff8ea5f2.jpeg
tags: kubernetes, devops, orchestration, trainwithshubham, kubeweekchallenge

---

# Kubernetes Networking:

# Services, Ingress, Network Policies, DNS, and CNI Plugins.

Kubernetes has become the go-to container orchestration platform for organizations of all sizes. Kubernetes networking is a crucial aspect of managing containerized applications and services in a Kubernetes cluster. It involves the configuration and management of network resources to facilitate communication between containers and services running on different nodes in the cluster.

However, with great power comes great complexity, and networking is one of the most challenging aspects of managing a Kubernetes cluster. In this blog, we will dive deep into Kubernetes networking and explore key concepts such as services, ingress, network policies, DNS, and CNI plugins.

There are several networking options available for Kubernetes, including:

1. **Kubernetes Service**: Kubernetes service is a virtual IP address that provides a stable endpoint for a set of pods. It helps to abstract the underlying network infrastructure and provides a consistent interface for communication between pods.
    
    ![Kubernetes Services Explained | Harness](https://assets-global.website-files.com/622642781cd7e96ac1f66807/62d0ef40f0c56e72d9433cc2_EEcT7vHbhMsp-_2JxvxUN0VLIq2rnBGNlPkya_NoHAoURjfY8zMcjI4m6oSASuGbeW8smf_KNx22WVqE_93zExyRnpFTI-Dm7zh4Es-aVU639xZ4YaZCiwtdI1QDzGfTu6NfDtggB4Qphm8gog.png align="left")
    
    Kubernetes Services provide a stable IP address and DNS name that can be used to access a set of pods running in the cluster. Services abstract away the underlying network details, allowing pods to communicate with each other without needing to know their exact IP addresses or hostnames.
    
    Services can be used to implement load balancing, failover, and service discovery. For example, you can create a Service that load balances traffic across a set of backend pods, ensuring that requests are evenly distributed and that the backend pods can be scaled up or down without impacting the availability of the service.
    
2. **Cluster Networking**: Kubernetes cluster networking is responsible for managing communication between the nodes in the cluster. It includes network policies, routing, and load balancing.
    

![Kubernetes Cluster Networking Components | Pure Storage Blog](https://blog.purestorage.com/wp-content/uploads/2020/02/Picture2.png align="left")

Cluster networking in Kubernetes is responsible for routing traffic between pods running on different nodes in the cluster. Kubernetes provides a default networking implementation called the Kubernetes Container Network Interface (CNI), which allows for the use of various networking plugins.

The CNI allows for a wide range of network policies, including network isolation, port-level security, and traffic shaping. Different networking plugins can be used to implement different networking features, such as load balancing, network segmentation, and packet filtering.

1. **Container Network Interface (CNI)**: The CNI is a specification that defines the interface between the container runtime and the network provider. It allows Kubernetes to use a wide variety of networking solutions, such as Flannel, Calico, and Weave.
    
    ![Kubernetes CNI Explained](https://www.tigera.io/app/uploads/2021/12/K8s-CNI-diagram02.png align="left")
    
    The Container Network Interface (CNI) is a specification that defines how container runtimes interface with the network provider. It allows Kubernetes to use a variety of network providers and plugins, depending on the specific requirements of the application.
    
    <mark>CNI plugins</mark> can provide different types of network topologies, such as overlay networks, host-based networks, and bridge networks. They can also provide advanced features, such as network segmentation, encryption, and traffic shaping.
    
    ![Introduction to Kubernetes Pod Networking - Part 1](https://images.contentstack.io/v3/assets/blt300387d93dabf50e/blt605e7720be3d37fd/5bf6f4bcc812d64628f03c5b/cni-plugin.png align="left")
    
    CNI plugins allow Kubernetes to configure the networking for each pod at runtime. The CNI plugin is responsible for setting up the network interface for each pod and connecting it to the appropriate network. This includes assigning IP addresses, setting up routing tables, and configuring network security policies.
    
    Some of the most popular CNI plugins include Calico, Flannel, Weave Net, and Cilium.
    
2. **Ingress Networking**: Kubernetes Ingress is an API that provides a way to manage external access to services running in a Kubernetes cluster. It allows for the configuration of rules for routing traffic to different services based on hostnames and URLs.
    
    Ingress networking is used to expose HTTP and HTTPS services running in a Kubernetes cluster to the outside world. The Kubernetes Ingress resource provides a way to configure rules for routing traffic from the external network to backend services running in the cluster.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682447677544/51992c89-ed3b-48ac-8570-0e314c758ec2.png align="center")
    
    Ingress can be used to implement complex routing rules, SSL termination, and load balancing. Different ingress controllers can be used to provide different features, such as the ability to route traffic based on URL path or header values, or to provide advanced traffic management features like traffic shaping and rate limiting.
    
3. **Network Policies:** Kubernetes Network Policies are a powerful feature that allows you to control the traffic flow to and from Kubernetes pods. Network Policies are implemented using rules that define what traffic is allowed or denied between pods. This provides a way to enforce security policies and prevent unauthorized access to resources.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682447758965/8de169a7-e2f6-48cf-a941-95a0119fa7c8.png align="center")
    
    Network Policies are defined using a YAML file that specifies the allowed traffic flow between pods. The file contains a list of rules that specify the source and destination pods, protocols, ports, and other parameters. For example, you can create a Network Policy that allows traffic from a specific pod to access a database pod while denying traffic from all other pods.
    
    Network Policies can be applied to a specific namespace or the entire cluster. They are enforced by a network plugin, such as Calico, that intercepts traffic and applies the policy rules. If traffic does not match a rule, it is denied by default.
    
    Network Policies are particularly useful for securing microservices-based architectures, where each service runs in its pod and communicates with other services over the network. By using Network Policies, you can enforce strict security policies and prevent unauthorized access to sensitive data.
    

Here are some common use cases for Network Policies in Kubernetes:

1. **Isolating workloads:** Network policies can be used to isolate different workloads from each other, preventing them from accessing each other's resources.
    
2. **Restricting ingress and egress traffic**: You can use Network Policies to control which pods are allowed to receive traffic from the outside world, or which pods are allowed to send traffic outside of the cluster.
    
3. **Enforcing security policies**: Network policies can be used to enforce security policies, such as limiting access to sensitive services to a specific set of pods, or enforcing encryption and authentication requirements for all network traffic.
    
4. **Enabling compliance requirements**: Network policies can help you meet compliance requirements by ensuring that only authorized traffic flows between pods, and by logging and auditing all network traffic.
    
5. **DNS**: DNS in Kubernetes refers to the Kubernetes DNS service, which provides a way for Kubernetes services to discover and communicate with each other using domain names.
    

When a Kubernetes service is created, a DNS record is automatically created for it in the Kubernetes DNS service. This allows other services in the cluster to refer to the service using its DNS name instead of its IP address, which can change frequently.

![Logical Shift: External DNS For Kubernetes Services](https://3.bp.blogspot.com/-0fFfzfGO9FU/XROw0x26uKI/AAAAAAAAANM/I-A4dKhXneUE7XqYXMitnggRjI_ljutxwCPcBGAYYCw/s1600/Screen%2BShot%2B2019-06-26%2Bat%2B10.52.05%2BAM.png align="left")

The Kubernetes DNS service also provides name resolution for Kubernetes pods, which are the smallest deployable units in a Kubernetes cluster. Each pod is assigned a unique hostname, and the Kubernetes DNS service maintains a mapping of each pod's hostname to its IP address.

Overall, the Kubernetes DNS service simplifies communication between services and pods in a Kubernetes cluster by providing a consistent and reliable way to refer to them using domain names.

In summary, Kubernetes networking is a complex topic that requires careful consideration of the specific requirements of your application. The different networking options available in Kubernetes provide a wide range of features that can be used to implement different types of networking topologies and advanced network policies. The specific networking options that you choose will depend on your specific requirements, such as the need for load balancing, security, or traffic shaping.

**Please, feel free to drop any questions in the comments below. I would be happy to answer them.**

**If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**

**\_ Thank you for reading**

**\_sandhya kumari**