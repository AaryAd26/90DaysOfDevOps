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









 
