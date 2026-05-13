## Challenge Tasks

### Task 1: Trigger on Pull Request
1. Create `.github/workflows/pr-check.yml`
2. Trigger it only when a pull request is **opened or updated** against `main`
3. Add a step that prints: `PR check running for branch: <branch name>`
4. Create a new branch, push a commit, and open a PR
5. Watch the workflow run automatically
<br></br>
<img width="641" height="355" alt="image" src="https://github.com/user-attachments/assets/cdf94867-9d3a-409e-b6f5-98c093a6e663" />
<br></br>
**Verify:** Does it show up on the PR page?

---

### Task 2: Scheduled Trigger
1. Add a `schedule:` trigger to any workflow using cron syntax
2. Set it to run every day at midnight UTC
3. Write in your notes: What is the cron expression for every Monday at 9 AM?

    > 0 9 * * 1  
<br></br>
<img width="468" height="321" alt="image" src="https://github.com/user-attachments/assets/8589d54d-bbee-4a36-bf61-8f7d00746682" />

---

### Task  3: Manual Trigger
1. Create `.github/workflows/manual.yml` with a `workflow_dispatch:` trigger
2. Add an **input** that asks for an `environment` name (staging/production)
3. Print the input value in a step
4. Go to the **Actions** tab → find the workflow → click **Run workflow**
<br></br>
<img width="617" height="421" alt="image" src="https://github.com/user-attachments/assets/1b710f6f-0abd-4f53-9a27-7840e0974c9a" />
<br></br>
**Verify:** Can you trigger it manually and see your input printed?
<br></br>
<img width="901" height="338" alt="image" src="https://github.com/user-attachments/assets/bc778cbb-dff5-4349-b9a7-888ef37b7463" />

---

### Task 4: Matrix Builds
Create `.github/workflows/matrix.yml` that:
1. Uses a matrix strategy to run the same job across:
   - Python versions: `3.10`, `3.11`, `3.12`
2. Each job installs Python and prints the version
3. Watch all 3 run in parallel

<img width="689" height="693" alt="image" src="https://github.com/user-attachments/assets/d36dd574-b674-42a7-b506-67a43f22846a" />

Then extend the matrix to also include 2 operating systems — how many total jobs run now?

<img width="1208" height="571" alt="image" src="https://github.com/user-attachments/assets/2beccfc0-590a-4d27-9d71-42b4e6311753" />
<br></br>
<img width="936" height="349" alt="image" src="https://github.com/user-attachments/assets/88675e69-d4b1-4787-bc91-04df65b43762" />

---

### Task 5: Exclude & Fail-Fast
1. In your matrix, **exclude** one specific combination (e.g., Python 3.10 on Windows)
- After adding exclude for python-3.10 on macos it skipped that job.
<br></br>
<img width="289" height="320" alt="image" src="https://github.com/user-attachments/assets/a4e52c25-9f7e-4d06-8614-6bd4a0ebe2e4" />
<br></br>

2. Set `fail-fast: false` — trigger a failure in one job and observe what happens to the rest
- fal-fast: false
<br></br>
<img width="303" height="390" alt="image" src="https://github.com/user-attachments/assets/9e26dde0-dfb1-409c-a055-a8ee8b59ed75" />
<br></br>
- fail-fast: true
<br></br>
<img width="283" height="381" alt="image" src="https://github.com/user-attachments/assets/64994474-2f27-4d66-9071-6db01400d29d" />
<br></br>

3. Write in your notes: What does `fail-fast: true` (the default) do vs `false`?
- fail-fast: true: If one job in matrix fails other remaining jobs are automatically cancelled.
- fail-fast: false: Even if one job fails in matrix other jobs continue running until completion.
<br></br>
<img width="581" height="571" alt="image" src="https://github.com/user-attachments/assets/065813b2-21cc-4113-b53c-ef45e0555c0c" />

---
