## Day 30 – Docker Images & Container Lifecycle

# Task

# Challenge Tasks

# Task 1: Docker Images

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

---

# Task 2: Image Layers

1.Run docker image history nginx — what do you see?
2.Each line is a layer. Note how some layers show sizes and some show 0B
3.Write in your notes: What are layers and why does Docker use them?

------> Docker image layers are created whenever changes are made to the file system.
        Each instruction in a Dockerfile—such as FROM, COPY, RUN, or CMD—generates a separate layer.
These layers are crucial because Docker caches them during the image build process and stores them in the Docker engine. When you rebuild an image, Docker reuses the cached layers for any steps that haven’t changed.
As a result, image builds become faster and more efficient.

<img width="1192" height="575" alt="image" src="https://github.com/user-attachments/assets/47fdf0b7-f8c0-4e95-8f32-986f7490374a" />

---

# Task 3: Container Lifecycle
Practice the full lifecycle on one container:

1. Create a container (without starting it)
2. Start the container
3.Pause it and check status
4. Unpause it
5. Stop it
6. Restart it
7. Kill it
8. Remove it

Check docker ps -a after each step — observe the state change

<img width="1141" height="709" alt="image" src="https://github.com/user-attachments/assets/4dfa9cb3-adac-4ac2-a845-df89b9e4809f" />

---

# Task 4: Working with Running Containers

1. Run an Nginx container in detached mode
<img width="1" height="3" alt="image" src="https://github.com/user-attachments/assets/656c25c5-fde8-40c5-b263-af411a585032" />

2. View its logs
<img width="901" height="612" alt="image" src="https://github.com/user-attachments/assets/c70935bf-3ccd-408a-b1fc-70ec9f3ec160" />

3. View real-time logs (follow mode)
<img width="902" height="656" alt="image" src="https://github.com/user-attachments/assets/7f6f13da-8910-4870-8d4e-20b624407261" />

4. Exec into the container and look around the filesystem
<img width="1338" height="687" alt="image" src="https://github.com/user-attachments/assets/ebf26c46-e952-446a-bf68-8d1ef643ee11" />

5. Run a single command inside the container without entering it
<img width="713" height="52" alt="Screenshot 2026-03-25 214624" src="https://github.com/user-attachments/assets/57a3fab5-3d01-4990-a859-dc59ea127173" />
<img width="838" height="115" alt="Screenshot 2026-03-25 214631" src="https://github.com/user-attachments/assets/cd214f16-c2e2-4eca-88d1-669984905ad8" />

6. Inspect the container — find its IP address, port mappings, and mounts

<img width="1069" height="445" alt="Screenshot 2026-03-25 214613" src="https://github.com/user-attachments/assets/5e80a883-abcd-4a3a-9ccd-2839f2f09b91" />
<img width="808" height="309" alt="Screenshot 2026-03-25 214605" src="https://github.com/user-attachments/assets/136b953a-ab03-4112-8289-145875b0485b" />
<img width="131" height="22" alt="Screenshot 2026-03-25 214547" src="https://github.com/user-attachments/assets/819782e4-6859-4311-9beb-a7c4bd79a3f6" />


---

# Task 5: Cleanup

1. Stop all running containers in one command
2. Remove all stopped containers in one command
3. Remove unused images
4. Check how much disk space Docker is using
