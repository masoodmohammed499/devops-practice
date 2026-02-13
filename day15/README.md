# 🚀 Day 15 - AWS S3 Static Website Hosting

## 📌 Objective
Deploy a static website using Amazon S3 without EC2, demonstrating serverless web hosting using AWS cloud services.

---

## 🛠 Services Used
- Amazon S3
- Bucket Policy (IAM-based access control)
- Static Website Hosting

---

## 🔥 What Was Implemented

### 1️⃣ Created S3 Bucket
- Bucket Name: `day15-masood-static-site`
- Region: Same as previous labs
- Disabled "Block all public access" for website hosting

---

### 2️⃣ Enabled Static Website Hosting
- Hosting Type: Static Website
- Index Document: `index.html`
- Error Document: `error.html`
- Generated S3 Website Endpoint

---

### 3️⃣ Created Website Files

**index.html**

Added bucket policy for public access

{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::day15-masood-static-site/*"
    }
  ]
}

```html
<h1>🔥 Day 15 Static Website Hosting Working 🔥</h1>
<p>Hosted on Amazon S3</p>
