# HTML Website on AWS EC2 with Jenkins Deployment

This repository contains the source code for a simple HTML website hosted on an AWS EC2 instance running Apache.  
The website is deployed automatically whenever changes are pushed to the `main` branch using **GitHub Webhooks** and **Jenkins**.

---

## 🚀 Deployment Workflow

1. Developer pushes changes to `main` branch in GitHub.
2. GitHub sends a webhook to Jenkins.
3. Jenkins pulls the latest code and copies it to Apache's DocumentRoot on EC2.
4. Website updates instantly.

---

## 🛠️ Prerequisites

- AWS EC2 instance (Ubuntu/Debian recommended)
- Apache installed and configured
- Jenkins installed and running on the EC2 instance
- GitHub repository with HTML files
- SSH access between Jenkins and GitHub

---

## 📦 Setup Steps

### 1. Configure Apache on EC2
```bash
sudo apt update
sudo apt install apache2 -y
sudo mkdir -p /var/www/asna
sudo chown -R $USER:$USER /var/www/asna
