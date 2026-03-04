# Day 26 – GitHub CLI: Managing GitHub from the Terminal

---

## Task 1: Installation & Authentication

1. Install GitHub CLI (`gh`) on your system.
2. Authenticate your GitHub account using:

   gh auth login

3. Verify your login status and active account:

   gh auth status

### Authentication Methods Supported by `gh`

- Login via web browser
- Personal Access Token (PAT)

---

## Task 2: Repository Management

Practice managing repositories directly from the terminal:

1. Create a new **public repository** with a README file.
2. Clone a repository using GitHub CLI:

   gh repo clone <repo-name>

3. View repository details:

   gh repo view <repo-name>

4. List all your repositories:

   gh repo list

5. Open a repository in your default browser:

   gh repo view <repo-name> --web

6. Delete the test repository (use carefully):

   gh repo delete <repo-name>

---

## Task 3: Managing Issues

1. Create a new issue from the terminal with:
   - Title
   - Description (body)
   - Label

2. List all open issues:

   gh issue list

3. View a specific issue:

   gh issue view <issue-number>

4. Close an issue:

   gh issue close <issue-number>

### Using `gh issue` in Automation

`gh issue` can be integrated into scripts to automate workflows such as:

- Automatically creating issues on failure
- Listing and monitoring issues
- Adding comments programmatically
- Closing issues after fixes are deployed

Example commands:
- gh issue list
- gh issue comment <issue-number>
- gh issue close <issue-number>

---

## Task 4: Pull Requests (PRs)

1. Create a new branch.
2. Make changes and commit.
3. Push the branch.
4. Create a pull request entirely from the terminal:

   gh pr create

5. List all open pull requests:

   gh pr list

6. View PR details (status, reviewers, checks):

   gh pr view <pr-number>

7. Merge a pull request:

   gh pr merge <pr-number>

### Merge Methods Supported

`gh pr merge` supports:

- Merge commit
- Rebase merge
- Squash merge

### Reviewing Someone Else’s PR

- View in browser:

  gh pr view --web

- Approve from terminal:

  gh pr review <pr-number> --approve

You can also request changes or leave comments using `gh pr review`.

---

## Task 5: GitHub Actions & Workflows (Overview)

1. List workflow runs:

   gh run list

2. View the status of a specific run:

   gh run view <run-id>

### How `gh run` and `gh workflow` Help in CI/CD

They allow you to:

- Trigger workflows from scripts
- Monitor pipeline status
- Re-run failed jobs
- Automate deployments
- Integrate GitHub Actions into DevOps pipelines

This makes it possible to manage CI/CD processes directly from the terminal without opening the browser.

---

End of Day 26 Notes.
