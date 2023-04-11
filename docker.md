<p style="text-align:center;"><img title="a title" alt="Alt text" src="/docker-resources/docker-logo-small.jpeg"></p?>
<p style="text-align:center;"><img title="a title" alt="Alt text" src="/docker-resources/docker-architecture.svg"></p?>

# Docker on PlayPen                         

## What are Containers 

Containers are a way of packaging software in a way that allows it to run consistently across different environments, such as a developer's laptop, a testing environment, or a production server. Containers allow you to isolate an application and its dependencies into a self-contained unit that can be easily deployed, managed, and scaled.

Containers are built on top of operating system-level virtualization, which allows multiple containers to share a single operating system kernel, while still providing a high degree of isolation between containers. This makes containers much more lightweight than virtual machines, which require a separate operating system to be installed for each virtual machine.

Each container includes all of the dependencies needed to run the application, such as libraries, runtime environments, and system tools. This allows the application to run consistently across different environments, without requiring any changes to the underlying system.

Containers are typically created using containerization platforms, such as Docker, which provide tools for building, running, and managing containers. These platforms allow you to package your application and its dependencies into a container image, which can then be easily deployed and scaled as needed.

Overall, containers provide a lightweight, portable, and consistent way to package and deploy applications, making them an ideal solution for modern application development and deployment.

## Containers vs Virtual Machines 

Containers and virtual machines are both ways of abstracting and isolating applications from the underlying system, but there are some key differences between the two:

* **Architecture:** Virtual machines (VMs) use hardware-level virtualization to create a virtualized environment that includes a guest operating system and any necessary dependencies. Containers, on the other hand, use operating system-level virtualization to create a lightweight, isolated environment that shares the host operating system kernel.

* **Resource Usage:** VMs require a full operating system to be installed for each virtual machine, which can be resource-intensive and result in significant overhead. Containers, on the other hand, share the underlying host operating system, which makes them much more lightweight and efficient in terms of resource usage.

* **Portability:** VMs are typically less portable than containers because they require a complete operating system to be installed, which can make them more difficult to move between different environments. Containers, on the other hand, are designed to be portable, since they include only the dependencies needed to run the application and can be easily moved between different environments.

* **Management:** VMs require a hypervisor to manage the virtualized environment, which can add complexity to the management of virtual machines. Containers, on the other hand, are managed through containerization platforms like Docker, which provide tools for building, running, and managing containers.

Overall, containers are a more lightweight, efficient, and portable way of packaging and deploying applications than virtual machines, making them an ideal solution for modern application development and deployment. However, virtual machines still have their place in certain scenarios, such as when multiple operating systems or hardware environments are needed.