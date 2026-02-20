<img width="877" height="1079" alt="image" src="https://github.com/user-attachments/assets/ca33d180-5a78-45dd-a947-0d8fc1b420a2" /># **Day 24 – Advanced Git: Merge, Rebase, Stash & Cherry Pick**

# **Challenge Tasks**
****Task 1: Git Merge — Hands-On****

1. Create a new branch feature-login from main, add a couple of commits to it
2. Switch back to main and merge feature-login into main
3. Observe the merge — did Git do a fast-forward merge or a merge commit?
4. Now create another branch feature-signup, add commits to it — but also add a commit to main before merging
5. Merge feature-signup into main — what happens this time?
6. Answer in your notes:
   -What is a fast-forward merge?
- Fast Forward merge means it merges 2 branches withhout creating a new commit in the branch, moves the current branch’s pointer to match the branch being merged.
   
   -When does Git create a merge commit instead?
- When you try to merge two branches that have diverged. Git makes a new commit to combine the incoming changes.

   -What is a merge conflict? (try creating one intentionally by editing the same line in both branches)
- Merge Conflicts mean when we try to change the same part of file in 2 differetn branches beacuse while merging the branches git cannot automnatically decide which brnach to keep.

<img width="877" height="1079" alt="image" src="https://github.com/user-attachments/assets/979d4a50-6b4b-420b-8f4e-c8e05bc951f5" />

<img width="766" height="1079" alt="image" src="https://github.com/user-attachments/assets/f19ce7e3-f2ac-4a86-b2a4-7d8cffffab52" />


# **Task 2: Git Rebase — Hands-On**

1. Create a branch feature-dashboard from main, add 2-3 commits
2. While on main, add a new commit (so main moves ahead)
3. Switch to feature-dashboard and rebase it onto main
4. Observe your git log --oneline --graph --all — how does the history look compared to a merge?
5. Answer in your notes:
   - What does rebase actually do to your commits?
- Git rebase is used to integrate change from one git branch to another by moving or reapplying a series of commit to a new base commit.

   - How is the history different from a merge?
- Merge does not create a history it shows the commits we have done on a specific branch. Rebase rewrites commit history by reapplying feature commits on top of the latest main branch, creating a clean, linear, and non-branching history.
  
   - Why should you never rebase commits that have been pushed and shared with others?
 - Because rebase creates entirely new commit hashes, it breaks the link with colleagues' local copies, leading to, complex, unresolvable merge conflicts, duplicate commits, and lost work.
 
   - When would you use rebase vs merge?
 - Merge, as it preserves when the commit was exactly made.

<img width="862" height="1070" alt="image" src="https://github.com/user-attachments/assets/4a8ff0f6-7bf3-4a3e-adf9-24eb4f3aa0be" />

# **Task 3: Squash Commit vs Merge Comm**it

1. reate a branch feature-profile, add 4-5 small commits (typo fix, formatting, etc.)
2. Merge it into main using --squash — what happens?
3. Check git log — how many commits were added to main?
4. Now create another branch feature-settings, add a few commits
5. Merge it into main without --squash (regular merge) — compare the history
6. Answer in your notes:
   - What does squash merging do?
- Squash Merge in git means that combinig multiple sequential commit into a single, Cohesive commit.

    - When would you use squash merge vs regular merge?
- if a file has multiple commits then the i will use squash merge else i will use the Regular Mege 
    
   - What is the trade-off of squashing?
- Detailed commit history is lost from feature branch as only one commit will be shown in main branch.

<img width="856" height="947" alt="image" src="https://github.com/user-attachments/assets/94a942da-50e1-495d-89db-704dd7f4867e" />

<img width="758" height="899" alt="image" src="https://github.com/user-attachments/assets/94b4787a-16ae-41d7-ab87-b3d214e34959" />

# **Task 4: Git Stash — Hands-On**

1. Start making changes to a file but do not commit
2. Now imagine you need to urgently switch to another branch — try switching. What happens?
3. Use git stash to save your work-in-progress
4. Switch to another branch, do some work, switch back
5. Apply your stashed changes using git stash pop
6. Try stashing multiple times and list all stashes
7. Try applying a specific stash from the list
8. Answer in your notes:
   - What is the difference between git stash pop and git stash apply?
- git stash pop applies stash changes to your working directory and deletes the stash entry.
- git stash apply applies stash changes to your working directory but keeps the stash entry.

   - When would you use stash in a real-world workflow?
- When if i am working on a project and an urgency came up with fixing then i will use the stash command, I would stash changes from my current branch and switch to another branch to work on urgent fix first.

<img width="1005" height="1079" alt="image" src="https://github.com/user-attachments/assets/023146d7-bd71-4f19-adc7-d40ede125774" />

# **Task 5: Cherry Picking**

1. Create a branch feature-hotfix, make 3 commits with different changes
2. Switch to main
3. Cherry-pick only the second commit from feature-hotfix onto main
4. Verify with git log that only that one commit was applied
5. Answer in your notes:
  - What does cherry-pick do?
  - When would you use cherry-pick in a real project?
  - What can go wrong with cherry-picking?













