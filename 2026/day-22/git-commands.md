# **List of Commands I am Using**

1.  git --version -- used for cheking if git is installed if yes whats its current version installed.
2.  git config -l -- used for setting up our git identity, name & email.
3.  git init -- used for initializing a empty git repo
4.  git status -- used to check that on which braanch we are currently working and also tell that if there any files that are untracked and ready for commit.
5.  git commit -m "Message" - This command is used to commit a file to a Repo. with a Message
6.  git add <file name> / git add . - we can used both commands where if we want a single file to be commited we add that filewith git add <file name> and ifwe want all file to be commited then we use git add  . command
7.  git add <file name> / git add . - we can used both commands where if we want a single file to be commited we add that filewith git add <file name> and if we want all file to be commited then we use git add  . command
8.  git log --online - Tells us about the full Commit history in compact form where it shows the tracking id.
9.  git revert commit-id - creates new commit that undoes changes made by given commit
10. git clone <url> - Clones a Already Exists GitHub repo
11. git checkout -b "<branch name>" -  Creates a New Branch in the existing Repo
12. git switch <branch name> - This command is used to seitch between multiple branches.
13. git branch - list all branches in the Repositories
14. git reset commit-id	reset head back till given commit id
15. git branch -D <branch>	delete a branch
16. git rebase <branch>	creates a linear history for current branch
17. git log --oneline --graph --all	shows history of all branches in graph
18. git stash	stash your current changes and switch to another branch
19. git cherry-pick <commit-id>	pick and apply one commit from multiple commits to another branch
20. git merge <branch> --squash	combine multiple commits to one and merge
21. git stash pop	get changes to working directory and deletes stash
22. git stash apply	get changes to working directory also keeps stash
