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



## File & Directory Permissions

- Create /devops_workspace and a file project_notes.txt.

```bash
mkdir devops_workspace
```

```bash
touch project_notes.txt.
```
Set permissions:

```bash
sudo chmod XXX file_name
```
- Owner can edit, group can read, others have no access.
```bash
chmod 640 project_notes.txt.
```

- Use ls -l to verify permissions.
```bash
la -l
```

## Log File Analysis with AWK, Grep & Sed

- Download the log file from the repository.
Extract insights using commands:
Use grep to find all occurrences of the word "error".

 ```bash
 grep -i "failure" Linux_2k.log 
 ```
- Use awk to extract timestamps and log levels.
  
 ```bash
    
 ```

