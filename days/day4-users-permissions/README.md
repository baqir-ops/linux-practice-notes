

# Day 4 – Linux Users & Permissions (Real-World Practice)

## 🎯 Objective
Learn how Linux controls access using users, ownership, and permissions in a real DevOps-style scenario.

---

## 🧑 Users Involved
- **baqir** → System admin / owner
- **appuser** → Application runtime user (non-root)

---

## 📁 Project Structure
```
day4-practice/
├── app.log
├── deploy.sh
├── secret.env
└── backups/
```

---

## 🔐 Permissions Setup

| File / Directory | Permissions | Purpose |
|------------------|------------|---------|
| `deploy.sh` | `755` | Executable deployment script |
| `secret.env` | `600` | Protect secrets (private) |
| `backups/` | `700` | Restrict directory access |
| `app.log` | `644` | Readable application logs |

---

## 🧪 Testing as appuser

Switch to app user:
```bash
su - appuser
```

Move to project directory:
```bash
cd /home/baqir/day4-practice
```

### ✅ Allowed
```bash
./deploy.sh
```

### ❌ Blocked (Security enforced)
```bash
cat secret.env
ls backups
```

Result:
```
Permission denied
```

---

## 🧠 Key Learnings

- Scripts need execute (`x`) permission to run
- Secrets must never be world-readable
- Directories require execute (`x`) permission to enter
- Applications should never run as root
- Ownership (`chown`) is critical for access control

---

## 🌍 Real-World DevOps Relevance
This mirrors real production systems where:
- Apps run as non-root users
- Secrets are protected
- Least privilege principle is enforced

---

## ✅ Status
Day 4 completed successfully.
