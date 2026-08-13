## What are Containers ?

- Containers are lightweight portable units used for running applications.
- They include the code, the runtime, the libraries and anything I need, including all dependencies needed for running an application. 

<img width="340" height="236" alt="image" src="https://github.com/user-attachments/assets/a93baea1-252c-42b1-8306-5a2be6ad4efc" />

- Infrastructure represents the physical or virtual hardware where everything runs.
- Docker Engine provides the environment to build, run and manage containers.
- Unlike virtual machines that take a subset of the OS, containers sit on top of the OS making them lightweight and efficient.

  
## Benefits of Containers

- Isolation: Each container is isolated, they have their own environment to run applications. This isolation prevents conflict and ensures each application runs smoothly without interfering  with each other.
- Consistency: It provides a consistent environment for applications to run, meaning applications behave the same way regardless of where its deployed making development and deployment more productive and reliable.
- Efficient: Containers are essentially sharing the whole systems kernel which reduces overhead and allows for more containers to run on the same hardware. This makes containers faster to start up and less resource incentive. 

## Docker 

- Docker is an open platform for developing, shipping and running applications in containers.
- Docker has several key components:
  . Docker Hub - Its a repository where you can find and share container images

  <img width="480" height="260" alt="image" src="https://github.com/user-attachments/assets/db021111-13b5-4aed-83f9-958601cb4078" />

## Images & Containers 

- Images are templates for creating containers, think of an image as a snapshot of an application at a certain point of time.
- Images are immutable, which means they do not change once created, the only way to change them is by recreating the image.
- The immutability ensures the application runs consistently regardless of where its deployed.
- Docker file is a file used to build docker images. It contains a series of instructions that Docker uses to assemble an image

## Importance of Docker in Modern Development

- Simplified Deployment: Docker ensures a consistent environment from development all the way to production. This eliminates the infamous statement "It works on my machine problem"
- Improved Efficiency: Traditional virtual machines can be resource heavy and slow to start. In Contrast, docker containers are lightweight and share the whole systems kernel which allows them to start up almost instantly using fewer resources.
- Enhanced Collaboration: Docker makes it easy to share development environments and applications with team members, it streamlines workflows by integrating seamlessly with CI/CD pipelines. By adopting Docker teams increase their productivity, reduce errors, and ensure a smoother development and deployment process

<img width="444" height="201" alt="image" src="https://github.com/user-attachments/assets/851e2ecf-2683-42fd-85a1-ded7f47e006c" />

## VMs Vs Containers

- Virtual machine allows multiple operating systems to run on a single physical machine , each virtual machine has a guest operating system making it resource intensive and slower to start.
- Containers on the other hand are lightweight and efficient way to isolate applications, they share the hosts operating system but instead of using a hypervisor they run on a docker engine. Contains don't have a guest operating system they sit on top of the host kernel which makes them lighter then VMs.
- Each Virtual machine needs to boot up a guest operating system which can take minutes, containers on the other hand share the host operating system and can start up in seconds.
- When it comes to resource usage  each VM includes a full host operating system which consumes significant resources. Containers are more efficient by using only what's necessary for the application and its dependencies.
- VMs provide a strong isolation with each VM having its own operating system. Containers provide process level isolation which means they share the hosts operating system kernel but they are isolated within the container itself
- VMs are less portable due to their size and dependency on hypervisors. Containers are highly portable and can run consistently across different environments.


<img width="491" height="255" alt="image" src="https://github.com/user-attachments/assets/03ff2f69-5230-466c-ac1c-eb5db6cc6a6c" />

## Understanding Docker Files 

- 5 KEY COMMANDS

  1. FROM - Specifies the base image to use to for the Docker image
  2. RUN - This command is used to execute commands in the container, for example its used to install packages, update dependencies and so on.
  3. COPY - This command copies files from the host machine into the container
  4. WORKDIR- Sets the working directory for subsequent instructions, this ensures the command runs in the correct directory within the container.
  5. CMD- Specifies the command to run when the container starts 
  
## Docker Networking 

- Docker provides several default network options that you can use to manage how networks containers communicate.
- Bridge Network is a default network mode for containers on the same machine, containers on the bridge network can communicate with each other using their own IP addresses.
- Host mode - In host mode a container uses the host machines network directly without any isolation. This is useful for containers that need to interact closely with the hosts system.
- None- This option gives a container no network interface at all which makes it completely isolated. This is used when you want to ensure a container has no network access whatsoever which could be useful for certain security scenarios
- In the context of DevOps, Docker Networking is extremely important because it simplifies the implementation of microservices architecture. Microservices allow different parts of an application to run as independent services each in its own container. It ensures these services can communicate with each other efficiently and securely. 

## Docker Compose 

- Docker Compose provides a powerful and efficient way to manage multiple container docker applications.
- At the heart of Docker Compose is a Docker Compose Yaml file, this yaml file lists all the services your application needs, its like a blueprint that specifies details like what image to use, which port to expose, and how the containers should interact.
- It allows you to orchestrate your entire stack with minimal effect.
- When you use Docker Compose it automatically creates a network for your containers, before we had to create a custom network 

<img width="462" height="236" alt="image" src="https://github.com/user-attachments/assets/5029feb9-d005-4602-84f7-5b9f5a5c495b" />

## Importance of Docker Compose in DevOps 

- It makes development and testing easier, you can easily spin up your desired environment using a single command in Docker Compose allowing developers to focus more on code rather then the infrastructure. 
- Ensures Consistency, by defining your environment in a yaml Docker Compose file, you guarantee that every developer, tester and CI/CD pipeline uses the exact same setup. This consistency reduces bugs and errors leading to more reliable software.
- Enhances teamwork, when every team member is using the same environment, it makes it much easier to share the code configurations and even the environment set up itself, in summary it makes it easier to version control your infrastructure. 


# Docker Registries 

- Think of Docker Registry as a storage or distribution hub for your docker images
- Key features of a Docker Registry:
- Public Registry: Its a place where you can share your images with the world
- Private Registry: They allow you to control who can have access to your images, this is crucial when dealing with sensitive or proprietary applications.


# Importance of Docker Registry in DevOps

- They streamline the deployment process, once your docker images are stored in the registry they can be easily accessed and deployed across multiple environments from deployment all the way to production, meaning that its easier to roll out updates or new features.
- Enhances collaboration - when your image is stored in a centralised registry, everyone on your team has access to the same resources. This makes it easier to share and manage your images, improving teamwork and efficiency.
- Ensures consistency across different environments. By storing your image in a registry you can be sure that the exact same image is used in development, testing and production. Once again it removes the it works on my machine problem.

   <img width="479" height="255" alt="image" src="https://github.com/user-attachments/assets/d06f0f63-d57e-48a7-94f2-2e340937553a" />
