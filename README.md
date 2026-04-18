# 🚀 DevOps Project 1 — Static Website Deployment on AWS EC2

## 📌 Project Overview

This project demonstrates how to deploy a static website on an AWS EC2 instance using Nginx.

It covers core DevOps concepts such as:

* Cloud provisioning (AWS EC2)
* Linux server management
* Web server setup (Nginx)
* Remote access via SSH

---

## 🏗️ Architecture

User → Browser → EC2 Instance → Nginx → Static Website

---

## ⚙️ Technologies Used

* AWS EC2
* Ubuntu Linux
* Nginx
* SSH

---

## 🪜 Step-by-Step Implementation

### 1️⃣ Launch EC2 Instance

* Created Ubuntu EC2 instance (t2.micro)
* Configured Security Group:

  * Port 22 (SSH)
  * Port 80 (HTTP)

---

### 2️⃣ Connect to EC2 via SSH

```bash
ssh -i your-key.pem ubuntu@your-public-ip
```

---

### 3️⃣ Install Nginx

```bash
sudo apt update
sudo apt install nginx -y
```

---

### 4️⃣ Start Nginx

```bash
sudo systemctl start nginx
```

---

### 5️⃣ Deploy Website

```bash
cd /var/www/html
sudo rm index.nginx-debian.html
sudo nano index.html
```

Added custom HTML page.

---

### 6️⃣ Restart Nginx

```bash
sudo systemctl restart nginx
```

---

## 🌐 Output

Website successfully deployed and accessible via:
http://75.101.223.47

---

## 📸 Screenshots

### 🔹 EC2 Instance

<img width="1899" height="866" alt="Screenshot 2026-04-18 100650" src="https://github.com/user-attachments/assets/36f6625a-b983-4687-bbd6-65d724ed7386" />


### 🔹 SSH Connection

<img width="1567" height="149" alt="Screenshot 2026-04-18 100906" src="https://github.com/user-attachments/assets/8c8b3d2b-9a38-47a8-9eb0-e82a02b0d02a" />

---

<img width="1892" height="482" alt="Screenshot 2026-04-18 101107" src="https://github.com/user-attachments/assets/c67407ac-6eae-410c-ab7b-9a31addfb3fb" />



### 🔹 Website Output

  <img width="1919" height="534" alt="Screenshot 2026-04-18 101127" src="https://github.com/user-attachments/assets/aff882d3-ddc8-4e5c-bbcf-37ebe1c50fcb" />


---

## 🧠 Key Learnings

* How to launch and configure EC2 instances
* How to connect securely using SSH
* Installing and managing Nginx
* Hosting a live website on cloud infrastructure

---

## 💬 Interview Explanation

"I deployed a static website on AWS EC2 by launching an Ubuntu instance, configuring security groups, connecting via SSH, installing Nginx, and serving the website over HTTP."

---

## 🔮 Future Improvements

* Dockerize the application
* Add CI/CD pipeline (GitHub Actions)
* Use Terraform for infrastructure automation
