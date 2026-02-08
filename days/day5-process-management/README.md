
# Day 5 – Linux Process Management (Hands-On)
### 🔹 Process Listing
![ps aux](images/day5-ps-aux.png)
![ps grep](images/day5-ps-grep.png)

### 🔹 Real-time Monitoring
![top](images/day5-top.png)
![htop](images/day5-htop.png)

### 🔹 Background Jobs
![background job](images/day5-background-job.png)

### 🔹 Killing Processes
![kill process](images/day5-kill-process.png)
This day focused on **Linux process management**, which is a core skill for
Cloud Engineers, DevOps Engineers, and System Administrators.

The goal was to understand how Linux handles running programs, background jobs,
and long-running processes in real-world production scenarios.

---

## 🔹 Topics Covered

### 1️⃣ Foreground vs Background Processes
- Foreground processes block the terminal
- Background processes allow the terminal to remain usable

Commands practiced:
sleep 100
sleep 100 &
###2️⃣ Job Control
Learned how to manage jobs inside the shell.
Commands:
jobs
Ctrl + Z
bg
fg
Explanation:
Ctrl + Z pauses a running process
bg resumes it in background
fg brings it back to foreground
###3️⃣ Process Monitoring
Checked running processes and filtered output.
Commands:
ps aux
ps aux | grep sleep
ps aux | grep [s]leep
###4️⃣ Killing Processes (Signals)
Learned how Linux signals work.
Commands:
kill PID
kill -15 PID # Graceful stop
kill -9 PID # Force kill
Signal meaning:
-15 (SIGTERM) → polite shutdown
-9 (SIGKILL) → immediate termination
###5️⃣ nohup (Run After Logout)
Used for long-running jobs that must survive terminal close or logout.
Command:
nohup sleep 300 &
Behavior:
Ignores terminal input
Writes output to nohup.out
Process continues after logout
###6️⃣ disown (Detach from Shell)
Removed jobs from shell job table.
Command:
disown
Effect:
Shell will not track the process
Process survives shell exit
###7️⃣ htop (Interactive Process Viewer)
Used htop for real-time monitoring.
Features used:
CPU & memory usage
Process tree
Kill processes interactively
Command:
htop
🔑 Key Learnings
Not all processes should run in foreground
Long-running services must survive logout
Proper signal usage prevents system instability
Process management is critical for production troubleshooting
🎯 Real-World Relevance
These skills are used daily in:
DevOps environments
Cloud server management
Production incident handling
CI/CD pipelines
Server automation
📌 Status
✅ Day 5 Completed

