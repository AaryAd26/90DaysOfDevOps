## Challenge Tasks

### Task 1: Multi-Job Workflow
Create `.github/workflows/multi-job.yml` with 3 jobs:
- `build` — prints "Building the app"
- `test` — prints "Running tests"
- `deploy` — prints "Deploying"

Make `test` run only **after** `build` succeeds.
Make `deploy` run only **after** `test` succeeds.

**Verify:** Check the workflow graph in the Actions tab — does it show the dependency chain?
<br></br>
[Multiple Jobs Workflow](https://github.com/AaryAd26/github-action-task/blob/main/.github/workflows/multi-job-workflow.yml)
<br></br>
<img width="1202" height="499" alt="image" src="https://github.com/user-attachments/assets/58dc16dd-0d4d-4fb9-bd52-c4204e651634" />
<br></br>

---

### Task 2: Environment Variables
In a new workflow, use environment variables at 3 levels:
1. **Workflow level** — `APP_NAME: myapp`
2. **Job level** — `ENVIRONMENT: staging`
3. **Step level** — `VERSION: 1.0.0`

Print all three in a single step and verify each is accessible.

Then use a **GitHub context variable** — print the commit SHA and the actor (who triggered the run).
<br></br>
[Environment variable yml](https://github.com/AaryAd26/github-action-task/blob/main/.github/workflows/test-env.yml)
<br></br>
<img width="709" height="377" alt="image" src="https://github.com/user-attachments/assets/feea881c-0439-4024-8f88-d841b0ad1c8e" />

---

### Task 3: Job Outputs
1. Create a job that **sets an output** — e.g., today's date as a string
2. Create a second job that **reads that output** and prints it
3. Pass the value using `outputs:` and `needs.<job>.outputs.<name>`

Write in your notes: Why would you pass outputs between jobs?
<br></br>
[Passing jobs output yml](https://github.com/AaryAd26/github-action-task/blob/main/.github/workflows/job-output.yml)
<br></br>
<img width="695" height="216" alt="image" src="https://github.com/user-attachments/assets/9f0c9881-f42a-4d41-9933-793535074fe4" />

---

### Task 4: Conditionals
In a workflow, add:
1. A step that only runs when the branch is `main`
<br></br>
<img width="333" height="257" alt="image" src="https://github.com/user-attachments/assets/e248f540-3b74-4be1-83f3-1b77223cb710" />
<br></br>
2. A step that only runs when the previous step **failed**
<br></br>
<img width="354" height="307" alt="image" src="https://github.com/user-attachments/assets/4df5eefb-4d65-4ba8-bb87-391127db17ad" />
<br></br>
3. A job that only runs on **push** events, not on pull requests
<br></br>
4. A step with `continue-on-error: true` — what does this do?
<br></br>
<img width="441" height="354" alt="image" src="https://github.com/user-attachments/assets/6875058b-f490-4c17-94ab-68aa4ba48a17" />
<br></br>
[conditions yml file](https://github.com/AaryAd26/github-action-task/blob/main/.github/workflows/conditions.yml)

---

### Task 5: Putting It Together
Create `.github/workflows/smart-pipeline.yml` that:
1. Triggers on push to any branch
2. Has a `lint` job and a `test` job running in parallel
3. Has a `summary` job that runs after both, prints whether it's a `main` branch push or a feature branch push, and prints the commit message

[smart-pipeline yml file](https://github.com/AaryAd26/github-action-task/blob/main/.github/workflows/dedicated-pipeline.yml)
<br></br>

<img width="395" height="451" alt="image" src="https://github.com/user-attachments/assets/2a04c665-fa14-4c01-88c4-0a96f77496be" />

<br></br>

<img width="606" height="473" alt="image" src="https://github.com/user-attachments/assets/944bcb06-1bae-4ae2-a079-a896eafb9b94" />

<br></br>

- summary<br></br>
  <img width="321" height="301" alt="image" src="https://github.com/user-attachments/assets/03ca2c69-777f-4a46-bb14-bb650fd11ec7" />

---
