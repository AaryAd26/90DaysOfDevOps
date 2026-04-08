## Challenge Tasks

### Task 1: Pick Your App

Choose **one** of these (or use your own project):
- A **Python Flask/Django** app with a database
- A **Node.js Express** app with MongoDB
- A **static website** served by Nginx with a backend API
- Any app from your GitHub that doesn't have Docker yet

   took a simple node js project for this task
  here is its github link : https://github.com/heroku/node-js-sample

If you don't have an app, clone a simple open-source one and Dockerize it.
<br></br>
<img width="601" height="526" alt="image" src="https://github.com/user-attachments/assets/54db3262-f5cf-4b34-bf87-1d687dfd5151" />

---

### Task 2: Write the Dockerfile

1. Create a Dockerfile for your application
<br></br>
<img width="638" height="514" alt="image" src="https://github.com/user-attachments/assets/d0da49cd-a425-434c-8e1a-03f9fc42daaa" />

2. Use a **multi-stage build** if applicable
 <br></br>
<img width="638" height="514" alt="image" src="https://github.com/user-attachments/assets/e8e98b56-2720-4216-8a78-bf5bd2f32fcd" />

3. Use a **non-root user**
4. Keep the image **small** — use alpine or slim base images
<br></br>
<img width="751" height="21" alt="image" src="https://github.com/user-attachments/assets/16c2970d-06fe-4257-bacb-4db1bcc730e9" />

5. Add a `.dockerignore` file
<br></br>
 <img width="338" height="203" alt="image" src="https://github.com/user-attachments/assets/b4019396-e36c-4703-9b3a-1cdc092bb33c" />


Build and test it locally.

Build : <br></br> <img width="1418" height="507" alt="image" src="https://github.com/user-attachments/assets/83d39020-7afb-44ff-b39f-cf15c559ee8f" />

Running Perfectly :<br></br> <img width="1903" height="502" alt="image" src="https://github.com/user-attachments/assets/ae4e0bfb-3fba-47ef-bbf8-38b786be2941" />

---

### Task 3: Add Docker Compose

Write a `docker-compose.yml` that includes:

1. Your **app** service (built from Dockerfile)

<img width="704" height="688" alt="image" src="https://github.com/user-attachments/assets/9ec7d31a-8bca-4c0b-b8d3-8fb5e39bc200" />

2. A **database** service (Postgres, MySQL, MongoDB — whatever your app needs)
3. **Volumes** for database persistence
4. A **custom network**
5. **Environment variables** for configuration (use `.env` file)

<img width="428" height="92" alt="image" src="https://github.com/user-attachments/assets/7a3c701a-85fe-4b35-8dac-97a097f5ec86" />

6. **Healthchecks** on the database

Run `docker compose up` and verify everything works together.

<br></br><img width="1917" height="500" alt="image" src="https://github.com/user-attachments/assets/41731c24-7587-4011-a79a-602208d58578" />

<br></br><img width="1919" height="440" alt="image" src="https://github.com/user-attachments/assets/34ce9d1a-fc1d-453c-abce-72b943af059d" />

---

### Task 4: Ship It

1. Tag your app image

<br></br><img width="997" height="19" alt="image" src="https://github.com/user-attachments/assets/992ceebc-a5b9-4b42-9140-2ed2283240a6" />
   
2. Push it to Docker Hub

<br></br><img width="915" height="213" alt="image" src="https://github.com/user-attachments/assets/3952e70a-cfe2-4aa1-afbe-e93cb2e7b180" />

3. Share the Docker Hub link

https://hub.docker.com/repository/docker/aarydeshpande/note-app/general

4. Write a `README.md` in your project with:
   - What the app does
   - How to run it with Docker Compose
   - Any environment variables needed
<br></br><img width="1919" height="1039" alt="image" src="https://github.com/user-attachments/assets/21c867e1-3391-48de-9c8c-0955e4aa3a71" />

---

### Task 5: Test the Whole Flow

1. Remove all local images and containers

<br></br><img width="1599" height="130" alt="image" src="https://github.com/user-attachments/assets/4460ce15-bce5-413d-baf7-baac8d9e0b11" />

2. Pull from Docker Hub and run using only your compose file

 <br></br><img width="823" height="104" alt="image" src="https://github.com/user-attachments/assets/36efd840-3715-49ef-a1d2-e49a8ccbf1ca" />

3. Does it work fresh? If not — fix it until it does

 yes the project works perfectly 

 <br></br><img width="1919" height="501" alt="image" src="https://github.com/user-attachments/assets/dfbf805c-10cc-4da8-81ac-269c68fd9b85" />


---
