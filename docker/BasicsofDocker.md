## Introduction of Container
Containers are lightweight packages of software that contain all of the necessary elements to run in any environment.
## virtual machine(Hypervisor) VS Container
The key differentiator between containers and virtual machines is that virtual machines virtualize an entire machine down to the hardware layers and containers only virtualize software layers above the operating system level.
## Why we use container instead of virtual machine
Virtual machines take up more storage space and require you to provision more hardware in your on-premises data centers. Switching to cloud instances reduces costs but migrating your entire environment brings its own challenges. Containers take up less space and are easier to scale. containers are often preferred for their lightweight nature, faster startup times, and high portability, making them well-suited for modern, agile, and cloud-native application development and deployment.
## Architecture of Container

![Getting Started][def2]
[def2]: D:\i3\dockerArch


The above picture, clearly indicates that Docker Deamon is brain of Docker. If Docker Deamon is killed, stops working for some reasons, Docker is brain dead.
## Why container is lightwaighted ?
Container are light weight- Because container doesn't have a complete Operating system. Container are going to use Host System Kernel.
## what is docker ?
Docker is a software platform that allows you to build, test, and deploy applications quickly.
## what is lifecycle of Docker ?
![Getting Started][def]

[def]: D:\i3\dockerLife
The lifecycle of a Docker container involves several stages, from creating a Docker image to running and managing the container.

## What is Docker demon,docker client, docker image, docker desktop,Docker registries, Dockerfile
Docker Daemon: \n

The Docker daemon (dockerd) is a background process that runs on the host system and manages Docker containers. It listens for Docker API requests and takes care of building, running, and managing containers.
The daemon communicates with the Docker client, handling tasks such as container creation, image building, and network management. \n
Docker Client: \n

The Docker client (docker) is a command-line interface (CLI) or graphical user interface (GUI) tool that allows users to interact with the Docker daemon. It accepts commands from users and communicates them to the Docker daemon for execution.
The Docker client can run on the same host as the daemon or connect to a remote Docker daemon.\n
Docker Image: \n

A Docker image is a lightweight, portable, and executable package that includes an application and its dependencies. It is the blueprint for creating Docker containers.\n
Docker images are built from a set of instructions defined in a text file called a Dockerfile. Images can be stored in Docker registries and pulled to different environments for running containers.\n
Docker Desktop:\n

Docker Desktop is an application for Windows and macOS that provides an integrated environment for developing, building, and testing Dockerized applications.
It includes the Docker daemon, Docker CLI, and other tools, making it easy for developers to work with Docker on their local machines.\n
Docker Registries:\n

Docker registries are repositories for storing and distributing Docker images. They can be public or private.
Docker Hub is a popular public registry where users can find and share Docker images. Organizations often set up private registries (e.g., Azure Container Registry, Google Container Registry) for storing proprietary or sensitive images.\n
Dockerfile:\n

A Dockerfile is a text file that contains instructions for building a Docker image. It specifies the base image, application code, dependencies, environment variables, and other configuration settings.
Developers use the docker build command to create a Docker image from a Dockerfile. Each instruction in the Dockerfile contributes to a layer in the image, allowing for efficient image building and caching.\n

##  File and folder in conatiner base images and Host(used by container)
Files and Folders in containers base images
    /bin: contains binary executable files, such as the ls, cp, and ps commands.

    /sbin: contains system binary executable files, such as the init and shutdown commands.

    /etc: contains configuration files for various system services.

    /lib: contains library files that are used by the binary executables.

    /usr: contains user-related files and utilities, such as applications, libraries, and documentation.

    /var: contains variable data, such as log files, spool files, and temporary files.

    /root: is the home directory of the root user.

Files and Folders that containers use from host operating system
    The host's file system: Docker containers can access the host file system using bind mounts, which allow the container to read and write files in the host file system.

    Networking stack: The host's networking stack is used to provide network connectivity to the container. Docker containers can be connected to the host's network directly or through a virtual network.

    System calls: The host's kernel handles system calls from the container, which is how the container accesses the host's resources, such as CPU, memory, and I/O.

    Namespaces: Docker containers use Linux namespaces to create isolated environments for the container's processes. Namespaces provide isolation for resources such as the file system, process ID, and network.

    Control groups (cgroups): Docker containers use cgroups to limit and control the amount of resources, such as CPU, memory, and I/O, that a container can access.
    

