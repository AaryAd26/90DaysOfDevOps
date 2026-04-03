 # Day 35 – Multi-Stage Builds & Docker Hub

  ---

## Challenge Tasks

### Task 1: The Problem with Large Images

1. Write a simple Go, Java, or Node.js app (even a "Hello World" is fine)
   <img width="370" height="141" alt="image" src="https://github.com/user-attachments/assets/2e850743-7278-4fa6-bc21-b00832a442e1" />
<img width="408" height="197" alt="image" src="https://github.com/user-attachments/assets/38383a7c-0165-4e12-9ca2-ddf4d07b9136" />

2. Create a Dockerfile that builds and runs it in a **single stage**
<img width="321" height="294" alt="image" src="https://github.com/user-attachments/assets/7e946f37-e50b-477b-80d9-6a72f0a309f8" />

3. Build the image and check its **size**
<img width="930" height="108" alt="image" src="https://github.com/user-attachments/assets/7906a9c8-2109-40de-9d23-ab869d468e21" />

Note down the size — you'll compare it later.

--> Node js application base image is too Heavy (almost 1.09GB).
--> It Also Include Build tools .
--> It also Includes Npm cache which makes it Hevay to pull the image

---

### Task 2: Multi-Stage Build

1. Rewrite the Dockerfile using **multi-stage build**:
   - Stage 1: Build the app (install dependencies, compile)
   - Stage 2: Copy only the built artifact into a minimal base image (`alpine`, `distroless`, or `scratch`)

<img width="360" height="403" alt="image" src="https://github.com/user-attachments/assets/83fbe8cb-b4f0-4b92-9ae6-a8c37c8db9b6" />

2. Build the image and check its size again

<img width="718" height="127" alt="image" src="https://github.com/user-attachments/assets/dc897906-a90a-4dc1-a903-eb16bb68c52c" />

3. Compare the two sizes

<img width="753" height="128" alt="image" src="https://github.com/user-attachments/assets/07fa67d1-c0ab-4db5-88a7-6a6ba8702b1d" />

**Q.**Write in your notes: Why is the multi-stage image so much smaller?

---> the Multu satge image is much smaller because the final image only contain the App code & Required Depedencies.
---> It does not Required any build tools. 
---> Alpine base image is lightweight that why the image size get small. 
---> Also it removes unnecessay layers.

---

### Task 3: Push to Docker Hub

1. Create a free account on [Docker Hub](https://hub.docker.com) (if you don't have one)

 ----> Alreadt have one 
 <img width="833" height="130" alt="image" src="https://github.com/user-attachments/assets/eb433f46-553d-4b91-ad04-f267820b1bdd" /> 
 
2. Log in from your terminal

<img width="833" height="130" alt="image" src="https://github.com/user-attachments/assets/a9466d72-f012-4bd3-b38e-a2518714240d" />

3. Tag your image properly: `yourusername/image-name:tag`

<img width="1013" height="22" alt="image" src="https://github.com/user-attachments/assets/a8576245-0fce-4f74-b169-7bb0ef6231dd" />

4. Push it to Docker Hub

<img width="1919" height="608" alt="image" src="https://github.com/user-attachments/assets/a41bdbe2-97dc-49db-abff-0f86bb89eae2" />

5. Pull it on a different machine (or after removing locally) to verify

---

### Task 4: Docker Hub Repository

1. Go to Docker Hub and check your pushed image

<img width="1917" height="556" alt="image" src="https://github.com/user-attachments/assets/ce27c5e7-dd9d-42d5-8ade-069c1e935257" />

2. Add a **description** to the repository

<img width="625" height="196" alt="image" src="https://github.com/user-attachments/assets/cfaa5c0e-30d3-4eea-b70e-45a2eef6a5b1" />

3. Explore the **tags** tab — understand how versioning works

<img width="1463" height="348" alt="image" src="https://github.com/user-attachments/assets/a0d0d5a4-06df-48de-8a3a-cc1faf71c887" />

4. Pull a specific tag vs `latest` — what happens?

---

### Task 5: Image Best Practices
Apply these to one of your images and rebuild:

1. Use a **minimal base image** (alpine vs ubuntu — compare sizes)

<img width="379" height="427" alt="image" src="https://github.com/user-attachments/assets/c5960608-c330-4acd-bd56-251dae33b50f" />

2. **Don't run as root** — add a non-root USER in your Dockerfile

3. Combine `RUN` commands to **reduce layers**

4. Use **specific tags** for base images (not `latest`)

Check the size before and after.

* size Before : 445MB
* Size After  : 303MB 
  
---
