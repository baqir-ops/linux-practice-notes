# Day 8 – File Search, Text Processing & System Logs (Linux)

This day focuses on practical Linux skills used daily by DevOps engineers:
- Searching files and directories
- Understanding system logs
- Managing services using `systemctl`
- Working with `journalctl`

---

## Topics Covered
- `find` command (by name, type, size)
- System logs with `journalctl`
- Service status using `systemctl`
- Managing `cron` service

---

## Step 1: Find files by name

**Command:**
```bash
find . -name "*.png"
Explanation:
Searches recursively for files ending with .png
**Screenshots**
![Find files by name](./images/day8-find-by-name.png)
##Step 2: Find files and directories by type
Find only directories

Bash
find . -type d
**Screenshots  (Directories)**
![Find directories](./images/day8-find-by-type-d.png)

Find only files

Bash
find . -type f
**Screenshots (Files)
![Find files](./images/day8-find-by-type-f.png)
##Step 3: Find files by size
Command:

Bash
find . -size +1M
Explanation:
Finds files larger than 1 MB
**Screenshot**
![Find files by size](./images/day8-find-by-size.png)
##Step 4: Viewing system logs using journalctl
View all logs

Bash
journalctl
**Screenshot**
![View all logs](./images/day8-journalctl-all.png)

View logs from today

Bash
journalctl --since today
**Screenshot**
![Journalctl today](./images/day8-journalctl-today.png)

View error logs only

Bash
journalctl -p err
**Screenshot**
![Journalctl errors](./images/day8-journalctl-errors.png)

View last 20 logs of a specific service

Bash
journalctl -u systemd-hostnamed -n 20
**Screenshot**
![Last 20 logs of systemd-hostnamed](./images/day8-journalctl-hostnamed-last20.png
##Step 5: Checking service status using systemctl
Check hostname service status

Bash
systemctl status systemd-hostnamed
**Screenshot**
![systemed-hostnamed service status](./images/day8-systemctl-hostnamed-status.png
##Step 6: Managing cron service
Check cron status

Bash
systemctl status cron
**Screenshot**
![Cron service status](./images/day8-cron-status.png)

Stop cron service

Bash
sudo systemctl stop cron
**Screenshot**
![Cron service stopped](./images/day8-cron-stopped.png)

Start cron service

Bash
sudo systemctl start cron
**Screenshot**
![Cron service started](./images/day8-cron-started.png)
Key Learnings
● find is a powerful tool for file and directory search

● journalctl helps debug system and service issues

● systemctl is essential for managing Linux services

● Understanding logs is critical for DevOps and production troubleshooting 


Day 8 Status
✅ Completed
📁 Screenshots organized
📘 README documented
