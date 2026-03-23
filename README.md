#  Wazuh SIEM Lab (UTM + Ubuntu + Docker)

##  Project Overview

This project demonstrates the deployment of a Wazuh SIEM environment using Docker containers on an Ubuntu Server virtual machine running in UTM on macOS.

The lab simulates a real-world Security Operations Center (SOC) setup for monitoring and analyzing system activity.

---

##  Objectives

* Deploy Wazuh SIEM using Docker
* Understand SIEM architecture and components
* Monitor logs and security events
* Gain hands-on experience with security monitoring

---

##  Tools & Technologies

* Wazuh SIEM (Dockerized)
* Docker & Docker Compose
* Ubuntu Server (UTM VM)
* macOS (Host)

---

##  Architecture

macOS (Host Machine)
│
└── UTM Virtual Machine
└── Ubuntu Server
└── Docker Containers
├── Wazuh Manager
├── Wazuh Indexer
└── Wazuh Dashboard

---

##  Installation Process

### 1. System Update

```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Install Docker

```bash
sudo apt install docker.io docker-compose -y
sudo systemctl enable docker
sudo systemctl start docker
```

### 3. Deploy Wazuh (Docker)

```bash
git clone https://github.com/wazuh/wazuh-docker.git
cd wazuh-docker
docker-compose up -d
```

### 4. Verify Containers

```bash
docker ps
```

### 5. Access Dashboard

Open in browser:

```
https://<your-server-ip>
```

---

##  Screenshots

Screenshots demonstrating the setup and functionality will be stored in the `/screenshots` folder.

---

##  Key Learnings

* SIEM deployment in a virtualized environment
* Containerized infrastructure using Docker
* Log collection and analysis
* Security monitoring fundamentals

---

##  Future Improvements

* Add endpoint agents (Kali Linux)
* Simulate attacks for detection testing
* Create custom detection rules
* Automate alerts and notifications
