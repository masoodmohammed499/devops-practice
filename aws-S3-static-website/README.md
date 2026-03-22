AWS S3 Static Website Hosting

Overview
This project demonstrates how to host a static website using Amazon S3. It showcases how S3 can be used as a cost-effective and scalable solution for hosting static web content such as HTML, CSS, and JavaScript files.

Objective
To configure an S3 bucket for static website hosting and make the website publicly accessible over the internet.

Services Used
Amazon S3

Key Features Implemented

- Created an S3 bucket with globally unique naming
- Disabled block public access to allow website hosting
- Uploaded static website files (index.html)
- Enabled static website hosting
- Configured bucket policy to allow public read access
- Accessed website using S3 endpoint URL

Architecture / Workflow

User (Browser)
↓
S3 Static Website Endpoint
↓
S3 Bucket (index.html hosted)

Implementation Steps

1. Created an S3 bucket with public access enabled
2. Uploaded index.html file to the bucket
3. Enabled static website hosting in bucket properties
4. Configured index document as index.html
5. Added bucket policy to allow public read access
6. Accessed the website using the S3 endpoint URL

Key Observations

- S3 can host static websites without needing a server
- Public access must be explicitly enabled
- Bucket policies are required to allow access to objects
- Website is accessible via S3 endpoint URL

Use Cases

- Personal portfolio websites
- Landing pages
- Static web applications
- Documentation sites

Conclusion

Amazon S3 provides a simple, scalable, and cost-effective way to host static websites. This project demonstrates how cloud storage can be used not just for data storage but also for delivering web content efficiently.
