# 📡 Day 11 — Linux Networking Deep Dive & Apache Troubleshooting

> Hands-on networking analysis and real-world service troubleshooting simulation.

---

# 🧠 Step 1 — Inspect Network Interface

### Check Interface Details

```bash
ip addr
```

![Interface Details](images/day11-step1-interface-details.png)

---

### Verify Assigned IP Address

![IP Address](images/day11-step1-ip-address.png)

---

# 🌐 Step 2 — Routing & DNS Configuration

### Check Default Gateway

```bash
ip route
```

![Default Gateway](images/day11-step2-default-gateway.png)

---

### View Routing Table

```bash
route -n
```

![Route Table](images/day11-step2-route-n.png)

---

### Verify DNS Configuration

```bash
cat /etc/resolv.conf
```

![DNS Config](images/day11-step2-dns-config.png)

---

### Check DNS Status

![DNS Status](images/day11-step2-dns-status.png)

---

# 🌍 Step 3 — Connectivity Testing

### Ping External IP

```bash
ping 8.8.8.8
```

![Ping IP](images/day11-step3-ping-ip.png)

---

### Ping Domain Name

```bash
ping google.com
```

![Ping Domain](images/day11-step3-ping-domain.png)

---

# 🔍 Step 4 — Inspect Open Ports

### Using ss

```bash
ss -tuln
```

![SS Open Ports](images/day11-step4-ss-open-ports.png)

---

### Using netstat

```bash
netstat -tuln
```

![Netstat Open Ports](images/day11-step4-netstat-open-ports.png)

---

### Using lsof

```bash
lsof -i
```

![LSOF Listening Ports](images/day11-step4-lsof-listening-ports.png)

---

# 🛰 Step 5 — Port Scanning with Netcat

### Netcat Installed

![NC Installed](images/day11-step5-nc-installed.png)

---

### Scan Localhost SSH Port

```bash
nc -zv localhost 22
```

![NC Localhost 22](images/day11-step5-nc-localhost-22.png)

---

### Scan Google Port 80

```bash
nc -zv google.com 80
```

![NC Google 80](images/day11-step5-nc-google-80.png)

---

### Local Listener Test

![NC Listener](images/day11-step5-nc-listner.png)

---

### Port Range Scan

![NC Port Scan](images/day11-step5-nc-port-scan.png)

---

# 🚨 Step 6 — Real DevOps Troubleshooting Simulation

---

## 🔴 Stop Apache

```bash
sudo systemctl stop apache2
```

![Apache Stopped](images/day11-step6-apache-stopped.png)

---

## 🔴 Port 80 Not Listening

```bash
ss -tuln | grep :80
```

![Port 80 Not Listening](images/day11-step6-port80-not-listening.png)

---

## 🔴 Curl Fails

```bash
curl -I localhost
```

![Curl Failed](images/day11-step6-curl-failed.png)

---

## 🟢 Start Apache

```bash
sudo systemctl start apache2
```

![Start Apache](images/day11-step6-start-apache.png)

---

## 🟢 Apache Running

![Apache Running](images/day11-step6-apache-running.png)

---

## 🟢 Port 80 Listening

![Port 80 Listening](images/day11-step6-port80-listening.png)

---

## 🟢 HTTP 200 OK

```bash
curl -I localhost
```

![HTTP 200](images/day11-step6-http-200.png)

---

## 🟢 Page Verified

![Updated Page Verified](images/day11-updated-page-verified.png)

---

## 🔥 Skills Practiced

- Network Interface Inspection
- Routing Table Analysis
- DNS Configuration
- Connectivity Testing
- Port Monitoring
- Service Binding to Ports
- Netcat Scanning
- Apache Service Control
- HTTP Verification with curl
- End-to-End Troubleshooting Workflow

---

# 🛠 Tools Used

- ip
- route
- ping
- ss
- netstat
- lsof
- nc (Netcat)
- systemctl
- curl
- Apache2

---

# 🎯 Final Outcome

Simulated real production issue:

Service Down → Port Closed → HTTP Failed  
Service Restarted → Port Listening → HTTP 200 OK  

Complete troubleshooting lifecycle successfully executed.

---

# 🏁 Conclusion

This lab reflects practical DevOps troubleshooting:

✔ Root cause detection  
✔ Service management  
✔ Port verification  
✔ HTTP validation  
✔ Recovery confirmation  

Networking fundamentals + Service debugging completed.
