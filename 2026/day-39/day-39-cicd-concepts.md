## Challenge Tasks

### Task 1: The Problem
Think about a team of 5 developers all pushing code to the same repo manually deploying to production.

Write in your notes:
1. What can go wrong?
- There may be a Merge Conflicts because there may be a scenario that 2 dev can push code at a same time.
- manual errors can take place as the deploying.
- Chances of Getting bugs will be high.
- There may be a Downtime because it requires a server restart.

2. What does "it works on my machine" mean and why is it a real problem?
- "it works on my machine" means that:
- the code is only working in your local machine the internet world outside cannot see the work you have done.
- It happes because of difference in dependencies, OS versions, libraries, database schemas.
- It leads to wasted debugging time, finger-pointing, and unstable deployments

3. How many times a day can a team safely deploy manually?
- 2-3 times a team can safely deploy manually, more than this it will be too much of manual errors.
- Because each manual deployment requires checks, downtime windows and human oversight.
- More frequent deployment increases the chance of mistkes and production instability.

---

### Task 2: CI vs CD

Research and write short definitions (2-3 lines each):
1. **Continuous Integration** — what happens, how often, what it catches
- continuous integration means a pulling the latest code which is pushed to github is continusously checking out the code, doing the manual checks and and building a Docker Image
- In Continuous Integration the CI part validates the uni test.
- We can do this Every time a code is pushed, multiple times a day.
- It cateches Compiling errors, logic errors, integration issues, environment drift.
- Engineers commit code most of times per day. Every commit triggers automated builds and tests across thousands of servers.

- For Ex: Facebook , there are daily code pushed to cloud which runs the test and triggers the pipeline.

2. **Continuous Delivery** — how it's different from CI, what "delivery" means
- CI stops at code works and passes tests.
- In Continuous Delivery the Docker image which is created is the pushed to Docker Hub and from their the image is pulled back.
- CD ensures the code packaged, versioned and ready to be deployed to production at any time.
- Delivery gurantees production readiness at anytime

- For Ex: Amazon :  

3. **Continuous Deployment** — how it differs from Delivery, when teams use it
- In Continuous Deployment it is used to automate the deployment for every change that passes a test direrctly to production with human intervation.
- whenever the test are passed the code is then ready for the deployment and the deployment part is automated.
- automating the deployment where the use of Human is not required then it is called the Contoinuos deployment.

- For Ex: Netflix : Code that passes automated tests is automatically deployed to production without human approval. It relies on strong monitoring, canary releases and rollback systems.

Write one real-world example for each.

---

### Task 3: Pipeline Anatomy
A pipeline has these parts — write what each one does:

- **Trigger** — what starts the pipeline
  - In trigger we have to set a trigger point from where the CI part should star. for ex: we say whenever the code is pushed to the main branch of Github then the pipeline must be triggered
  - It can a push, pull request, sceduled cron job, manual action.

- **Stage** — a logical phase (build, test, deploy)
  - A logical grouping of jobs, organizes the pipeline into clear phases(build, test, deploy) for readability and control.
  
- **Job** — a unit of work inside a stage
   - A set of steps executes on the same runner. By Default, multiple jobs run simuntenously until you tel them to wait for each other.

- **Step** — a single command or action inside a job
   - it is a sequential of commands within the job.
   - it is mainly used to sequencing the job.

- **Runner** — the machine that executes the job
   - it is a machine that executes the job. We say it Runner because it runs the job.

- **Artifact** — output produced by a job
   - An output produced by a job, stored for later use.
   - Examples: Docker image, compiled binaries.
   - Allows sharing results between stages(build->test->deploy)

---

### Task 4: Draw a Pipeline
Draw a CI/CD pipeline for this scenario:
> A developer pushes code to GitHub. The app is tested, built into a Docker image, and deployed to a staging server.
<br></br>
<img width="1210" height="827" alt="Screenshot 2026-04-26 140038" src="https://github.com/user-attachments/assets/86f7bcb5-8437-4575-b7fe-f77678e5c753" />
<br></br>
Include at least 3 stages. Hand-drawn and photographed is perfectly fine.

---

### Task 5: Explore in the Wild

1. Open any popular open-source repo on GitHub (Kubernetes, React, FastAPI — pick one you know)

2. Find their `.github/workflows/` folder

3. Open one workflow YAML file

4. Write in your notes:
- Choosing : https://github.com/kubernetes/minikube/blob/master/.github/workflows/build.yml

   - What triggers it?
     - Push on branch master, pushed only on specified files.

    - How many jobs does it have?
     - it Has 3 jobs in the workflow. 
 
   - What does it do? (best guess)
     - First job build_minikube: It uses ubuntu 22.04 runner, checkouts the code, set-up environemnt.
        - download dependncies, builds binaries and uploads artifact.
     
     - Second job : checks code for style, formatting, and common errors before it runs.
    
     - Third job : Does unit test(verifies the smallest pieces of code behaves as expected) 
---
