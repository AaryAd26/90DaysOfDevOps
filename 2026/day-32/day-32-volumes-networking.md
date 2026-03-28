## Task 1 : The Problem

1. Run a Postgres or MySQL container
<img width="1156" height="402" alt="image" src="https://github.com/user-attachments/assets/7dc17dee-6a0a-41de-b31d-e7964726b9e1" />
<img width="1381" height="83" alt="image" src="https://github.com/user-attachments/assets/b0ae9d2e-c885-424c-b3c2-ff6a216fa515" />

2. Create some data inside it (a table, a few rows — anything)
<img width="817" height="175" alt="image" src="https://github.com/user-attachments/assets/342aec8c-1799-4a13-bd33-5f1c2272471f" />

3. Stop and remove the container
<img width="422" height="162" alt="image" src="https://github.com/user-attachments/assets/f16cf307-3f81-4ec9-bd63-a2ddc6bebaea" />

4. Run a new one — is your data still there?
<img width="1173" height="419" alt="image" src="https://github.com/user-attachments/assets/f966ae83-0bd2-4a8b-b3d2-15b5a056e719" />

Q. Write what happened and why.
  ---> After Deleting the Image the data was lost and the table does not exists anymore because Data is stored inside container filesystem so when container is deleted the data is deleted permenantly 

---

### Task 2: Named Volumes

1. Create a named volume
<img width="698" height="173" alt="image" src="https://github.com/user-attachments/assets/562966ce-88d1-4647-8623-9e6e08c91144" />

2. Run the same database container, but this time **attach the volume** to it

3. Add some data, stop and remove the container

4. Run a brand new container with the **same volume**

5. Is the data still there?

---

### Task 3: Bind Mounts

1. Create a folder on your host machine with an `index.html` file

2. Run an Nginx container and **bind mount** your folder to the Nginx web directory

3. Access the page in your browser

4. Edit the `index.html` on your host — refresh the browser

Write in your notes: What is the difference between a named volume and a bind mount?

---

### Task 4: Docker Networking Basics

1. List all Docker networks on your machine

2. Inspect the default `bridge` network

3. Run two containers on the default bridge — can they ping each other by **name**?

4. Run two containers on the default bridge — can they ping each other by **IP**?

---

### Task 5: Custom Networks

1. Create a custom bridge network called `my-app-net`

2. Run two containers on `my-app-net`

3. Can they ping each other by **name** now?

4. Write in your notes: Why does custom networking allow name-based communication but the default bridge doesn't?

---

### Task 6: Put It Together

1. Create a custom network

2. Run a **database container** (MySQL/Postgres) on that network with a volume for data

3. Run an **app container** (use any image) on the same network

5. Verify the app container can reach the database by container name



---






