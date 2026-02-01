# Day 10 – EC2 + IAM + S3 Website Deployment (Nginx)

## 🔹 Objective
Deploy a basic website on an EC2 instance using Nginx and demonstrate secure access to S3 using an IAM Role.

## 🔹 Services Used
- Amazon EC2
- AWS IAM (Role-based access)
- Amazon S3
- Nginx (Web Server)

## 🔹 What Was Done
- Launched an EC2 instance with a public IP
- Created and attached an IAM role to EC2 for S3 access (no access keys used)
- Created an S3 bucket and uploaded a website asset (`hero.png.png`)
- Installed and started Nginx on the EC2 instance
- Verified the web server using the default Nginx welcome page

## 🔹 Proof of Work
Screenshots included in this folder:
1. EC2 instance running
2. IAM role attached to EC2
3. S3 bucket with uploaded asset
4. Nginx welcome page / website output

## 🔹 Key Learning
- Secure AWS access using IAM roles instead of credentials
- Basic Linux and Nginx setup on EC2
- Understanding how EC2, IAM, and S3 integrate in real-world deployments

---

✅ **Status:** Completed
