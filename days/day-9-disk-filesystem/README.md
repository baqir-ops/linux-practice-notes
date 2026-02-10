## 📀 Day 9 – Disk & File System (Linux)

## 🎯 Objective
Understand how Linux manages disks, partitions, filesystems, mounts, and disk usage — essential for DevOps and production servers.

## 📚 Topics Covered
•Block devices and partitions
•Disk usage analysis
•Mounted filesystems
•Persistent mounts (/etc/fstab)
•Finding mount points

## 🔹 Step 1: List block devices

**Command**:

```Bash
lsblk
```
## Explanation:
Displays all block devices, partitions, and mount points.

**Screenshot**

![lsblk](./images/day9-lsblk.png)

## 🔹 Step 2: Check disk space usage

a) Human readable disk usage

**Command**

```Bash
df -h
```
## Explanation:
Shows disk size, used space, available space, and mount points.

**Screenshot**

![df-h](./images/day9-df-h.png)

b) Filesystem type
**Command**

```Bash
df -T
```
## Explanation:
Displays filesystem types (ext4, tmpfs, etc.).

**Screenshot**

![df-T](./images/day9-df-T.png)

## 🔹 Step 3: Check total home directory size

**command**

```Bash
du -sh ~
```
## Explanation:
Shows total disk usage of the home directory.

**Screenshot**

![du-home](./images/day9-du-home.png)

## 🔹 Step 4: Find large directories (sorted)

**Command**

```Bash
du -h --max-depth=1 ~ | sort -h
```
## Explanation:
Helps identify large directories consuming disk space.

**Screenshot**

![du-sort](./images/day9-du-sort-home.png)

## 🔹 Step 5: Check subdirectory sizes

**Command**

```Bash
du -sh *
```
## Explanation:
Displays size of each directory in the current folder.

**Screenshot**

![du-subdirs](./images/day9-du-subdirs.png)

## 🔹 Step 6: Find mount points

**Command**

```Bash
findmnt
```
## Explanation:
Shows mounted filesystems and hierarchy.

**Screenshot**

![findmnt](./images/day9-findmnt.png)

## 🔹 Step 7: Persistent mounts configuration

**Command**

```Bash
cat /etc/fstab
```
## Explanation:
Lists filesystems mounted automatically at boot.

**Screenshot**

![fstab](./images/day9-fstab.png)

## 🧠 Key Learnings

•lsblk → disk & partition layout
•df → filesystem usage
•du → directory usage
•findmnt → mount hierarchy
•/etc/fstab → permanent mounts

## ✅ Day 9 Status

✔ Commands practiced
✔ Screenshots captured
✔ README documented
✔ Git-ready structure
