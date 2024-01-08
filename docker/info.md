## What is Container 
A container is a lightweight, standalone, and portable package that includes everything needed to run a software application, making it easy to deploy and run consistently across different environments. Containers use containerization technology, like Docker, to isolate and encapsulate applications and their dependencies.
Ok, let me make it easy !!!
A container is a bundle of Application, Application libraries required to run your application and the minimum system dependencies.
 
## Containers vs Virtual Machine
1.	Container:
•	A running instance of a Docker image or a containerized application.
•	It is the executable unit that encapsulates the application and its dependencies, isolated from the host system and other containers.
2.	Image:
•	A lightweight, standalone, and portable package that includes the application code, runtime, libraries, and settings.
•	It serves as a blueprint for creating containers.
•	Images are used to create containers, and they can be shared and reused across different environments.

1. Resource Utilization: Containers share the host operating system kernel, making them lighter and faster than VMs. VMs have a full-fledged OS and hypervisor, making them more resource-intensive.
2. Portability: Containers are designed to be portable and can run on any system with a compatible host operating system. VMs are less portable as they need a compatible hypervisor to run.
3. Security: VMs provide a higher level of security as each VM has its own operating system and can be isolated from the host and other VMs. Containers provide less isolation, as they share the host operating system.
4. Management: Managing containers is typically easier than managing VMs, as containers are designed to be lightweight and fast-moving.
Why are containers light weight ?
Containers are lightweight because they share the host operating system's kernel, include only essential components, utilize efficient resource management, employ a layered filesystem for image construction, and offer quick start/stop capabilities. These characteristics result in faster deployment, efficient resource utilization, and rapid scaling.
# Files and Folders in containers base images
 /bin: contains binary executable files, such as the ls, cp, and ps commands.\
 /sbin: contains system binary executable files, such as the init and shutdown commands.\
/etc: contains configuration files for various system services.\
/lib: contains library files that are used by the binary executables.\
 /usr: contains user-related files and utilities, such as applications, libraries, and documentation.\
 /var: contains variable data, such as log files, spool files, and temporary files.\
 /root: is the home directory of the root user.\
Files and Folders that containers use from host operating system\
The host's file system: Docker containers can access the host file system using bind mounts, which allow the container to read and write
# files in the host file system.
Networking stack: The host's networking stack is used to provide network connectivity to the container. Docker containers can be connected to the host's network directly or through a virtual network.
System calls: The host's kernel handles system calls from the container, which is how the container accesses the host's resources, such as CPU, memory, and I/O.
Namespaces: Docker containers use Linux namespaces to create isolated environments for the container's processes. Namespaces provide isolation for resources such as the file system, process ID, and network.
Control groups (cgroups): Docker containers use cgroups to limit and control the amount of resources, such as CPU, memory, and I/O, that a container can access.
What is Docker ?
Docker is a platform for developing, shipping, and running applications in containers. It provides a set of tools and a platform to simplify the process of creating, deploying, and managing containerized applications. Docker uses containerization technology, which allows developers to package an application and its dependencies into a standardized unit called a container.
Docker Architecture ?
 

## Key components and features of Docker include:
1.	Containerization: Docker allows applications to be packaged along with their dependencies and runtime environment into a container. Containers provide consistency across different environments, making it easier to deploy and run applications.
2.	Docker Engine: The core component of Docker, responsible for building, running, and managing containers. It includes a daemon process, REST API, and a command-line interface (CLI) for interacting with Docker.
3.	Docker Images: These are lightweight, portable, and standalone packages that include the application code, runtime, libraries, and settings. Docker images serve as the blueprint for creating containers.
4.	Docker Hub: A cloud-based registry service where users can share and access Docker images. It facilitates collaboration by allowing users to publish and distribute their container images.
5.	Docker Compose: A tool for defining and running multi-container Docker applications. It uses a YAML file to configure the application's services, networks, and volumes, enabling easy management of complex applications.
6.	Docker Swarm: A native clustering and orchestration solution for Docker. It allows users to create and manage a swarm of Docker nodes, making it easy to scale applications and distribute workloads across multiple containers.
Docker daemon
The Docker daemon (dockerd) listens for Docker API requests and manages Docker objects such as images, containers, networks, and volumes. A daemon can also communicate with other daemons to manage Docker services.
Docker client
The Docker client (docker) is the primary way that many Docker users interact with Docker. When you use commands such as docker run, the client sends these commands to dockerd, which carries them out. The docker command uses the Docker API. The Docker client can communicate with more than one daemon.
Docker Desktop
Docker Desktop is an easy-to-install application for your Mac, Windows or Linux environment that enables you to build and share containerized applications and microservices. Docker Desktop includes the Docker daemon (dockerd), the Docker client (docker), Docker Compose, Docker Content Trust, Kubernetes, and Credential Helper. For more information, see Docker Desktop.
Docker registries
A Docker registry stores Docker images. Docker Hub is a public registry that anyone can use, and Docker is configured to look for images on Docker Hub by default. You can even run your own private registry.
When you use the docker pull or docker run commands, the required images are pulled from your configured registry. When you use the docker push command, your image is pushed to your configured registry. Docker objects
When you use Docker, you are creating and using images, containers, networks, volumes, plugins, and other objects. This section is a brief overview of some of those objects.
Dockerfile
Dockerfile is a file where you provide the steps to build your Docker Image.
Images
An image is a read-only template with instructions for creating a Docker container. Often, an image is based on another image, with some additional customization. For example, you may build an image which is based on the ubuntu image, but installs the Apache web server and your application, as well as the configuration details needed to make your application run.
You might create your own images or you might only use those created by others and published in a registry. To build your own image, you create a Dockerfile with a simple syntax for defining the steps needed to create the image and run it. Each instruction in a Dockerfile creates a layer in the image. When you change the Dockerfile and rebuild the image, only those layers which have changed are rebuilt. This is part of what makes images so lightweight, small, and fast, when compared to other virtualization technologies.
Docker has become a widely adopted technology in the software development and IT industry due to its simplicity, efficiency, and portability. It has revolutionized the way applications are developed, deployed, and maintained by providing a standardized and consistent environment across various platforms.
Docker LifeCycle
 We can use the above Image as reference to understand the lifecycle of Docker.
There are three important things,
1.	docker build -> builds docker images from Dockerfile
2.	docker run -> runs container from docker images
3.	docker push -> push the container image to public/private regestries to share the docker images.




