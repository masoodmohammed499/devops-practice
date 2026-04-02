AWS RDS MySQL Database Lab 🚀
📌 Overview
In this project, I created and configured an Amazon RDS MySQL database and enabled external connectivity using security groups.

🛠️ Services Used
Amazon RDS
Amazon EC2 (Security Groups)
⚙️ Steps Performed
Created an RDS database using MySQL engine
Selected Free Tier configuration
Configured database credentials
Enabled public access for connectivity
Modified security group to allow MySQL port (3306)
Retrieved database endpoint
🔐 Security Configuration
Opened port 3306 in security group
Allowed inbound traffic from:
0.0.0.0/0 (for lab purposes only)
🌐 Connectivity
Endpoint used to connect to database
Port: 3306
📸 Screenshots
Database Created
DB

Endpoint & Connectivity
Endpoint

Security Group Rule
SG

⚠️ Important Notes
Public access enabled only for testing
In production, restrict access using specific IPs
Database deleted after lab to avoid charges
💡 Key Learnings
How to create RDS MySQL database
How to configure security groups
How database connectivity works in AWS
Difference between private and public access
🚀 Conclusion
Successfully created and configured a publicly accessible RDS database and understood real-world connectivity and security concepts.
