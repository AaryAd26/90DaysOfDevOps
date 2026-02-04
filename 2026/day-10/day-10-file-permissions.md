<img width="795" height="279" alt="Screenshot 2026-02-04 211138" src="https://github.com/user-attachments/assets/a244b196-6b52-44b0-9e77-4759dc349153" /><img width="538" height="365" alt="Screenshot 2026-02-04 205549" src="https://github.com/user-attachments/assets/2f0071e3-a6c7-44f9-a4a6-4c02370b1e3f" /># Day 10 Challenge

## Files Created
- Created a empty file in my instace name devops.txt by using touch command
- Create notes.txt with some content using echo command 
- Create script.sh using vim with content: echo "Hello DevOps"
- ls -l to see permissions

<br></br><img width="538" height="365" alt="Screenshot 2026-02-04 205549" src="https://github.com/user-attachments/assets/91012aa0-2781-47cc-b587-4c48b3b4acff" />


## Permission Changes
Current permissions :
1.Devops.txt :
-rw-rw-r--
 1. - → indicates it’s a regular file (not a directory or special file).
 2. rw- → (user/owner) → read + write, no execute.
 3. rw- → (group) → read + write, no execute.
 4. r-- → (others) → read only, no write or execute.

<br></br><img width="613" height="504" alt="Screenshot 2026-02-04 210737" src="https://github.com/user-attachments/assets/3f9316f6-cca4-4921-9dde-d103be0633b3" />


#Test permission 

Q. Writing to a read-only file - what happens?

- When a file is set to read-only permission, users can view its content but cannot modify, overwrite, or delete the file.
- If someone tries to write or add content to a read-only file, the system blocks the action and displays a “Permission denied” error.
- Read-only permissions are used to protect important files from accidental changes or data loss.

<br></br><img width="795" height="279" alt="Screenshot 2026-02-04 211138" src="https://github.com/user-attachments/assets/fad7c6aa-68bf-4d32-89c0-c223fc56c919" />


Q. Try executing a file without execute permission. (I Haved done this by reading it on google and understanding it.)

-When a file does not have execute permission, the system does not allow it to run as a program or script.
-If a user tries to execute such a file, Linux shows a “Permission denied” error.
-Execute permission is required to run scripts, binaries, or programs, and it helps control who is allowed to run specific files for security and system stability.

   <br></br><img width="453" height="236" alt="Screenshot 2026-02-04 211243" src="https://github.com/user-attachments/assets/7f097fe3-f07e-4736-a86f-a04cbcf02843" />

   #Commands I Used 

1.touch fname - Creates empty file.
2. echo "Hello" > fname - Create file with content.
3. vim fname - Create/open file in Vim.
4. cat fname - Prints files content.
5. vim -R fname - Open file in read only mode.
6. cat /etc/passwd | tail -5 - Prints last 5 lines of /etc/passwd.
7. cat /etc/passwd | head -5 - Prints first 5 lines of /etc/passwd.
8. chmod -w fname - Removing write permission for all(owner,group,others).
9. chmod +x fname - Adding executable permission for all(owner,group,others).
10. mkdir -m 755 dname - Create directory with permissions(rwx,r-x,r-x).


#What i Learned 

- never giveup if you dont understand the task go through the notes and try to fighure out things yourself then ask fot help.
- learned about modifying the files persmission.
- r - for read permission.
- w - for write permission.
- x - execute permission.
- tried to understan what happends when we try to write in a read only file it shows acces denied and throws back an Error.
- Also same for trying to execute file with no execute permission.
- some new commands like echo "Read only File" | sudo tee -a devops.txt  like how it changes the permission and help in read the file which has no read permission.
