<img width="1453" height="112" alt="image" src="https://github.com/user-attachments/assets/0c1c3a82-fe75-4cfb-933f-31b39ea83776" />## Challenge Tasks

### Task 1: Install & Verify
1. Check if Docker Compose is available on your machine
2. Verify the version
<img width="583" height="76" alt="image" src="https://github.com/user-attachments/assets/3edd200f-5c39-4984-8d1b-b0ca9cbadd3a" />

---

### Task 2: Your First Compose File
1. Create a folder `compose-basics`
<img width="573" height="63" alt="image" src="https://github.com/user-attachments/assets/c4e07c4c-8ee2-41c3-8322-6c4eaf3db16d" />

2. Write a `docker-compose.yml` that runs a single **Nginx** container with port mapping
<img width="390" height="215" alt="image" src="https://github.com/user-attachments/assets/473aa3f6-3251-4e1d-a9bf-ba38ee238fb5" />

3. Start it with `docker compose up`
<img width="1464" height="754" alt="image" src="https://github.com/user-attachments/assets/8ebc7358-bc21-46c5-8315-5f71a43b81c9" />

4. Access it in your browser
<img width="1919" height="336" alt="image" src="https://github.com/user-attachments/assets/356f395f-e839-468a-9100-9f30b191ce36" />

5. Stop it with `docker compose down`
<img width="1453" height="112" alt="image" src="https://github.com/user-attachments/assets/0826e88f-7eb9-4ddb-8da9-d50658d0c482" />

---

### Task 3: Two-Container Setup
Write a `docker-compose.yml` that runs:
- A **WordPress** container
- A **MySQL** container
  
<img width="423" height="644" alt="image" src="https://github.com/user-attachments/assets/1b70a047-19c7-4d9d-afa8-f225b40957a7" />

<img width="1480" height="215" alt="image" src="https://github.com/user-attachments/assets/5a569f85-6c4f-44be-ad96-9be65930db4e" />

They should:
- Be on the same network (Compose does this automatically)
- MySQL should have a named volume for data persistence
- WordPress should connect to MySQL using the service name

- <img width="1919" height="1045" alt="image" src="https://github.com/user-attachments/assets/06a5c007-75ed-4626-bf4d-dbb38a1872cf" />

Start it, access WordPress in your browser, and set it up.

**Verify:** Stop and restart with `docker compose down` and `docker compose up` — is your WordPress data still there?

<img width="1919" height="288" alt="image" src="https://github.com/user-attachments/assets/e606d4e6-7a5a-4d65-b925-dd7c8b1ab2fd" />

Yes the WordPress site + data is still here safe. it worked because 
- db_data = named volume → MySQL data persists.
- db = service name → used as hostname.
- Compose auto-creates network → containers talk easily.

---

### Task 4: Compose Commands

Practice and document these:

1. Start services in **detached mode**

<img width="1510" height="160" alt="image" src="https://github.com/user-attachments/assets/a1f48dcd-2e5b-4657-ad24-ca8c503154fa" />

2. View running services

<img width="1458" height="127" alt="image" src="https://github.com/user-attachments/assets/52020f6f-efd5-4b97-935a-d483342e0c5e" />

3. View **logs** of all services

<img width="1916" height="836" alt="image" src="https://github.com/user-attachments/assets/8015fa1e-9a99-4a4e-92b9-bf43c3825726" />

4. View logs of a **specific** service

<img width="1919" height="650" alt="image" src="https://github.com/user-attachments/assets/8191ed11-71dc-4be2-bfad-ad7517a09558" />

5. **Stop** services without removing

<img width="1621" height="169" alt="image" src="https://github.com/user-attachments/assets/03eb19d0-3f38-44cf-9ed1-a623795aabdd" />

6. **Remove** everything (containers, networks)

<img width="1621" height="169" alt="image" src="https://github.com/user-attachments/assets/40ef50e3-192d-42b3-9426-421793353d03" />

7. **Rebuild** images if you make a change

<img width="1479" height="223" alt="image" src="https://github.com/user-attachments/assets/06146145-6e92-419c-b5b1-01c8b9a3f873" />

---

### Task 5: Environment Variables

1. Add environment variables directly in your `docker-compose.yml`

<img width="301" height="144" alt="image" src="https://github.com/user-attachments/assets/9d789487-182a-4d74-a975-82d10c9547b9" />

2. Create a `.env` file and reference variables from it in your compose file

<img width="471" height="531" alt="image" src="https://github.com/user-attachments/assets/d1098382-1af0-4e9e-8149-081b8c619598" />

3. Verify the variables are being picked up

<img width="1477" height="202" alt="image" src="https://github.com/user-attachments/assets/e81579b7-6e35-4b46-af74-8b4fb873e5c8" />

---
