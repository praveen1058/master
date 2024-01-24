## Dockerfile details- FROM, WORKDIR, COPY, RUN, ENV, CMD, ENTRYPOINT
A Dockerfile is a script used to build a Docker image. It consists of a set of instructions that specify how to assemble a Docker image layer by layer. Here are details about some commonly used instructions in a Dockerfile:

## FROM:

The FROM instruction specifies the base image from which the current image is built. It is the starting point for the Dockerfile.
Example: FROM ubuntu:20.04 specifies that the base image is Ubuntu version 20.04.
## WORKDIR:

The WORKDIR instruction sets the working directory for subsequent instructions in the Dockerfile.
Example: WORKDIR /app sets the working directory to /app for subsequent commands.
## COPY:

The COPY instruction copies files or directories from the build context (the directory containing the Dockerfile) into the image.
Example: COPY . /app copies all files from the build context to the /app directory in the image.
## RUN:

The RUN instruction executes commands in a new layer on top of the current image and commits the results. It is used for installing packages, setting up configurations, or running any command during image build.
Example: RUN apt-get update && apt-get install -y nginx installs the Nginx web server during image build.
## ENV:

The ENV instruction sets environment variables in the image. These variables can be used in subsequent instructions.
Example: ENV APP_VERSION 1.0 sets the environment variable APP_VERSION to 1.0.
## CMD:

The CMD instruction provides the default command to run when a container is started from the image. It can be overridden when running the container.
Example: CMD ["npm", "start"] sets the default command to run an application using npm when the container starts.
## ENTRYPOINT:

The ENTRYPOINT instruction allows you to configure a container that will run as an executable. It is often used to define the default executable for the container.
Example: ENTRYPOINT ["nginx", "-g", "daemon off;"] sets the default executable to run the Nginx web server.

## difference b/w CMD and ENTRYPOINT
Both CMD and ENTRYPOINT directives serve the same purpose. They provide default commands to be executed when a Docker image is run as a container. However, they differ in how their arguments behave.

The main distinction is that the argument passed to the ENTRYPOINT directive cannot be overridden, while the argument passed to the CMD directive can. This means that the ENTRYPOINT directive sets a fixed command that cannot be modified when running the container, whereas the CMD directive allows for flexibility in specifying alternative arguments.

Choosing between CMD and ENTRYPOINT depends on your specific requirements. However, it is a common practice to use both directives together. The ENTRYPOINT directive is used to define the default command, while the CMD directive is used to pass default arguments to the ENTRYPOINT directive.





