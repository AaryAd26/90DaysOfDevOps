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
<br></br>
  ---> After Deleting the Image the data was lost and the table does not exists anymore because Data is stored inside container filesystem so when container is deleted the data is deleted permenantly 

---

### Task 2: Named Volumes

1. Create a named volume

<img width="698" height="173" alt="image" src="https://github.com/user-attachments/assets/562966ce-88d1-4647-8623-9e6e08c91144" />

2. Run the same database container, but this time **attach the volume** to it
 
<img width="722" height="140" alt="image" src="https://github.com/user-attachments/assets/e46af7bc-c34f-413c-8b96-c032b8a8d81d" />

3. Add some data, stop and remove the container

   <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8db191d7-0cea-40c8-8fd6-6fbf750d9ad9" />
<img width="456" height="337" alt="image" src="https://github.com/user-attachments/assets/2160b4a6-7a7f-41ac-90ba-348f18d730fc" />
  <img width="456" height="337" alt="image" src="https://github.com/user-attachments/assets/0db49d94-6d7a-49cc-9b96-f8924aba4e2f" />
  
4. Run a brand new container with the **same volume**
 
<img width="1911" height="908" alt="image" src="https://github.com/user-attachments/assets/e1dc42ad-c9a5-4a6f-b7d8-cc0f117c32d7" />

5. Is the data still there?<br></br>

Yes the same Data is still there → Volume working perfectly

---

### Task 3: Bind Mounts

1. Create a folder on your host machine with an `index.html` file
2. 
<img width="456" height="128" alt="image" src="https://github.com/user-attachments/assets/34d002e2-a018-4603-9979-b319802b0878" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a3636893-edf3-4ee1-a5a5-274679151feb" />

2. Run an Nginx container and **bind mount** your folder to the Nginx web directory

<img width="1768" height="661" alt="image" src="https://github.com/user-attachments/assets/2b2d77e9-2a65-4aaa-b3ee-5fb8e9ccfe44" />


3. Access the page in your browser

<img width="1919" height="974" alt="image" src="https://github.com/user-attachments/assets/ba9a2e47-5012-40da-bf5f-d78251375f9a" />

4. Edit the `index.html` on your host — refresh the browser

<img width="1419" height="145" alt="image" src="https://github.com/user-attachments/assets/4ee7d529-15ce-407f-ad1e-b7dd7241cc8c" />

**Q** Write in your notes: What is the difference between a named volume and a bind mount?    <br></br>
     ------> **Named Volume** :  Named Volume is manage by Docker and its data is store in docker internal, best use fo Named volume is that we can use it has a Database. Only drawback is that you cannot edit that file. <br></>br>
     ------> **Bind Mount** : Bind Mount is not manage by Docker and its data is store in Local files of the machine, It is mostly used in Development part. and we can do real time editing in this.
     
---

### Task 4: Docker Networking Basics

1. List all Docker networks on your machine
<img width="1419" height="145" alt="image" src="https://github.com/user-attachments/assets/41dc3d6b-d49b-4144-a784-e067fb883a9c" />

2. Inspect the default `bridge` network

<img width="569" height="138" alt="image" src="https://github.com/user-attachments/assets/f084870e-2ae3-4418-a052-2d2c686c0494" />
<img width="942" height="923" alt="image" src="https://github.com/user-attachments/assets/39cfba75-70d4-42ef-8c02-02afa34ae5ce" />

3. Run two containers on the default bridge — can they ping each other by **name**?
<img width="753" height="199" alt="image" src="https://github.com/user-attachments/assets/261f9f2d-f924-48c9-93c1-aa0d56b6f3d7" />

4. Run two containers on the default bridge — can they ping each other by **IP**?
<img width="696" height="97" alt="image" src="https://github.com/user-attachments/assets/76394661-7274-4278-9c63-660761d3a2ed" />

---

### Task 5: Custom Networks

1. Create a custom bridge network called `my-app-net`
<img width="689" height="247" alt="image" src="https://github.com/user-attachments/assets/af5cfba5-bbcf-49fe-b7cb-50640ee8ce67" />

2. Run two containers on `my-app-net`
<img width="933" height="175" alt="image" src="https://github.com/user-attachments/assets/883bd9b9-8fed-4c5d-9bd3-afba357e041b" />

3. Can they ping each other by **name** now?
<img width="766" height="576" alt="image" src="https://github.com/user-attachments/assets/3a614ba9-b180-45c4-8093-8de84c49f27b" />

4. Write in your notes: Why does custom networking allow name-based communication but the default bridge doesn't?  <br></br>
   -----> Custom Netword has a build in DNS and container resolves name automatically, also Default bridge lacks automatic DNS resolution.
---

### Task 6: Put It Together

1. Create a custom network
<img width="646" height="46" alt="image" src="https://github.com/user-attachments/assets/ecd745c6-0620-4d6f-8412-667673627408" />

2. Run a **database container** (MySQL/Postgres) on that network with a volume for data
<img width="645" height="44" alt="image" src="https://github.com/user-attachments/assets/916e3669-99eb-409f-b15b-60cb6b211e65" />

3. Run an **app container** (use any image) on the same network
<img width="595" height="152" alt="image" src="https://github.com/user-attachments/assets/6125cea9-85ed-4e91-8d02-53e751f388c3" />

5. Verify the app container can reach the database by container name
<img width="607" height="176" alt="image" src="https://github.com/user-attachments/assets/b517ccea-4f4b-4942-af4b-7aa15efdf290" />

---






