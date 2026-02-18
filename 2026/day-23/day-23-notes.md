# **Challenge Tasks**

# **Task 1: Understanding Branches**

1. What is a branch in Git?
> Branch in git is a Different line of Development used for Expimenting new Features in Same Repo without harming the main Branch. We can also say that if we are creating a new feature then we can try it out first in different branch and test it before pushing the code to the main Branch 

2. Why do we use branches instead of committing everything to main?
> We use Branches instead of commiting everything to main because if someday or sometime a code get an Error which can leak something sensitive or we commit a piece of code having bug then it can harm our main brnach and if the main branch is in Production our deployment can fail.

3. What is HEAD in Git?
>In Git, HEAD is a symbolic reference (a pointer) to the commit you are currently working on. It is Git's way of knowing where you are in the project's history and serves as the parent of the next commit you create.

4.What happens to your files when you switch branches?
> When we switch git branches the git updates the current working directory to match the commit of a new branch.
> Untracked files from previous branch remain untouched.
> taged files from previous branch need to be stashed, otherwise git may block switch to avoid overwriting.

# **Task 2: Branching Commands — Hands-On**

1. List all branches in your repo
2. Create a new branch called feature-1
3. Switch to feature-1
4. Create a new branch and switch to it in a single command — call it feature-2
5. Try using git switch to move between branches — how is it different from git checkout?
6. Make a commit on feature-1 that does not exist on main
7. Switch back to main — verify that the commit from feature-1 is not there
8. Delete a branch you no longer need
9. Add all branching commands to your git-commands.md

<img width="1110" height="618" alt="Screenshot 2026-02-18 234121" src="https://github.com/user-attachments/assets/946331cb-7c1a-4ca4-9e8a-0982d8888eba" />

<img width="838" height="1079" alt="image" src="https://github.com/user-attachments/assets/5ce1d80f-1129-4967-99f4-f07e98564e60" />

# **Task 3: Push to GitHub**

1. Create a new repository on GitHub (do NOT initialize it with a README)
2. Connect your local devops-git-practice repo to the GitHub remote
3. Push your main branch to GitHub
4. Push feature-1 branch to GitHub
5. Verify both branches are visible on GitHub
6. Answer in your notes: What is the difference between origin and upstream?

<img width="1044" height="807" alt="image" src="https://github.com/user-attachments/assets/27e17745-e841-4c64-98d3-77f8a66e499e" />

<img width="841" height="531" alt="image" src="https://github.com/user-attachments/assets/a3aad909-876f-47d4-8af4-1942515d5b15" />

# **ask 4: Pull from GitHub**

1. Make a change to a file directly on GitHub (use the GitHub editor)
2. Pull that change to your local repo
3. Answer in your notes: What is the difference between git fetch and git pull?

git fetch -  Only downloads changes from the remote. It does not merge them into your local branch. The fetched commit reference is saved in the FETCH_HEAD file.
gi pull - it pulls the branch from remote to the local also it downloades and and merge them 

# **Task 5: Clone vs Fork**

1. Clone any public repository from GitHub to your local machine
2. Fork the same repository on GitHub, then clone your fork
3. Answer in your notes:
   > What is the difference between clone and fork?
- Clone : Suppose we want a particular project to be changes and want that to be in our local then we clone the full project from **remote to local **
- Fork : When we want a repository From a **Remote to our Remote** we fork the repository in GitHub

   > When would you clone vs fork?
- Clone : When i want a Publically accessable repo to my Local Then i will clone repository.
- Fork : When i want a Public repository to my remote then i will Fork 
 
   > After forking, how do you keep your fork in sync with the original repo?
- There is a option avilable on GitHub, SyncFork. You can update a fork using that option.




