## User & Group Management: Learn about Linux users, groups, and permissions (/etc/passwd, /etc/group).

-  Create a user devops_user and add them to a group devops_team.
-  Set a password and grant sudo access.
  
   ```bash
   sudo useradd -m devops_user
   ```

   ```bash
   sudo groupadd devops_team
   ```

   ```bash
   sudo usermod -aG devops_team devops_user
   ```

   ```bash
   sudo passwd devops_user
   ```

   ```bash
   sudo usermod -aG sudo devops_user
   ```

- Restrict SSH login for certain users in /etc/ssh/sshd_config.
 
   ```bash
   sudo nano /etc/ssh/sshd_config       # add AllowUsers devops_user
   ```

   ```bash
   sudo systemctl restart sshd
   ```
