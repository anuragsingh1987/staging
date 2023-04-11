<p style="text-align:center;"><img title="a title" alt="Alt text" src="/docker-resources/docker-logo-small.jpeg"></p?>

# Docker on PlayPen

*Please Note : Though this repository has been created considering users of all levels (beginners, intermediate and experts) , but it is recommended that before using the repo , you should complete a docker course offered by pluralsight which is available to all LGB employees. The course will provide all the required and idepth knowledge about docker and should be supplemented by hands On labs supplied as part of this repo.*

**Here is the course link and description -- >   <<Link to be added>>**


## What are Containers

**Containers** are a way of packaging software in a way that allows it to run consistently across different environments, such as a developer's laptop, a testing environment, or a production server. Containers allow you to isolate an application and its dependencies into a self-contained unit that can be easily deployed, managed, and scaled.

Containers are built on top of operating system-level virtualization, which allows multiple containers to share a single operating system kernel, while still providing a high degree of isolation between containers. This makes containers much more lightweight than virtual machines, which require a separate operating system to be installed for each virtual machine.

Each container includes all of the dependencies needed to run the application, such as libraries, runtime environments, and system tools. This allows the application to run consistently across different environments, without requiring any changes to the underlying system.

Containers are typically created using containerization platforms, such as Docker, which provide tools for building, running, and managing containers. These platforms allow you to package your application and its dependencies into a container image, which can then be easily deployed and scaled as needed.

Overall, containers provide a lightweight, portable, and consistent way to package and deploy applications, making them an ideal solution for modern application development and deployment.

## Containers vs Virtual Machines

Containers and virtual machines are both ways of abstracting and isolating applications from the underlying system, but there are some key differences between the two:

- **Architecture:** Virtual machines (VMs) use hardware-level virtualization to create a virtualized environment that includes a guest operating system and any necessary dependencies. Containers, on the other hand, use operating system-level virtualization to create a lightweight, isolated environment that shares the host operating system kernel.

- **Resource Usage:** VMs require a full operating system to be installed for each virtual machine, which can be resource-intensive and result in significant overhead. Containers, on the other hand, share the underlying host operating system, which makes them much more lightweight and efficient in terms of resource usage.

- **Portability:** VMs are typically less portable than containers because they require a complete operating system to be installed, which can make them more difficult to move between different environments. Containers, on the other hand, are designed to be portable, since they include only the dependencies needed to run the application and can be easily moved between different environments.

- **Management:** VMs require a hypervisor to manage the virtualized environment, which can add complexity to the management of virtual machines. Containers, on the other hand, are managed through containerization platforms like Docker, which provide tools for building, running, and managing containers.

Overall, containers are a more lightweight, efficient, and portable way of packaging and deploying applications than virtual machines, making them an ideal solution for modern application development and deployment. However, virtual machines still have their place in certain scenarios, such as when multiple operating systems or hardware environments are needed.

## Docker Architecture

<p style="text-align:center;"><img title="a title" alt="Alt text" src="/docker-resources/docker-architecture.svg"></p?>

The architecture of Docker consists of several components that work together to enable containerization:

- **Docker daemon:** The Docker daemon is the core component of the Docker architecture. It is responsible for managing the Docker objects such as images, containers, networks, and volumes. The daemon runs on the host machine and interacts with the Docker CLI and other components to perform container-related operations.

- **Docker client:** The Docker client is a command-line tool that allows users to interact with the Docker daemon. Users can use the Docker client to build, manage, and deploy Docker containers on their host machine.

- **Docker registries:** Docker registries are used to store Docker images. A Docker image is a lightweight, standalone, executable package that includes everything needed to run an application, including the code, libraries, and dependencies. Docker registries can be public, such as Docker Hub, or private, such as a registry hosted within an organization.

- **Docker images:** Docker images are templates for creating Docker containers. They contain all the necessary files and dependencies needed to run an application, along with the operating system and other system-level components.

- **Docker containers:** Docker containers are instances of Docker images. They are lightweight and can be easily created and destroyed as needed. Containers are isolated from each other and from the host machine, which provides a high level of security and flexibility.

- **Docker networks:** Docker networks are used to connect containers to each other and to the outside world. They allow containers to communicate with each other and with other services on the same network.

- **Docker volumes:** Docker volumes are used to store data that needs to persist between container restarts. They allow data to be shared between containers and can be backed up or replicated as needed.

Overall, the Docker architecture provides a powerful and flexible platform for containerization, enabling developers to easily create and manage containerized applications with a high level of security and flexibility.

## Installing Docker on a PlayPen Virtual Machine (Ubuntu)

Best way to learn docker is to get your hands dirty , so launch a playpen ( GCP or Azure ) and launch a Virtual Machine with an Ubuntu Image , If you are not sure how to do this , please refer GCP or Azure Tutorials under Incubation Lab.

Here are the basic steps to install Docker on Ubuntu:

Update your system: Before installing Docker, make sure your system is up-to-date by running the following command:

```sql
Copy code
sudo apt update
```

Install the necessary packages: Run the following command to install the packages required for Docker:

```arduino
Copy code
sudo apt install apt-transport-https ca-certificates curl gnupg lsb-release
```

Add Docker GPG key: Run the following command to add the Docker GPG key:

```bash
Copy code
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

Add Docker repository: Run the following command to add the Docker repository:

```bash
Copy code
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

Install Docker: Finally, run the following command to install Docker:

```lua
Copy code
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io
```

Verify Docker installation: After the installation is complete, run the following command to verify that Docker is installed correctly:

```arduino
Copy code
sudo docker run hello-world
```

This will download a test Docker image and run it in a container. If everything is working correctly, you should see a message that says "Hello from Docker!".

That's it! Docker is now installed on your Ubuntu system.

## Getting Started with Docker

**Install Docker:** The first step is to install Docker on your machine.

**Create a Dockerfile:** A Dockerfile is a script that specifies the configuration of a Docker image. Create a new file called Dockerfile in your project directory and add the following lines:

```sql
Copy code
FROM python:3.9-slim-buster
WORKDIR /app
COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt
COPY . .
CMD [ "python3", "app.py" ]
```

This Dockerfile specifies that we're using the Python 3.9 slim-buster image as our base, sets the working directory to /app, installs any dependencies specified in requirements.txt, copies the project files into the container, and sets the command to run the app.py file.

**Build the Docker image:** Run the following command to build the Docker image:

```
docker build -t myapp .
```

This will build a Docker image named myapp based on the instructions in the Dockerfile.

**Run the Docker container:** Run the following command to start a container based on the myapp image:

```arduino
Copy code
docker run -p 5000:5000 myapp
```

This will start a container based on the myapp image and map port 5000 from the container to port 5000 on the host machine.

**Test the app:** Open a web browser and navigate to http://localhost:5000 to test the app running inside the Docker container.

That's it! This is just a simple example of how to use Docker, but it demonstrates the basic workflow for building and running Docker images and containers. There's a lot more you can do with Docker, including deploying containers to a production environment, managing Docker networks and volumes, and more.

---

**Commonly Used Docker Commands**

- `docker run`: This command is used to run a container from a Docker image.

- `docker ps`: This command lists all the running containers.

- `docker images`: This command lists all the Docker images that are currently stored on the system.

- `docker pull`: This command is used to download a Docker image from a registry.

- `docker build`: This command is used to build a Docker image from a Dockerfile.

- `docker stop`: This command is used to stop a running container.

- `docker rm`: This command is used to remove a container.

- `docker rmi`: This command is used to remove a Docker image.

- `docker exec`: This command is used to run a command inside a running container.

- `docker logs`: This command is used to view the logs of a container.

These are just a few of the most commonly used Docker commands. There are many other Docker commands available, depending on your use case. You can view the complete list of commands by running `docker --help`.



## A Simple Docker Challenge 

**Challenge:**
Create a Docker container that runs a simple Node.js web application that displays the current date and time in the browser when accessed. The web application should run on port 8080.

The Docker container should be built using the official Node.js 14 base image and should install the Express framework using npm.

Once the container is built, you should be able to run it with the command "docker run -p 8080:8080 &lt;image-name&gt;" and access the web application by opening a browser and navigating to http://localhost:8080.

**Solution:**

To complete this challenge, follow the steps below:

1. Create a new directory for the project and navigate to it:

```bash
mkdir nodejs-webapp && cd nodejs-webapp
```

2. Create a new file named ```app.js``` and add the following code to it:

```javascript
const express = require('express');
const app = express();

app.get('/', (req, res) =&gt; {
  const now = new Date();
  res.send(`The current time is: ${now.toLocaleString()}`);
});

const PORT = process.env.PORT || 8080;
app.listen(PORT, () =&gt; {
  console.log(`Server running on port ${PORT}`);
});
```

3. Create a new file named ```Dockerfile``` and add the following code to it:

```Dockerfile
FROM node:14

WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .

EXPOSE 8080

CMD ["npm", "start"]

```

4. Build the Docker image:

```docker build -t nodejs-webapp .```

5. Run the Docker container:arduino

```arduino
docker run -p 8080:8080 nodejs-webapp
```

6. Access the web application by opening a browser and navigating to http://localhost:8080.

That's it! You should see the current date and time displayed in the browser. If you want to stop the container, press ```Ctrl+C``` in the terminal.


**Bonus challenge solution:**

To create a multi-stage build, modify the ```Dockerfile``` as follows:

```Dockerfile
FROM node:14 AS build

WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

FROM node:14-alpine

WORKDIR /app
COPY package*.json ./
RUN npm install --production
COPY --from=build /app/dist /app/dist

EXPOSE 8080

CMD ["npm", "start"]
```

In this modified ```Dockerfile```, we first use the ```node:14``` base image to build the application, and then copy only the necessary files into the final image using the ```--from``` flag. This results in a smaller and more efficient image. To build and run the container, use the same commands as before.

---


**Now here is another challenge for you to try**

Create a Docker container that runs a simple Python web application that prints "Hello, World!" to the browser when accessed. The web application should run on port 8080.

The Docker container should be built using the official Python 3.9 base image and should install the Flask framework using pip.

Once the container is built, you should be able to run it with the command "docker run -p 8080:8080 <image-name>" and access the web application by opening a browser and navigating to http://localhost:8080.

To make it more challenging, add a feature to the web application that allows the user to input their name and have the application print "Hello, <name>!" to the browser. Make sure the input is properly validated and sanitized to prevent any security vulnerabilities.

Bonus challenge: Modify the Dockerfile to create a multi-stage build that first installs the necessary dependencies and then copies only the required files into the final image, making the image smaller and more efficient.


---

## Here are some resources you can use to learn Docker:

- **Docker documentation:** The official Docker documentation is a great place to start learning about Docker. It includes a comprehensive guide to Docker and its components, as well as tutorials and examples.

- **Docker Getting Started guide:** This guide provides step-by-step instructions on how to use Docker to build and deploy applications.

- **Docker YouTube channel:** The Docker YouTube channel has a variety of videos and tutorials that cover Docker basics, as well as more advanced topics.

- **Docker Mastery course on Udemy:** This course covers everything you need to know to use Docker effectively, including how to build and deploy applications with Docker.

- **Docker for Developers course on Pluralsight:** This course is aimed at developers and covers how to use Docker to create and deploy applications.

- **Docker Cookbook:** This book provides recipes for using Docker to solve common problems and perform common tasks.

These resources should give you a solid foundation in Docker and help you get started with using it.

---

## Here are some Docker reference materials you can use:

- **Docker documentation:** The official Docker documentation provides detailed information on how to use Docker and its components.

- **Docker Hub:** Docker Hub is a registry of Docker images that you can use as a base for your own images. It also provides a platform for sharing and discovering Docker images.

- **Dockerfile reference:** The Dockerfile reference provides detailed information on how to write Dockerfiles, which are used to build Docker images.

- **Docker Compose documentation:** Docker Compose is a tool for defining and running multi-container Docker applications. The Docker Compose documentation provides information on how to use this tool.

- **Docker API documentation:** The Docker API documentation provides information on how to use the Docker API, which allows you to programmatically interact with Docker.

- **Docker security documentation:** Docker security documentation provides information on how to secure Docker deployments and best practices for securing Docker containers.

These reference materials should provide you with the information you need to work with Docker effectively and securely.
