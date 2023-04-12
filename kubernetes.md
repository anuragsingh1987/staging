<p style="text-align:center;"><img title="a title" alt="Alt text" src="/kubernetes-resources/Kubernetes_logo.png"></p?>

## Kubernetes on PlayPen

*Please Note : Though this repository has been created considering users of all levels (beginners, intermediate and experts) , but it is recommended that before using the repo , you should complete a docker course offered by pluralsight which is available to all LGB employees. The course will provide all the required and idepth knowledge about docker and should be supplemented by hands On labs supplied as part of this repo.*

**Here is the course link and description -- > <<Link to  be  added>>**

**Kubernetes (also known as "K8s")** is an open-source container orchestration platform that automates the deployment, scaling, and management of containerized applications. It was developed by Google and is now maintained by the Cloud Native Computing Foundation (CNCF).

Kubernetes is designed to provide a platform for deploying and managing containerized applications across a cluster of machines. It automates the processes of container orchestration, such as scheduling containers to run on specific nodes, scaling containers up or down based on demand, and managing container health and availability.

Kubernetes provides a rich set of features for managing containers, including load balancing, service discovery, automatic failover, and rolling updates. It can be used with a variety of container runtimes, including Docker, and can run on any infrastructure, including public clouds, private clouds, and bare-metal servers.

Kubernetes has become the de facto standard for container orchestration, and is widely used in production environments to run large-scale, distributed applications.

## Kubernetes Vs Docker Swarm

**Kubernetes and Docker Swarm** are two popular container orchestration platforms that enable the management of containerized applications at scale. While they share some similarities, there are also some significant differences between them.

Here are some key differences between Kubernetes and Docker Swarm:

 - **Architecture:** Kubernetes has a more complex architecture, with multiple components and a more modular design, while Docker Swarm has a simpler architecture with fewer components.

 - **Scaling:** Kubernetes has a more powerful and flexible scaling mechanism than Docker Swarm, allowing for automatic scaling based on resource usage, custom metrics, or user-defined policies.

 - **Networking:** Kubernetes has a more sophisticated networking model, including support for multiple network plugins and advanced networking features such as service discovery and load balancing. Docker Swarm has a simpler networking model that supports only a single network driver.

 - **Storage:** Kubernetes has a more robust storage model, with support for various storage plugins and features such as dynamic provisioning, snapshotting, and cloning. Docker Swarm has a more limited storage model, with support for only a few storage plugins.

 - **Community:** Kubernetes has a larger and more active community than Docker Swarm, with a wider range of third-party tools and integrations.

In summary, Kubernetes is a more powerful and flexible platform, with a more complex architecture and advanced features such as networking and storage. Docker Swarm, on the other hand, is a simpler and more lightweight platform, with a focus on ease of use and simplicity. The choice between the two depends on the specific requirements of your application and your organization's technical expertise and resources.

## Kubernetes architecture

<p style="text-align:center;"><img title="a title" alt="Alt text" src="/kubernetes-resources/components-of-kubernetes.svg"></p?>

**Kubernetes architecture** is composed of several components that work together to provide a platform for deploying and managing containerized applications. The main components of the Kubernetes architecture are:

**Control plane:** The control plane is responsible for managing the overall state of the cluster. It includes several components that work together to schedule and manage containers, and to provide services to the cluster.

-   **API server:** The API server is the main management component of the control plane. It provides a RESTful API for interacting with the Kubernetes cluster.
-   **etcd:** etcd is a distributed key-value store used to store the configuration data of the cluster, such as the state of nodes and containers.
-   **Controller Manager:** The Controller Manager watches the state of the cluster and ensures that the desired state is maintained.
-   **Scheduler:** The scheduler assigns containers to nodes based on resource availability and other constraints.

**Nodes:** Nodes are the worker machines in the Kubernetes cluster that run containers. Each node runs a container runtime, such as Docker or rkt, and the Kubernetes agent, called the kubelet.

-   **Kubelet:** The Kubelet is responsible for managing the containers running on a node and reporting their status to the control plane.
-   **Container runtime:** The container runtime is responsible for running containers on the node.

3.  **Networking:** Networking is a critical component of Kubernetes, as it enables communication between containers and services within the cluster. Kubernetes uses a software-defined networking (SDN) approach to networking, which allows containers to communicate with each other across the cluster.

-   **Service proxy:** The service proxy is responsible for load balancing traffic between containers and services.
-   **Network plugin:** The network plugin provides networking capabilities to the cluster, such as virtual networks and IP address management.

Overall, the Kubernetes architecture provides a highly scalable and fault-tolerant platform for deploying and managing containerized applications.