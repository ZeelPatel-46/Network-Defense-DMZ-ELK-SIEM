
# Network Defense Implementation: DMZ Apache Web Server with ELK SIEM

## 📌 Project Overview
This project demonstrates a **layered network defense architecture** using:
- An **Apache Web Server deployed in a DMZ**
- A **centralized SIEM solution using the ELK Stack**
- **Filebeat** for real-time log forwarding
- **Docker-based network segmentation**

The objective is to isolate public-facing services while enabling **real-time attack detection and visibility** through centralized logging.

---

## 🧠 Key Security Concepts Demonstrated
- DMZ network segmentation
- Defense-in-depth
- Centralized logging (SIEM)
- Log correlation and attack detection
- Docker-based network simulation

---

## 🧱 Network Architecture

| Component | IP Address | Role |
|---------|------------|------|
| DMZ Web Server | 10.9.0.5 | Apache HTTP Server |
| Router | 10.9.0.11 | Inter-network routing |
| Internal Network | 192.168.60.0/24 | Protected LAN |
| ELK Stack | Host VM | SIEM Platform |

📌 The Apache server is **isolated in the DMZ**, preventing lateral movement to the internal network.

---

## 🛠️ Technologies Used
- Apache HTTP Server 2.4
- Docker & Docker Compose
- Elasticsearch 7.17.3
- Logstash 7.17.3
- Kibana 7.17.3
- Filebeat 7.17.3
- Ubuntu (SEED Labs 2.0)

---

## 🚀 Deployment Steps

### 1️⃣ DMZ Apache Web Server Setup
```bash
sudo apt update
sudo apt install apache2 -y
sudo service apache2 start
curl http://localhost
