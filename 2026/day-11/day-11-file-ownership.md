# Day 11 Challenge

## Files & Directories Created
#Users Created
-tokyo
-berlin
-nairobi
-professor

#Groups Created
-heist-team
-planners
-vault-team
-tech-team

#Files & Directories Created
-devops-file.txt
-app-logs/
-bank-heist/access-codes.txt
-bank-heist/blueprints.pdf
-bank-heist/escape-plan.txt
-heist-project/plans/strategy.conf
-heist-project/vault/gold.txt
-project-config.yml
-team-notes.txt

## Ownership Changes
-Run ls -l in your home directory.
-Identify the owner and group columns.
-Check who owns your files.
-Owner : The owner is usually the user who created the file or directory. Owner can change permission of file.
-Group : The group is a collection of users who share access to the file.

<br></br><img width="539" height="427" alt="Screenshot 2026-02-14 235411" src="https://github.com/user-attachments/assets/2a5f5bc5-6e9e-416d-8241-65397fe094c1" />

## Commands Used
1. ls -l filename : View ownership
2. sudo chown newowner filename : Change owner only
3. sudo chgrp newgroup filename : Change group only
4. sudo chown owner:group filename : Change both owner and group
5. sudo chown -R owner:group directory/ : Recursive change (directories) 
6. sudo chown :groupname filename : Change only group with chown

## What I Learned
- Managing User & Groups
- Understood file ownership
-  creating user and modyfing their ownership 
