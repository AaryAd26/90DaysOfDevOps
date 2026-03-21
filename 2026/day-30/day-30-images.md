## Day 30 – Docker Images & Container Lifecycle

# Task

# Challenge Tasks

Task 1: Docker Images

1. Pull the nginx, ubuntu, and alpine images from Docker Hub
     Pulled Images usinig command - docker pull <imagename>
     For nginx - docker pull nginx
     For Alpine - docker pull alpine
     For ubuntu - docker pull ubuntu

3. List all images on your machine — note the sizes
   <img width="1184" height="167" alt="image" src="https://github.com/user-attachments/assets/59acbd0e-87a9-4bd1-ac2a-18e3f660f138" />

4. Compare ubuntu vs alpine — why is one much smaller?
   **UBUNTU** - Ubuntu docker size is bigger because ubuntu is a full fledgee Operating System that includes many default utilities and libraries
   **ALPINE** - Alpine Linux is a minimalist distribution designed to contain only the bare essentials needed to run a single application

5. Inspect an image — what information can you see?
  - Image ID
  - Image Tag
  - Created Time
  - Default Config
  - Ports
  - Environment variables
  - Entrypoint
  - CMD
  - Architecture
  - OS
  - Size
  - Graph Driver
  - Layers
   
6. Remove an image you no longer need
    docker rm <imageid>
   <img width="689" height="81" alt="image" src="https://github.com/user-attachments/assets/2c973453-7f46-4001-a7ca-f8c64c0b7610" />
