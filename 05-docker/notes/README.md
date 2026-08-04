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

  
