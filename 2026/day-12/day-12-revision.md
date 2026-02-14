##Revision (Days 01–11)
- My goal for 2026 is to become a DevOps Engineer, and I’m confidently progressing in the right direction. With consistent learning, hands-on practice, and a clear focus on mastering Linux, automation, and cloud technologies.
- My Goal is also to learn kubernetes and teraaform

#Processes & services

When my system hangs or slows down, I use the following commands to troubleshoot and check service health:
-ps aux → Lists all running processes on the system.
-top→ Display sorted information about processes.
-systemctl status <service> → Displays the status of a specific service (whether it’s active, failed, or inactive).
-journalctl -u <service>→ Displays logs for a specific service, useful for debugging issues.

I have practiced creating/modifying/permission of Linux file/folder. Here is how to safely change ownership and permissions:
-Check current ownership and permissions
Change permissions (least privilege principle)
-chmod 751 /path/to/file
Change ownership (user and group)
-sudo chown user:group /path/to/file

##Cheat Sheet 

- cat /var/log/nginx/error.log - Reads raw logs for web server errors (replace with relevant service log path).
- systemctl status service - Verifies if a critical service is active, failed, or restarting.
- mpstat - Monitors CPU utilization across cores, highlighting bottlenecks or unusual load.
- ps aux - Lists all running processes with CPU/memory usage
- journalctl -u service - Retrieves detailed logs for a given service, useful for debugging failures.
- free -m - Displays memory usage in MB to check for exhaustion or leaks.

  ##What will you focus on improving in the next 3 days?
  - I want to complete volume management and start learning networking. I want to make my networking fundamentals strong.
  - make a strong fundamentals and command pratice on changing group, owner, files in user and group managments.
  - If i completes this and if i have a spare time i will start Pythons for DevOps Course and revise that.


  <img width="683" height="374" alt="Screenshot 2026-02-15 002610" src="https://github.com/user-attachments/assets/a2c7ab8d-eb70-4123-921e-82bc2cc721e6" />
