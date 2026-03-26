# Day 31 – Dockerfile: Build Your Own Images

---

## Challenge Tasks

### Task 1: Your First Dockerfile

1. Create a folder called `my-first-image`
2. Inside it, create a `Dockerfile` that:
   - Uses `ubuntu` as the base image
   - Installs `curl`
   - Sets a default command to print `"Hello from my custom image!"`
3. Build the image and tag it `my-ubuntu:v1`
4. Run a container from your image

<img width="1919" height="577" alt="image" src="https://github.com/user-attachments/assets/05115e17-f105-4a2d-a1e1-2b3de0a3cda2" />

---

### Task 2: Dockerfile Instructions

Create a new Dockerfile that uses **all** of these instructions:
- `FROM` — base image
- `RUN` — execute commands during build
- `COPY` — copy files from host to image
- `WORKDIR` — set working directory
- `EXPOSE` — document the port
- `CMD` — default command

<img width="470" height="268" alt="image" src="https://github.com/user-attachments/assets/90b875c2-06d9-40fd-9325-2e68707a1cfe" />
<img width="1919" height="366" alt="image" src="https://github.com/user-attachments/assets/0c682ec7-734a-41ce-aebc-5343ee1d1288" />
<img width="1919" height="487" alt="image" src="https://github.com/user-attachments/assets/3c9d1995-77d7-4dfa-8809-0fb2f64b7b9e" />

---

### Task 3: CMD vs ENTRYPOINT

1. Create an image with `CMD ["echo", "hello"]` — run it, then run it with a custom command. What happens?
2. 
<img width="318" height="108" alt="image" src="https://github.com/user-attachments/assets/45e31a52-4b74-425e-b1e1-e7a7083d4683" />
<img width="556" height="61" alt="image" src="https://github.com/user-attachments/assets/f5c6d7de-d972-4d3d-bfe9-b12e667a94eb" />
<img width="617" height="63" alt="image" src="https://github.com/user-attachments/assets/90d22ada-0209-4122-ad1e-b6505fccf051" />

3. Create an image with `ENTRYPOINT ["echo"]` — run it, then run it with additional arguments. What happens?
<img width="1167" height="293" alt="image" src="https://github.com/user-attachments/assets/5b0c0236-8e46-4ba2-ab3c-24f3d077098c" />

4. Write in your notes: When would you use CMD vs ENTRYPOINT?
   **CMD** :  In CMD we can over write a command if you pass a command at runtime,
   **ENTRYPOINT** : Always runs the specified command first. Appends any additional arguments passed at runtime.

---

### Task 4: Build a Simple Web App Image

1. Create a small static HTML file (`index.html`) with any content
2. 
    <img width="901" height="1016" alt="image" src="https://github.com/user-attachments/assets/d467c162-f268-4575-bd1b-e3157109ab51" />
    <img width="1919" height="728" alt="image" src="https://github.com/user-attachments/assets/a0e348cb-4f5c-4b15-b89e-77eb479acfde" />
    
3. Write a Dockerfile that:
   - Uses `nginx:alpine` as base
   - Copies your `index.html` to the Nginx web directory
   - 
<img width="1044" height="1079" alt="image" src="https://github.com/user-attachments/assets/731398e3-7954-4f44-84ea-f88e5653022b" />

4. Build and tag it `my-website:v1`
5. Run it with port mapping and access it in your browser
   
<img width="1919" height="728" alt="image" src="https://github.com/user-attachments/assets/793358cf-d473-4155-94cf-1561ad3154ea" />

---

### Task 5: .dockerignore

1. Create a `.dockerignore` file in one of your project folders
2. 
<img width="522" height="28" alt="image" src="https://github.com/user-attachments/assets/ad8dbadb-a9f8-4778-90fc-6f982c839aed" />

3. Add entries for: `node_modules`, `.git`, `*.md`, `.env`
4. 
<img width="330" height="177" alt="image" src="https://github.com/user-attachments/assets/d4bf0c1d-111e-479e-9bbc-5a23f8a0e1c4" />

5. Build the image — verify that ignored files are not included

---

### Task 6: Build Optimization

1. Build an image, then change one line and rebuild — notice how Docker uses **cache**
2. 
    <img width="475" height="179" alt="image" src="https://github.com/user-attachments/assets/82dd88b2-009a-4e67-98d4-b863c089e510" />
    <img width="1919" height="367" alt="image" src="https://github.com/user-attachments/assets/3b4dc446-8f1d-4baf-b29e-b8fd8b5224df" />

3. Reorder your Dockerfile so that frequently changing lines come **last**
4. 
   <img width="518" height="208" alt="image" src="https://github.com/user-attachments/assets/7c70be68-555e-468f-bb69-64aafbb33d46" />
  <img width="1919" height="392" alt="image" src="https://github.com/user-attachments/assets/1b20a36d-c3b3-4ee5-8b43-b0a6d84c4f81" />

5. Write in your notes: Why does layer order matter for build speed?
  -> Docker builds images layer by layer, and each layer is cached. If a layer changes, all subsequent layers must be rebuilt. Therefore, placing frequently changing instructions (like COPY) at the end allows Docker to reuse cached layers for earlier steps, significantly improving build speed.

---



   
