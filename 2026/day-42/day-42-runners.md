<img width="986" height="588" alt="Screenshot 2026-05-13 145709" src="https://github.com/user-attachments/assets/049b7d8f-a5c6-480f-95d2-db927d56936f" />## Challenge Tasks

### Task 1: GitHub-Hosted Runners
1. Create a workflow with 3 jobs, each on a different OS:
   - `ubuntu-latest`
   - `windows-latest`
   - `macos-latest`
2. In each job, print:
   - The OS name
   - The runner's hostname
   - The current user running the job
3. Watch all 3 run in parallel
<br></br>
<img width="986" height="588" alt="Screenshot 2026-05-13 145709" src="https://github.com/user-attachments/assets/3d20e19b-b16d-4e23-bfd8-160b61862a93" />
<br></br>
<img width="948" height="677" alt="image" src="https://github.com/user-attachments/assets/6ea3fa99-e6ab-4f71-845b-bc07d45f746c" />

Write in your notes: What is a GitHub-hosted runner? Who manages it?
- A GitHub‑hosted runner is a temporary virtual machine (VM) or container that GitHub provides to execute your workflow jobs.
- It spins up fresh for each job, and comes preinstalled with common tools, languages.
- After job completion runner is discarded.
- GitHub manages it entirely on Microsoft Azure Infrastructure as GitHub is owned by Microsoft.

---

### Task 2: Explore What's Pre-installed
1. On the `ubuntu-latest` runner, run a step that prints:
   - Docker version
   - Python version
   - Node version
   - Git version
2. Look up the GitHub docs for the full list of pre-installed software on `ubuntu-latest`
 
[Pre-installed yaml file](https://github.com/AaryAd26/github-action-task/blob/main/.github/workflows/pre-install.yml)
<br></br>
<img width="1005" height="587" alt="image" src="https://github.com/user-attachments/assets/067f9267-4a69-4fda-bb87-7855085fd674" />
<br></br>
Write in your notes: Why does it matter that runners come with tools pre-installed?

-Certain tools & languages needs to be pre-installed for smooth & fast workflow run. For example, code checkout needs git, building needs docker. It saves writing long setup steps & installing them.
---

### Task 3: Set Up a Self-Hosted Runner
1. Go to your GitHub repo → Settings → Actions → Runners → **New self-hosted runner**
2. Choose Linux as the OS
3. Follow the instructions to download and configure the runner on:
   - Your local machine, OR
   - A cloud VM (EC2, Utho, or any VPS)
4. Start the runner — verify it shows as **Idle** in GitHub

**Verify:** Your runner appears in the Runners list with a green dot.

---

### Task 4: Use Your Self-Hosted Runner
1. Create `.github/workflows/self-hosted.yml`
2. Set `runs-on: self-hosted`
3. Add steps that:
   - Print the hostname of the machine (it should be YOUR machine/VM)
   - Print the working directory
   - Create a file and verify it exists on your machine after the run
4. Trigger it and watch it run on your own hardware

**Verify:** Check your machine — is the file there?

---

### Task 5: Labels
1. Add a **label** to your self-hosted runner (e.g., `my-linux-runner`)
2. Update your workflow to use `runs-on: [self-hosted, my-linux-runner]`
3. Trigger it — does it still pick up the job?

Write in your notes: Why are labels useful when you have multiple self-hosted runners?

---

### Task 6: GitHub-Hosted vs Self-Hosted
Fill this in your notes:

| | GitHub-Hosted | Self-Hosted |
|---|---|---|
| Who manages it? | ? | ? |
| Cost | ? | ? |
| Pre-installed tools | ? | ? |
| Good for | ? | ? |
| Security concern | ? | ? |

---  
