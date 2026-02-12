# Day 14 - Auto Scaling with Nginx on AWS

**Objective:**  
Setup a fully functional Auto Scaling Group (ASG) with EC2 instances running Nginx, integrated with an Application Load Balancer (ALB) and Target Group, demonstrating scalable web infrastructure.

---

## ✅ What was done today:

1. **Launch Template**
   - Created `day14-launch-template` using Ubuntu 22.04 AMI.
   - Added User Data script to automatically install and start Nginx.

2. **Security Groups**
   - Configured EC2 SG with HTTP (80) and SSH (22) access.
   - Configured ALB SG for secure traffic routing.

3. **Target Group & Load Balancer**
   - Created Target Group `day14-tg` for HTTP traffic.
   - Created ALB `day14-alb` attached to the Target Group.

4. **Auto Scaling Group**
   - Created `day14-asg` with:
     - Desired capacity: 2
     - Min: 1, Max: 3
     - Attached to Target Group
   - Verified instances launch and register automatically.

5. **Health Verification**
   - Target Group showing **Healthy** instances.
   - Nginx page served:  
     ```
     Auto Scaling Server Working
     ```

---

## 📸 Screenshots

Check `screenshots/` folder for visual proof of setup:
- Launch Template version with User Data
- Security Group configuration
- ASG details
- Target Group & LB registration
- Browser output showing Nginx

---

**Outcome:**  
✅ Fully automated, scalable web server deployment using AWS EC2, ALB, and ASG.  
✅ Instances automatically register and deregister from Target Group.  
✅ Nginx is installed via user data — no manual intervention required.

--
