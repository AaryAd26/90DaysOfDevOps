# Day 29 – Introduction to Docker

## Challenge Tasks
## Task 1: What is Docker?

- Research and write short notes on:

- What is a container and why do we need them?
-> A **container** is a runtime instance of a Docker image. It includes everything required to run an application:
      - Code  
      - Dependencies  
      - Libraries  
      - Configuration  

- Containers vs Virtual Machines — what's the real difference?
  -> ### 🔹 Containers vs Virtual Machines

| Containers | Virtual Machines |
|-----------|----------------|
| Use host OS | Have their own OS |
| Share system resources | Dedicated resources |
| Lightweight | Heavy |
| Fast startup | Slow startup |
| Highly portable | Less portable | 

- What is the Docker architecture? (daemon, client, images, containers, registry)
  -> ### 🔹 Docker Architecture

Docker follows a **client-server architecture**.

#### Components:

- **Docker Daemon**
  - Manages containers, images, networks, and volumes  

- **Docker Client**
  - Sends commands to the Docker daemon  

- **Docker Images**
  - Blueprint used to create containers  

- **Docker Containers**
  - Running instances of images  

- **Docker Registry**
  - Stores Docker images  

  **Types:**
  - Public → Docker Hub  
  - Private → Used by organizations  

---

 ### task 2 
1. Install Docker on your machine (or use a cloud instance)
3. Verify the installation
4. Run the hello-world container
5. Read the output carefully — it explains what just happened

   <img width="738" height="524" alt="Screenshot 2026-03-19 004622" src="https://github.com/user-attachments/assets/543255e1-d0f6-4d3f-83ff-e3a1864e4697" />

---

### Task 3: Run Real Containers

1. Run an Nginx container and access it in your browser
   <img width="727" height="283" alt="Screenshot 2026-03-19 004807" src="https://github.com/user-attachments/assets/2a21d660-f549-4899-85bf-6e6ffddd0d6f" />

   <img width="1919" height="534" alt="Screenshot 2026-03-19 004814" src="https://github.com/user-attachments/assets/fc6c03f3-e45e-4118-a1d4-47f272c72e29" />

 
2. Run an Ubuntu container in interactive mode — explore it like a mini Linux machine

    <img width="961" height="736" alt="Screenshot 2026-03-19 005050" src="https://github.com/user-attachments/assets/e3d82308-cb5b-4625-9940-2ca6e43f87ac" />

3. List all running containers
    <img width="1428" height="63" alt="Screenshot 2026-03-19 005250" src="https://github.com/user-attachments/assets/9f341c75-f6d5-4ef8-a30f-33584865243a" />

4. List all containers (including stopped ones)
    <img width="1524" height="99" alt="Screenshot 2026-03-19 005254" src="https://github.com/user-attachments/assets/f771054a-0a65-4c27-9ba9-b5ec881bedc4" />

 
5. Stop and remove a container
    <img width="674" height="183" alt="Screenshot 2026-03-19 005312" src="https://github.com/user-attachments/assets/78a2cea6-0909-4e5f-86de-9e9f1fbcf43b" />

---

### Task 4: Explore

1. Run a container in detached mode — what's different?
   <img width="732" height="252" alt="Screenshot 2026-03-19 005741" src="https://github.com/user-attachments/assets/6259a560-849b-4c97-9bc9-945e2ae2071e" />


2. Give a container a custom name
  <img width="593" height="44" alt="Screenshot 2026-03-19 005747" src="https://github.com/user-attachments/assets/b2cf5f8e-ef95-48c8-94e3-c713deb6994a" />

3.Map a port from the container to your host
  <img width="727" height="283" alt="Screenshot 2026-03-19 004807" src="https://github.com/user-attachments/assets/2a21d660-f549-4899-85bf-6e6ffddd0d6f" />
   
   <img width="1919" height="735" alt="Screenshot 2026-03-19 005731" src="https://github.com/user-attachments/assets/fa543f57-677e-4473-ac1f-c3e012071035" />

4.Check logs of a running container
   <img width="883" height="624" alt="Screenshot 2026-03-19 005821" src="https://github.com/user-attachments/assets/f2edbcf4-8020-4a5e-9af0-932d7d27abaa" />

5.Run a command inside a running container
  <img width="1373" height="167" alt="Screenshot 2026-03-19 005900" src="https://github.com/user-attachments/assets/50914345-699c-4282-8448-043fe76f01bd" />

  -----

  # COMPLETED WITH DAY 29 TASK 






 
