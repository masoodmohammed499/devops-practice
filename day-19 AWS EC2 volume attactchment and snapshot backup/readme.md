AWS EC2 EBS Volume Attachment and Snapshot Backup

Project Overview

This project demonstrates how to attach an EBS volume to a running EC2 instance, format it, mount it in Linux, and create a snapshot backup.

The goal is to understand how persistent storage works in cloud infrastructure and how DevOps engineers manage server storage.

Technologies Used

- Amazon EC2
- Amazon EBS
- Ubuntu Linux
- AWS Management Console
- Linux CLI

Services Used

- EC2 (Virtual Server)
- EBS (Block Storage)
- EBS Snapshot (Backup)

Architecture

EC2 Instance → Attached EBS Volume → Mounted in Linux → Snapshot Backup

Step 1: Launch EC2 Instance

1. Go to AWS Console
2. Navigate to EC2 Dashboard
3. Launch an Ubuntu Instance
4. Connect using SSH

Step 2: Create EBS Volume

1. Go to EC2 → Elastic Block Store → Volumes
2. Click "Create Volume"
3. Size: 1 GiB
4. Availability Zone: Same as EC2
5. Create volume

Step 3: Attach Volume to EC2

1. Select the volume
2. Click Actions → Attach Volume
3. Select EC2 instance
4. Device name: /dev/sdf

Step 4: Verify Disk in Linux

Run the command:

lsblk

The new disk appears as:

nvme1n1

Step 5: Format the Disk

sudo mkfs -t ext4 /dev/nvme1n1

Step 6: Create Mount Directory

sudo mkdir /data

Step 7: Mount the Volume

sudo mount /dev/nvme1n1 /data

Verify:

df -h

Step 8: Test Storage

cd /data
sudo nano test.txt

Content:

Hello from EBS Volume

Step 9: Create Snapshot Backup

1. Go to EC2 → Snapshots
2. Select the volume
3. Click Create Snapshot
4. Add description and create backup

Screenshots

Screenshots of the following steps are included:

- EC2 instance running
- EBS volume created
- Volume attached to instance
- Disk detected in Linux
- Volume mounted
- File stored in EBS
- Snapshot created

Key Learnings

- How to attach storage to a running EC2 instance
- How Linux detects AWS NVMe volumes
- How to format and mount a disk in Linux
- How to create backups using EBS snapshots

Author

Masood
DevOps Learning Project
