## Task 1 : The Problem

1. Run a Postgres or MySQL container
2. 
<img width="1156" height="402" alt="image" src="https://github.com/user-attachments/assets/7dc17dee-6a0a-41de-b31d-e7964726b9e1" />
<img width="1381" height="83" alt="image" src="https://github.com/user-attachments/assets/b0ae9d2e-c885-424c-b3c2-ff6a216fa515" />

3. Create some data inside it (a table, a few rows — anything)
4. 
<img width="817" height="175" alt="image" src="https://github.com/user-attachments/assets/342aec8c-1799-4a13-bd33-5f1c2272471f" />

5. Stop and remove the container
6. 
<img width="422" height="162" alt="image" src="https://github.com/user-attachments/assets/f16cf307-3f81-4ec9-bd63-a2ddc6bebaea" />

7. Run a new one — is your data still there?
8. 
<img width="1173" height="419" alt="image" src="https://github.com/user-attachments/assets/f966ae83-0bd2-4a8b-b3d2-15b5a056e719" />

Q. Write what happened and why.
  ---> After Deleting the Image the data was lost and the table does not exists anymore because Data is stored inside container filesystem so when container is deleted the data is deleted permenantly 

---

### Task 2: Named Volumes

1. Create a named volume

<img width="698" height="173" alt="image" src="https://github.com/user-attachments/assets/562966ce-88d1-4647-8623-9e6e08c91144" />

2. Run the same database container, but this time **attach the volume** to it
3. 
<img width="722" height="140" alt="image" src="https://github.com/user-attachments/assets/e46af7bc-c34f-413c-8b96-c032b8a8d81d" />

4. Add some data, stop and remove the container
5. 
  <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8db191d7-0cea-40c8-8fd6-6fbf750d9ad9" />
<img width="456" height="337" alt="image" src="https://github.com/user-attachments/assets/2160b4a6-7a7f-41ac-90ba-348f18d730fc" />
  <img width="456" height="337" alt="image" src="https://github.com/user-attachments/assets/0db49d94-6d7a-49cc-9b96-f8924aba4e2f" />

6. Run a brand new container with the **same volume**
7. 
<img width="1911" height="908" alt="image" src="https://github.com/user-attachments/assets/e1dc42ad-c9a5-4a6f-b7d8-cc0f117c32d7" />

8. Is the data still there?
Yes the same Data is still there → Volume working perfectly

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






