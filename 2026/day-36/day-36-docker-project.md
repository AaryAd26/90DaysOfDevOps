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

<img width="601" height="526" alt="image" src="https://github.com/user-attachments/assets/54db3262-f5cf-4b34-bf87-1d687dfd5151" />

---

### Task 2: Write the Dockerfile

1. Create a Dockerfile for your application

<img width="638" height="514" alt="image" src="https://github.com/user-attachments/assets/d0da49cd-a425-434c-8e1a-03f9fc42daaa" />

2. Use a **multi-stage build** if applicable
 
<img width="638" height="514" alt="image" src="https://github.com/user-attachments/assets/e8e98b56-2720-4216-8a78-bf5bd2f32fcd" />

3. Use a **non-root user**
4. Keep the image **small** — use alpine or slim base images

<img width="751" height="21" alt="image" src="https://github.com/user-attachments/assets/16c2970d-06fe-4257-bacb-4db1bcc730e9" />

5. Add a `.dockerignore` file

 <img width="338" height="203" alt="image" src="https://github.com/user-attachments/assets/b4019396-e36c-4703-9b3a-1cdc092bb33c" />


Build and test it locally.

Build : <br></br> <img width="638" height="514" alt="image" src="https://github.com/user-attachments/assets/96b0e138-3db6-4944-90cf-3084bb74844e" />

<img width="437" height="161" alt="image" src="https://github.com/user-attachments/assets/7310cba6-91a9-4df9-84b0-204e7447d559" />

Running Perfectly :<br></br> <img width="437" height="161" alt="image" src="https://github.com/user-attachments/assets/fa52f0cb-81b8-4e89-91ce-fbd66f250e1e" />

---

### Task 3: Add Docker Compose

Write a `docker-compose.yml` that includes:
1. Your **app** service (built from Dockerfile)
2. A **database** service (Postgres, MySQL, MongoDB — whatever your app needs)
3. **Volumes** for database persistence
4. A **custom network**
5. **Environment variables** for configuration (use `.env` file)
6. **Healthchecks** on the database

Run `docker compose up` and verify everything works together.

---

### Task 4: Ship It
1. Tag your app image
2. Push it to Docker Hub
3. Share the Docker Hub link
4. Write a `README.md` in your project with:
   - What the app does
   - How to run it with Docker Compose
   - Any environment variables needed

---

### Task 5: Test the Whole Flow
1. Remove all local images and containers
2. Pull from Docker Hub and run using only your compose file
3. Does it work fresh? If not — fix it until it does

---
