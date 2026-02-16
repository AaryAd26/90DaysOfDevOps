# **Challenge Tasks**
# **Task 1: Install and Configure Git**

1. Verify Git is installed on your machine
2. Set up your Git identity — name and email
3. Verify your configuration

<img width="388" height="142" alt="image" src="https://github.com/user-attachments/assets/e3f52fee-b69c-42fb-bda9-d8665bd0ba8f" />


# **Task 2: Create Your Git Project**

1. Create a new folder called devops-git-practice.
2. Initialize it as a Git repository.
3.  Check the status — read and understand what Git is telling you.
4.  Explore the hidden .git/ directory — look at what's inside

<img width="749" height="475" alt="image" src="https://github.com/user-attachments/assets/e181d123-7cf1-49a6-8f98-7f378194cbb1" />

# **Task 3: Create Your Git Commands Reference**

1. Create a file called git-commands.md inside the repo
2. Add the Git commands you've used so far, organized by category:
    - Setup & Config
    -Basic Workflow
    - Viewing Changes
3.For each command, write:
    -What it does (1 line)
    -An example of how to use it

<img width="758" height="231" alt="image" src="https://github.com/user-attachments/assets/71de5e71-93b6-4a97-bb9e-2708b4c8823e" />

<img width="1112" height="620" alt="image" src="https://github.com/user-attachments/assets/29206884-b706-4363-bd3f-33df35dac1b0" />

# **Task 4: Stage and Commit**

1. Stage your file
2. Check what's staged
3. Commit with a meaningful message
4. View your commit history

<img width="876" height="446" alt="image" src="https://github.com/user-attachments/assets/77cb0467-003f-4c6d-9cba-967f756ec235" />

# **Task 5: Make More Changes and Build History**

1. Edit git-commands.md — add more commands as you discover them
2. Check what changed since your last commit
3. Stage and commit again with a different, descriptive message
4. Repeat this process at least 3 times so you have multiple commits in your history
5. View the full history in a compact format

<img width="573" height="164" alt="image" src="https://github.com/user-attachments/assets/2cfaed90-81c1-46d1-84d8-843b9897b303" />

<img width="1109" height="627" alt="Screenshot 2026-02-17 010920" src="https://github.com/user-attachments/assets/bfa5fe10-591d-4834-ad92-68b020755b82" />

# **Task 6: Understand the Git Workflow**

1. What is the difference between git add and git commit?
-- The Git add keeps file in staging area. So it can be included in next commit.
-- git commit command is used to commit a tracked file to a repo with a message. Creates a new commit with commit id.

2. What does the staging area do? Why doesn't Git just commit directly?
-Staging area stores files/changes that need to be added in next commit.
-That is why staging is needed, So if I added something mistakenly it can be unstaged without any mess. Also we can commit multiple changes with single commit.
-What if I accidentally added something, and it gets committed.

3. What information does git log show you?
- it Shows us a Commit id which is generated everytime we commit a file Basically History

4. What is the .git/ folder and what happens if you delete it?
-git folder stores the complete history of your repository, holds config file, hooks. If you delete .
-git folder, your project history is gone. Nothing can be tracked. 

5. What is the difference between a working directory, staging area, and repository?
- staging area - After adding files to staging area it can be committed and traced.
- repository - All your commites, branches is your repository. Basically history of your working directory with version control.
- working directory - It is your project directory. Where you write files. Changes here are not tracked until you add,commit.





