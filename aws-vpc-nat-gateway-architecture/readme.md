AWS VPC NAT Gateway Architecture

Project Description
This project demonstrates how to create a secure network architecture in AWS using VPC, public subnet, private subnet, Internet Gateway and NAT Gateway. The purpose of this lab is to allow instances in the private subnet to access the internet securely without exposing them directly to the public internet.

Services Used
Amazon VPC
Amazon EC2
Internet Gateway
NAT Gateway
Route Tables
Elastic IP

Architecture
Internet
↓
Internet Gateway
↓
Public Subnet
↓
NAT Gateway
↓
Private Subnet
↓
EC2 Instance

Steps Performed

1. Created a VPC with CIDR block 10.0.0.0/16
2. Created two subnets
   - Public Subnet (10.0.1.0/24)
   - Private Subnet (10.0.2.0/24)
3. Created and attached an Internet Gateway to the VPC
4. Created a public route table and added route 0.0.0.0/0 to Internet Gateway
5. Associated the public subnet with the public route table
6. Allocated an Elastic IP for NAT Gateway
7. Created a NAT Gateway inside the public subnet
8. Created a private route table and added route 0.0.0.0/0 to NAT Gateway
9. Associated the private subnet with the private route table

Result
Private subnet instances can access the internet through NAT Gateway while remaining secure and not directly accessible from the internet.

Screenshots
All screenshots of the configuration and resources created in AWS are attached in the screenshots folder.
