Environment basics (2):
1. unmae -a   :  basically it tells about the current local machine i am working on alongside what i am currenly using. in my case i am using WSL for ubuntu and also it is mentioning Global standard time (UTC).<br></br>
2. cat /etc/os-release  :  this command is tells is about the image we are using also its version also with its Home URl. 

<img width="1252" height="365" alt="Screenshot 2026-01-28 234644" src="https://github.com/user-attachments/assets/fbc1aa4f-cb96-4775-848c-264aba4dbd71" />


Filesystem sanity (2):
1.mkdir /tmp/rundemo-book -  made a directory named rundemo-book.<br></br>
2.cp /etc/hosts /tmp/rundemo-book/hosts-copy && ls -l /tmp/rundemo-book  -  

<img width="1325" height="195" alt="image" src="https://github.com/user-attachments/assets/b7a5427e-8fc8-417d-895e-e0cf340ea4e1" />

CPU / Memory (2):
1.free -h : configures and go through our disk and tell how much space is vacant and how much is occupied.<br></br>
2.ps -o pid : It displays only the process IDs (PIDs) of all running processes.

<img width="737" height="334" alt="image" src="https://github.com/user-attachments/assets/4f246f45-c82c-416d-b389-a2be6d784935" />

Disk / IO (2):
1. df -h: list downs the file name, tells us about the size of that particular application how much is used and where it is currentlt mounted. <br></br>
2. vmstat : Displays a real-time summary of system performance, including CPU usage, memory, processes, and I/O activity.

<img width="798" height="528" alt="image" src="https://github.com/user-attachments/assets/2cb9d556-282b-4a3d-9ed1-57b6b0589e06" />

Network (2):
1. ss -tulpn : after running this command it showed me all listening TCP/UDP sockets along with the associated processes and port numbers.
2.ping - this command is used to ping a particular website. for ex in my case i used google.com

<img width="1814" height="366" alt="image" src="https://github.com/user-attachments/assets/36be1be9-87a4-4491-b9c8-d2732892ebc6" />

Logs (2):
1. journalctl -u <service> -n 50t
2. ail -n 50 /var/log/<file>.log

ssh:
<img width="686" height="260" alt="image" src="https://github.com/user-attachments/assets/9cccc620-4a25-420a-aab4-27a922551dc8" />
