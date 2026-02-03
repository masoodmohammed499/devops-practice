# Day 11 – EC2 + Nginx + S3 Static Website Deployment

## Objective
Deploy a static website on an EC2 instance using Nginx and fetch website files securely from Amazon S3 using an IAM Role.

## Architecture
- EC2 (Ubuntu)
- IAM Role (S3 Read-Only access)
- S3 Bucket (stores website files)
- Nginx Web Server

## Steps Performed
1. Created an S3 bucket and uploaded website files.
2. Created an IAM policy with least-privilege S3 access.
3. Attached IAM role to EC2 instance.
4. Installed and configured Nginx on EC2.
5. Pulled website files from S3 using AWS CLI.
6. Deployed website and verified via browser.

## Security
- No AWS access keys stored on EC2.
- IAM role used for secure S3 access.

## Output
Static website successfully accessible via EC2 public IP.
