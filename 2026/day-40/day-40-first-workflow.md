## Challenge Tasks

### Task 1: Set Up

1. Create a new **public** GitHub repository called `github-actions-practice`
2. Clone it locally
3. Create the folder structure: `.github/workflows/`
<br></br>
<img width="850" height="249" alt="image" src="https://github.com/user-attachments/assets/1d134c98-bc91-42e8-8edf-b2459f68e105" />
<br></br>
[Github Repo](https://github.com/AaryAd26/github-action-TWS)

---

### Task 2: Hello Workflow

Create `.github/workflows/hello.yml` with a workflow that:
1. Triggers on every `push`
2. Has one job called `greet`
3. Runs on `ubuntu-latest`
4. Has two steps:
   - Step 1: Check out the code using `actions/checkout`
   - Step 2: Print `Hello from GitHub Actions!`
<br></br>
<img width="528" height="349" alt="image" src="https://github.com/user-attachments/assets/cf95930b-4c08-4bd7-ab1b-2e9aec91a8af" />

Push it. Go to the **Actions** tab on GitHub and watch it run.

**Verify:** Is it green? Click into the job and read every step.
<br></br>
<img width="1149" height="136" alt="image" src="https://github.com/user-attachments/assets/6c9202f9-1735-4630-ab4f-6d6e2fc2c487" />

<br></br>
<img width="943" height="613" alt="image" src="https://github.com/user-attachments/assets/8d266d44-ac2d-4502-bb6c-0f94b690c3ec" />

---

### Task 3: Understand the Anatomy

Look at your workflow file and write in your notes what each key does:
- `on:` 
  - Defines the events(push,pull_request) that trigger the workflow to run.

- `jobs:`
  - A collection of one or more jobs. Runs parallely by default.

- `runs-on:`
  - Github's or selfhosted environment that provides container or virtual machine for a job to execute.

- `steps:`
  - A ordered list of tasks within a job.

- `uses:`
  - Refers to pre-built GitHub Actions or reusable workflows.

- `run:`
  - Executes a command or a script in the runner's shell.

- `name:` (on a step)
  - A name given to that steps.
  
---

### Task 4: Add More Steps

Update `hello.yml` to also:
1. Print the current date and time
2. Print the name of the branch that triggered the run (hint: GitHub provides this as a variable)
3. List the files in the repo
4. Print the runner's operating system

Push again — watch the new run.
<br></br> <img width="1386" height="777" alt="image" src="https://github.com/user-attachments/assets/ea5f8a5c-9a1a-4236-97b7-480d220036f5" />

---

### Task 5: Break It On Purpose

1. Add a step that runs a command that will **fail** (e.g., `exit 1` or a misspelled command)
2. Push and observe what happens in the Actions tab
3. Fix it and push again

  - Error :
<br></br><img width="993" height="878" alt="image" src="https://github.com/user-attachments/assets/fc6e190c-895d-41b6-862b-478254402b6c" />

  - After solving error :
<br></br><img width="826" height="740" alt="image" src="https://github.com/user-attachments/assets/66f5e1e1-c73e-4045-97c6-b1b9af8d2baf" />


---
