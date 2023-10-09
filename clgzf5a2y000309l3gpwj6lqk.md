---
title: "Kubeweek Challenge(Day4)"
datePublished: Thu Apr 27 2023 17:48:40 GMT+0000 (Coordinated Universal Time)
cuid: clgzf5a2y000309l3gpwj6lqk
slug: kubeweek-challengeday4
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682619699961/ba65a988-6b03-4fbd-86b8-d6d997aef1ca.png
tags: kubernetes, devops, orchestration, kubeweek, kubeweekchallenge

---

# Services and Service Discovery

### **Kubernetes Services :**

Kubernetes Services are an essential part of managing containerized applications in a Kubernetes cluster. A Service provides a stable network endpoint for a set of Pods in a Kubernetes cluster, enabling other services to access the applications running in those Pods. In this answer, we will dive deep into Kubernetes Services and cover the following topics:

1. What is a Kubernetes Service?
    
2. Types of Kubernetes Services
    
3. How Kubernetes Services work
    
4. Kubernetes Service configurations
    
5. Service discovery
    
6. Load balancing
    
7. Scaling Kubernetes Services
    
8. Headless Services
    
9. Kubernetes Service and DNS
    
10. Kubernetes Service vs Ingress
    

Let's get started!

## **1\. What is a Kubernetes Service?**

A Kubernetes Service is an abstraction layer that provides a stable IP address and DNS name for a set of Pods in a Kubernetes cluster. It acts as a load balancer for network traffic and enables communication between different components of a Kubernetes application.

## **2\. Types of Kubernetes Services**

There are three types of Kubernetes Services:

### **ClusterIP**

A ClusterIP Service exposes a set of Pods on a cluster-internal IP address. This type of Service is only accessible within the cluster, and other services can access it using the Service's DNS name.

### **NodePort**

A NodePort Service exposes a set of Pods on a static port on each Node in the cluster. This type of Service is accessible from outside the cluster, and the Service is accessible on each Node's IP address on the static port.

### **LoadBalancer**

A LoadBalancer Service exposes a set of Pods through an external load balancer. This type of Service is typically used in cloud environments where an external load balancer can be created automatically to distribute traffic to the Service.

## **3\. How Kubernetes Services work**

When you create a Service, Kubernetes assigns it a virtual IP address (ClusterIP) or static port (NodePort) that acts as a stable endpoint for the Service. The Service monitors the Pods that are associated with it and creates an Endpoints object that lists the IP addresses of the Pods.

When another component in the cluster wants to communicate with the Service, it uses the Service's DNS name. Kubernetes automatically resolves the DNS name to the virtual IP address or static port of the Service, which in turn forwards the traffic to one of the Pods in the associated Endpoints object.

## **4\. Kubernetes Service configurations**

You can configure a Kubernetes Service using YAML or JSON configuration files. Here's an example of a simple Service configuration:

```yaml
yamlCopy codeapiVersion: v1
kind: Service
metadata:
  name: my-service
spec:
  selector:
    app: my-app
  ports:
    - name: http
      port: 80
      targetPort: 8080
```

In this example, the Service is named "my-service" and selects Pods labelled with "app=my-app". The Service exposes port 80 and forwards traffic to port 8080 on the Pods.

## **5\. Service discovery**

Kubernetes Services use DNS for service discovery. When you create a Service, Kubernetes creates a DNS entry for it in the form of `<service-name>.<namespace>.svc.cluster.local`. This DNS name resolves to the virtual IP address of the Service, allowing other components in the cluster to access the Service using its DNS name.

Here is an example YAML file that demonstrates how to create a Kubernetes Service with discovery:

```yaml
yamlCopy codeapiVersion: v1
kind: Service
metadata:
  name: my-service
spec:
  selector:
    app: my-app
  ports:
    - name: http
      port: 80
      targetPort: 8080
```

In this example, the YAML file creates a Service named "my-service" with a selector of "app: my-app", which means it will target all the Pods with a label of "app=my-app". The Service listens on port 80 and forwards traffic to the Pods on port 8080.

You can use this Service to discover the Pods that are associated with it. For example, you could create a Pod that runs a command to query the DNS of the Service:

```yaml
yamlCopy codeapiVersion: v1
kind: Pod
metadata:
  name: my-pod
spec:
  containers:
    - name: my-container
      image: nginx
      command: ["sh", "-c", "nslookup my-service"]
```

In this example, the YAML file creates a Pod named "my-pod" that runs a command to query the DNS of the Service named "my-service". When you run this Pod, it will output the IP addresses of the Pods that are associated with the Service.

Another way to discover Services in Kubernetes is to use environment variables. When you create a Service, Kubernetes automatically creates environment variables for each Pod in the same namespace that include the IP address and port number of the Service. For example, you could create a Deployment that sets the environment variables for a container:

```yaml
yamlCopy codeapiVersion: apps/v1
kind: Deployment
metadata:
  name: my-deployment
spec:
  selector:
    matchLabels:
      app: my-app
  replicas: 2
  template:
    metadata:
      labels:
        app: my-app
    spec:
      containers:
        - name: my-container
          image: nginx
          env:
            - name: MY_SERVICE_HOST
              value: my-service
            - name: MY_SERVICE_PORT
              value: "80"
```

In this example, the YAML file creates a Deployment named "my-deployment" with two replicas. The Deployment sets environment variables for a container that includes the host and port of the Service named "my-service". You can use these environment variables to access the Service from within the container.

## **6\. Load balancing**

Kubernetes Services act as load balancers for network traffic. When a component in the cluster wants to access a Service, it sends a request to the Service's virtual IP address or a static port. The Service forwards the traffic to one of the Pods in its associated Endpoints object using a round-robin load balancing algorithm.

Here is an example YAML file that demonstrates how to create a LoadBalancer Service in Kubernetes:

```yaml
yamlCopy codeapiVersion: v1
kind: Service
metadata:
  name: my-loadbalancer
spec:
  type: LoadBalancer
  selector:
    app: my-app
  ports:
    - name: http
      port: 80
      targetPort: 8080
```

In this example, the YAML file creates a Service named "my-load balancer" with a type of "LoadBalancer". The Service is defined with a selector of "app: my-app", which means it will target all the Pods with a label of "app=my-app". The Service listens on port 80 and forwards traffic to the Pods on port 8080.

When you create a Service with a type of "LoadBalancer", Kubernetes will automatically provision a load balancer in the cloud provider's infrastructure and assign it a public IP address. You can use this IP address to access the Service from outside the cluster.

Note that the exact configuration of the load balancer may depend on the cloud provider you are using. Some cloud providers allow you to specify additional configuration options in the Service YAML file, such as the type of load balancer, the protocol, or SSL termination settings. You can consult the documentation of your cloud provider for more information on how to configure LoadBalancer Services in Kubernetes.

## **7\. Scaling Kubernetes Services**

You can scale a Kubernetes Service by scaling

### \*\*

How to expose Kubernetes workloads to the outside world using Services?\*\*

Kubernetes provides several ways to expose workloads outside of the cluster and make them accessible to users on the internet or other networks.

\&gt;&gt;One way to expose a workload is to use a Service with a type of "LoadBalancer". When you create a Service of this type, Kubernetes automatically provisions a load balancer in the cloud provider's infrastructure and configures it to route traffic to the Service. The load balancer is assigned a public IP address, which can be used by users to access the Service from outside the cluster.

\&gt;&gt;Another way to expose a workload is to use a Service with a type of "NodePort". When you create a Service of this type, Kubernetes allocates a port on each node in the cluster and configures the node's firewall to forward traffic to the Service. Users can access the Service by using the public IP address of any node in the cluster, along with the allocated port number.

\&gt;&gt;A third way to expose a workload is to use an Ingress resource. An Ingress is a Kubernetes resource that defines a set of routing rules for HTTP and HTTPS traffic. You can use an Ingress to expose multiple Services under a single IP address and to configure SSL/TLS termination and other advanced features such as path-based routing.

To use an Ingress, you need to deploy an Ingress controller in your cluster. An Ingress controller is a pod that runs a software application to implement the Ingress rules and manage the routing of traffic. There are several open-source and commercial Ingress controllers available for Kubernetes, including Nginx, Traefik, and Istio.

Overall, Kubernetes provides several options for exposing workloads outside of the cluster and making them accessible to users on the internet or other networks. By using the appropriate method for your needs, you can ensure that your applications are secure, scalable, and reliable.

To expose a Kubernetes workload to the outside world using a Service, you can use a Service with a type of <mark>"LoadBalancer" or "NodePort".</mark>

Here is an example YAML file that demonstrates how to create a Service with a type of "LoadBalancer" to expose a workload:

```yaml
yamlCopy codeapiVersion: v1
kind: Service
metadata:
  name: my-service
spec:
  type: LoadBalancer
  ports:
  - name: http
    port: 80
    targetPort: 8080
  selector:
    app: my-app
```

In this example, the YAML file creates a Service named "my-service" with a type of "LoadBalancer". The Service listens on port 80 and forwards traffic to the Pods with the label "app=my-app" on port 8080. The cloud provider will automatically provision a load balancer and assign it a public IP address, which can be used to access the Service from outside the cluster.

Here is an example YAML file that demonstrates how to create a Service with a type of "NodePort" to expose a workload:

```yaml
yamlCopy codeapiVersion: v1
kind: Service
metadata:
  name: my-service
spec:
  type: NodePort
  ports:
  - name: http
    port: 80
    targetPort: 8080
    nodePort: 30000
  selector:
    app: my-app
```

In this example, the YAML file creates a Service named "my-service" with a type of "NodePort". The Service listens on port 80 and forwards traffic to the Pods with the label "app=my-app" on port 8080. The Service is exposed on port 30000 on each node in the cluster, and users can access the Service using the public IP address of any node in the cluster along with the allocated port number.

Overall, by using YAML files like these to define Services in Kubernetes, you can easily expose your workloads to the outside world and make them accessible to users on the internet or other networks.

### Kubernetes DNS

Kubernetes DNS (Domain Name System) is a built-in DNS service that provides service discovery for Kubernetes Services and Pods. It allows components in a Kubernetes cluster to discover and communicate with each other using DNS names instead of IP addresses.

## **Kubernetes DNS for Services**

When you create a Kubernetes Service, Kubernetes automatically creates a DNS entry for it in the form of `<service-name>.<namespace>.svc.cluster.local`. This DNS entry resolves to the virtual IP address of the Service, which acts as a stable endpoint for the Service. Other components in the cluster can access the Service using its DNS name.

For example, if you have a Service named "my-service" in the "default" namespace, its DNS name would be "my-service.default.svc.cluster.local". Other components in the cluster can access the Service using this DNS name.

## **Kubernetes DNS for Pods**

Kubernetes also provides DNS entries for Pods. When you create a Pod, Kubernetes assigns it a unique hostname in the form of `<pod-name>.<pod-namespace>.pod.cluster.local`. This hostname resolves to the IP address of the Pod.

For example, if you have a Pod named "my-pod" in the "default" namespace, its hostname would be "my-pod.default.pod.cluster.local". Other components in the cluster can access the Pod using its hostname.

## **Configuring Kubernetes DNS**

By default, Kubernetes uses the CoreDNS DNS server to provide DNS services for the cluster. You can configure CoreDNS using a ConfigMap. Here's an example of a simple CoreDNS configuration:

```yaml
yamlCopy codeapiVersion: v1
kind: ConfigMap
metadata:
  name: coredns
  namespace: kube-system
data:
  Corefile: |
    .:53 {
        errors
        health
        kubernetes cluster.local in-addr.arpa ip6.arpa {
          pods insecure
          upstream
          fallthrough in-addr.arpa ip6.arpa
        }
        prometheus :9153
        forward . /etc/resolv.conf
        cache 30
        loop
        reload
        loadbalance
    }
```

In this example, the core file defines a DNS server that listens on port 53 and forwards DNS requests to the Kubernetes DNS service. The Kubernetes DNS service resolves DNS names for Kubernetes Services and Pods. The configuration also includes settings for health checks, Prometheus metrics, caching, and load balancing.

## **Summary**

Kubernetes DNS provides service discovery for Kubernetes Services and Pods using DNS names. It allows components in a Kubernetes cluster to communicate with each other using DNS names instead of IP addresses. Kubernetes uses the CoreDNS DNS server to provide DNS services for the cluster, and you can configure CoreDNS using a ConfigMap.

### **What objects get DNS records?**

In Kubernetes, DNS records are automatically created for several types of objects, including Services, Pods, and Endpoints.

When you create a Service in Kubernetes, a DNS record is automatically created with the format `<service-name>.<namespace>.svc.cluster.local`. This DNS record maps to the IP address of the Service, and can be used by other components in the cluster to access the Service.

Each Pod in Kubernetes is also assigned a unique hostname and IP address, and a DNS record is automatically created for the Pod with the format `<pod-name>.<pod-namespace>.pod.cluster.local`. This hostname can be used by other components in the cluster to access the Pod.

When you create an Endpoint object in Kubernetes, which represents a set of network endpoints that implement a Service, a DNS record is automatically created with the format `<service-name>.<namespace>.svc.cluster.local`. This DNS record maps to the IP addresses of the endpoints.

In addition to these objects, custom DNS records can also be created to map domain names to IP addresses or to provide hostname resolution for specific resources in the cluster. This can be useful when you have multiple Services or Pods that need to be accessed using a single domain name.

Overall, DNS records play a crucial role in enabling service discovery and hostname resolution within the cluster. By using DNS records effectively, you can simplify communication between components in your Kubernetes cluster and provide a consistent and reliable experience for users.

DNS records play an important role in Kubernetes because they provide a mechanism for discovering and accessing resources in the cluster. In Kubernetes, DNS records are used to map service names to IP addresses and to provide hostname resolution for Pods.

## **Service DNS Records**

When you create a Kubernetes Service, a DNS record is automatically created for it. The DNS record is of the form `<service-name>.<namespace>.svc.cluster.local`, where `<service-name>` is the name of the Service, `<namespace>` is the namespace the Service is in and `svc.cluster.local` is the default domain used by Kubernetes. This DNS record maps to the IP address of the Service.

For example, if you have a Service named "my-service" in the "default" namespace, its DNS record would be "my-service.default.svc.cluster.local". Other components in the cluster can access the Service using this DNS name.

## **Pod DNS Records**

Each Pod in Kubernetes is assigned a unique hostname and IP address. The hostname is of the form `<pod-name>.<pod-namespace>.pod.cluster.local`, where `<pod-name>` is the name of the Pod, `<pod-namespace>` is the namespace the Pod is in and `pod.cluster.local` is the default domain used by Kubernetes. This hostname can be used by other components in the cluster to access the Pod.

For example, if you have a Pod named "my-pod" in the "default" namespace, its hostname would be "my-pod.default.pod.cluster.local". Other components in the cluster can access the Pod using this hostname.

## **Custom DNS Records**

In addition to the default DNS records created by Kubernetes, you can also create custom DNS records to map domain names to IP addresses or to provide hostname resolution for specific resources in the cluster. This can be useful when you have multiple Services or Pods that need to be accessed using a single domain name.

To create a custom DNS record in Kubernetes, you can create a ConfigMap with the desired DNS configuration and mount it as a volume in your Pods. The ConfigMap can contain DNS entries in the form of `<hostname>: <ip-address>`, where `<hostname>` is the hostname to map and `<ip-address>` is the IP address to map it to.

## **Summary**

DNS records in Kubernetes play a crucial role in enabling service discovery and hostname resolution within the cluster. Service DNS records map service names to IP addresses, while Pod DNS records provide hostname resolution for Pods. Custom DNS records can also be created to map domain names to IP addresses or to provide hostname resolution for specific resources in the cluster. By using DNS records effectively, you can simplify communication between components in your Kubernetes cluster.

### **Pod:**

In Kubernetes, a pod is the smallest and simplest unit in the Kubernetes object model, which represents a single instance of a running process in the cluster. A pod can contain one or more containers that share the same network namespace and can communicate with each other via the local host.

Pods are designed to be ephemeral and can be created, deleted, and replaced at any time. Kubernetes uses pods to deploy and manage containerized applications and services. By grouping one or more containers in a pod, Kubernetes provides a simple and efficient way to manage and orchestrate containerized applications.

Each pod in Kubernetes has a unique IP address, and it can be exposed to the network using a service. Pods are typically deployed and managed by higher-level Kubernetes objects, such as ReplicaSets, Deployments, and StatefulSets, which provide additional features for scaling, self-healing, and managing the lifecycle of the pods.

### **A Records:**

"A records" refer to the DNS records that map a domain name to an IPv4 address. Pods in Kubernetes do not have A records as they do not have a stable IP address. Instead, each pod in Kubernetes is assigned a unique IP address within the cluster's network.

When a pod is created, it is assigned an IP address from the cluster's PodCIDR range. This IP address is used to communicate with other pods and services within the same Kubernetes cluster. However, this IP address is not stable and can change if the pod is rescheduled to a different node or deleted and recreated. Therefore, it is not recommended to use the pod's IP address directly for communication.

To enable communication with pods, Kubernetes provides a service abstraction that exposes a stable IP address and DNS name for a set of pods. A service is associated with one or more pods using a selector and can be accessed using the service's DNS name or IP address.

In summary, pods in Kubernetes do not have A records, but they are assigned a unique IP address that is used for internal communication within the cluster. Services provide a stable IP address and DNS name for accessing pods in Kubernetes.

### **Pod’s Hostname and Subdomain Fields :**

In Kubernetes, a pod's `hostname` and `subdomain` fields are used to set the hostname and subdomain for the pod's containers.

The `hostname` field specifies the hostname for the pod. If the `hostname` field is not set, Kubernetes will automatically generate a hostname for the pod using the pod name as the prefix and a random string as the suffix.

The `subdomain` field specifies the subdomain for the pod. This field is used to create a fully qualified domain name (FQDN) for the pod. The FQDN is created by concatenating the pod name, the `subdomain` field, and the cluster's default domain name. For example, if the `subdomain` field is set to "web" and the cluster's default domain name is "cluster. local", the FQDN for the pod will be "pod name.web.cluster.local".

The `hostname` and `subdomain` fields can be useful for configuring applications that require a specific hostname or FQDN to function properly. They can also be used to enable service discovery within the cluster by providing a predictable hostname or FQDN for other pods or services to connect to.

It's worth noting that the `hostname` and `subdomain` fields are only used for internal DNS resolution within the cluster. They do not affect external DNS resolution or the pod's IP address.

### **Pod's DNS Policy:**

In Kubernetes, a pod's DNS policy determines how the pod's DNS resolution is configured.

There are three DNS policy options available for pods in Kubernetes:

1. `Default` - This is the default DNS policy for pods in Kubernetes. In this policy, the pod inherits the DNS settings from the node it is running on. This means that the pod will use the DNS server(s) configured on the node for DNS resolution.
    
2. `ClusterFirst` - In this DNS policy, Kubernetes sets up a DNS server for the pod to use. The DNS server is located at a well-known IP address (`10.96.0.10`) and is provided by the `kubelet` service. If the pod's DNS query matches a Kubernetes service or a pod with a `hostname` in the same namespace, the DNS server returns the corresponding IP address. Otherwise, the DNS server forwards the query to the upstream DNS server(s) configured on the node.
    
3. `None` - In this DNS policy, the pod has no DNS resolution configured. The pod must be able to communicate with other pods and services using IP addresses only. This DNS policy is useful for pods that do not require DNS resolution, or for pods that have custom DNS resolution requirements.
    

The DNS policy can be set at the pod level or at the container level using the `DNS policy` field in the pod or container specification. If the DNS policy is set at the container level, it will override the pod-level DNS policy.

It's important to choose the appropriate DNS policy for your pod based on its DNS

When a pod's DNS policy is set to "ClusterFirstWithHostNet", the pod's DNS resolution is configured to use the node's DNS resolver, and the pod shares the network namespace with the node. This means that the pod can access the node's [localhost](http://localhost) interface and services running on the node's host network.

Here is an example YAML manifest for a pod with the `dnsPolicy` set to "ClusterFirstWithHostNet":

```yaml
yamlCopy codeapiVersion: v1
kind: Pod
metadata:
  name: my-pod
spec:
  dnsPolicy: ClusterFirstWithHostNet
  hostNetwork: true
  containers:
  - name: my-container
    image: my-image
```

In this example, the `dnsPolicy` is set to "ClusterFirstWithHostNet", and the `hostNetwork` field is set to `true`. This allows the pod to share the network namespace with the node and use the node's DNS resolver.

If the pod's DNS query matches a Kubernetes service or a pod with a `hostname` in the same namespace, the Kubernetes DNS server will return the corresponding IP address. Otherwise, the DNS query is forwarded to the node's DNS resolver.

Using the "ClusterFirstWithHostNet" DNS policy is useful for certain types of workloads that require access to services running on the node's host network or need to resolve DNS queries using the node's DNS resolver. However, it can also introduce security risks, so it should be used with caution.

### **Pod's DNS Config:**

In Kubernetes, a pod's DNS configuration determines how DNS resolution is configured for the pod. This configuration can be used to customize the DNS settings for the pod and can be set using the `dnsConfig` field in the pod specification.

The `dnsConfig` field allows you to configure the following DNS settings for the pod:

1. `nameservers` - Specifies a list of IP addresses for DNS servers to use for DNS resolution.
    
2. `searches` - Specifies a list of DNS search domains to use for DNS resolution.
    
3. `options` - Specify a list of DNS options to use for DNS resolution.
    

The `dnsConfig` field can be set at the pod level or at the container level using the `dnsConfig` field in the pod or container specification. If the `dnsConfig` field is set at the container level, it will override the pod-level DNS configuration.

The `dnsConfig` field is useful for customizing DNS resolution for pods that require specific DNS settings or for integrating with external DNS servers or services.

It's worth noting that the `dnsConfig` field is only applicable when the pod's DNS policy is set to `ClusterFirst`. When the DNS policy is set to `Default` or `None`, the pod inherits the DNS settings from the node it is running on, and the `dnsConfig` field is ignored.

Here is an example YAML manifest for a pod with custom DNS settings:

```yaml
yamlCopy codeapiVersion: v1
kind: Pod
metadata:
  name: my-pod
spec:
  dnsPolicy: ClusterFirst
  containers:
  - name: my-container
    image: my-image
    dnsConfig:
      nameservers:
        - 8.8.8.8
        - 8.8.4.4
      searches:
        - mydomain.com
      options:
        - ndots:2
```

In this example, the `dnsPolicy` is set to "ClusterFirst", and the `dnsConfig` field is used to specify custom DNS settings for the container. The `nameservers` field specifies a list of IP addresses for DNS servers to use for DNS resolution. In this case, the container will use Google's public DNS servers. The `searches` field specifies a list of DNS search domains to use for DNS resolution. In this case, the container will search for DNS queries in the "[mydomain.com](http://mydomain.com)" domain. The `options` field specifies a list of DNS options to use for DNS resolution. In this case, the container is configured to perform a DNS lookup with at least two dots in the name before trying to append the search domain.

Custom DNS settings can be useful for pods that require specific DNS configurations or for integrating with external DNS servers or services.

**Please, feel free to drop any questions in the comments below. I would be happy to answer them.**

**If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**

**\_ Thank you for reading**

**\_sandhya kumari**