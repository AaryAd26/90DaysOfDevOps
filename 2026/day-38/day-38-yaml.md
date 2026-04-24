## Challenge Tasks

### Task 1: Key-Value Pairs
Create `person.yaml` that describes yourself with:
- `name`
- `role`
- `experience_years`
- `learning` (a boolean)

<img width="255" height="130" alt="image" src="https://github.com/user-attachments/assets/5eabedb8-facc-4144-aa47-663b12106b4c" />

**Verify:** Run `cat person.yaml` — does it look clean? No tabs?

---

### Task 2: Lists
Add to `person.yaml`:
- `tools` — a list of 5 DevOps tools you know or are learning
- `hobbies` — a list using the inline format `[item1, item2]`

<img width="318" height="337" alt="image" src="https://github.com/user-attachments/assets/43f8db10-9d87-47f0-adda-e9fa37ff79ac" />

<img width="722" height="363" alt="image" src="https://github.com/user-attachments/assets/570f66e8-3d16-4a6c-8c45-eb7353947724" />


Write in your notes: What are the two ways to write a list in YAML?

1.
```sh
tools:
  - Docker
  - Kubernetes
  - git and github
  - github actions
```
2 -
```sh
hobbies: [learning devops, cricket, swimming]
```
---

### Task 3: Nested Objects
Create `server.yaml` that describes a server:
- `server` with nested keys: `name`, `ip`, `port`
- `database` with nested keys: `host`, `name`, `credentials` (nested further: `user`, `password`)

**Verify:** Try adding a tab instead of spaces — what happens when you validate it?

 - validation error

<img width="412" height="315" alt="image" src="https://github.com/user-attachments/assets/6aefd21c-f972-44f0-98fa-d34373a852a8" />

<img width="267" height="208" alt="image" src="https://github.com/user-attachments/assets/2070fe61-07ac-4862-b702-c61dc4f7f898" />

---

### Task 4: Multi-line Strings
In `server.yaml`, add a `startup_script` field using:
1. The `|` block style (preserves newlines)
2. The `>` fold style (folds into one line)

<img width="471" height="470" alt="image" src="https://github.com/user-attachments/assets/1a669fd0-873d-47fc-a0f3-e82f5dde220d" />

<img width="509" height="287" alt="image" src="https://github.com/user-attachments/assets/c7197f55-46a7-485d-bcbd-b26cc8dc2766" />

Write in your notes: When would you use `|` vs `>`?

```sh
startup_script: |
  echo "starting server"
  systemctl start server
  systemctl status server
  echo "Done"

description: >
  This is the description to startup script.
  Script finished.
```

---

### Task 5: Validate Your YAML
1. Install `yamllint` or use an online validator
2. Validate both your YAML files
3. Intentionally break the indentation — what error do you get?
4. Fix it and validate again

**Before:**<br></br>
<img width="217" height="232" alt="image" src="https://github.com/user-attachments/assets/edfbcba3-40c4-4677-8cad-28dba7897533" />

**After:**<br></br>
<img width="261" height="231" alt="image" src="https://github.com/user-attachments/assets/6d7ee756-8dac-4b7e-8053-eca06711812f" />

---

**Before:**<br></br>
<img width="422" height="294" alt="image" src="https://github.com/user-attachments/assets/e1459733-ee96-45a3-8974-6113e6de947c" />

**After:**<br></br>
<img width="494" height="257" alt="image" src="https://github.com/user-attachments/assets/db351980-d25e-4c6a-8c0e-ea6698ae571e" />

---

### Task 6: Spot the Difference

Read both blocks and write what's wrong with the second one:
```yaml
# Block 1 - correct
name: devops
tools:
  - docker
  - kubernetes
```

```yaml
# Block 2 - broken
name: devops
tools:
- docker
  - kubernetes
```

**Correct:**

```yaml
# Block 2 - broken
name: devops
tools:
- docker
  - kubernetes   # <-- wrong indentation
```

- In Block number 1 the  indentation is correct and the nest is correctly written.
- in Block number 2 the Inconsistent indentation , docker is not properly indented under tools.
