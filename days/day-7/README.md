# Day 7 – Linux Users, Groups & Permissions (Very Important)
## 📸 Screenshots – Day 7 Practice
> Proof of hands-on practice covering users, groups, permissions, SGID, sticky bit, and shared DevOps directories.
### User & Identity
![whoami](images/day-7-whoami.png)
![user-id](images/day-7-user-id.png)

### Group Management
![group-created](images/day7-group-created.png)
![groups-output](images/day-7-groups-outputs.png)
![user-added-group](images/day-7-user-added-to-devops-group.png)
![user-added-team](images/day-7-user-added-to-devops-team.png)

### File Permissions
![initial-permissions](images/day-7-initial-file-permissions.png)
![numeric-permissions](images/day-7-numeric-permissions-640.png)
![script-executable](images/day-7-made-script-executable.png)

### Ownership & Shared Directory
![ownership-changed](images/day-7-ownership-changed-root-devops.png)
![sgid-directory](images/day-7-sgid-directory.png)
![sgid-inheritance](images/day-7-sgid-file-inheritance.png)
![shared-dir](images/day7-devops-shared-dir-sgid.png)

### Special Permissions
![suid](images/day-7-suid-permissions.png)
![sticky-bit](images/day-7-sticky-bit-directory.png)
![numeric-special](images/numeric-special-permissions.png)

### System Context
![systemd](images/day-7-systemd-running-services.png)


## 🎯 Objective
Understand how Linux manages **users**, **groups**, and **permissions**, and practice real-world scenarios like **team-based access**, **SGID**, and **shared directories** used in DevOps environments.

---

## 🔹 Step 1: Identify Current User & Groups
Commands practiced:

whoami
id
groups
✔ Learned about:
UID (User ID)
GID (Group ID)
Primary vs Secondary groups

##🔹 Step 2: Create a New Group
Created a DevOps team group:

sudo groupadd devops-team
getent group devops-team
✔ Verified group creation successfully.
##🔹 Step 3: Add User to Group
Added current user to the DevOps team:

sudo usermod -aG devops-team baqir
newgrp devops-team
groups
✔ User is now part of devops-team.
##🔹 Step 4: SGID on Files & Directories
SGID on file:
chmod u+s suid-test.sh
ls -l suid-test.sh
SGID on directory:

mkdir shared-dir
chmod g+s shared-dir
ls -ld shared-dir
✔ Understood how SGID works on files vs directories.
##🔹 Step 5: Real-World Shared DevOps Directory
Created a shared DevOps directory:

sudo mkdir -p /srv/devops
sudo chown :devops-team /srv/devops
sudo chmod 2775 /srv/devops
ls -ld /srv/devops
✔ SGID ensures all files inherit the devops-team group.
##🔹 Step 6: Verify Group Inheritance

cd /srv/devops
touch test.txt
ls -l test.txt
✔ File automatically inherited group:

devops-team
🧠 Key Learnings
Linux permissions = security foundation
SGID is critical for team collaboration
/srv is commonly used for shared service data
Group ownership prevents permission conflicts

🌍 Real-World Use Case
Used in DevOps teams where:
Multiple engineers deploy files
CI/CD pipelines need shared access
Production directories must stay secure
✅ Day 7 Status
✔ Users
✔ Groups
✔ Permissions
✔ SGID
✔ Shared DevOps Directory
Day 7 completed successfully- hands-on verify 🚀
