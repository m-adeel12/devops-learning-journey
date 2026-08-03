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
