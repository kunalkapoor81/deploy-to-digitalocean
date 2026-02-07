# 🚀 DigitalOcean Java Application Deployment

## 📌 Project Overview
This project demonstrates how to securely configure a DigitalOcean Droplet and deploy a Java Gradle application following cloud security best practices.

---

## 🛠 Features
- Setup and configure a DigitalOcean server
- Create and configure a secure Linux user
- Deploy and run a Java Gradle application




## ☁️ Infrastructure Setup

### 1️⃣ Create DigitalOcean Droplet
- Provision a Linux-based Droplet (Ubuntu recommended)
- Configure SSH key authentication
- Verify remote access

```bash
ssh root@your_droplet_ip
```

---

### 2️⃣ Create Secure Linux User (Security Best Practice)

Create a new user instead of using root for daily operations.

```bash
adduser appuser
```

Grant sudo privileges:

```bash
usermod -aG sudo appuser
```

Switch to new user:

```bash
su - appuser


### Build Java Application

```bash
gradle build
```

Generated JAR file will be located in:

```
build/libs/
```

---

### Run Application

```bash
java -jar build/libs/application.jar
