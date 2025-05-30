# Static-Website-Hosting-using-S3
This project demonstrates how to host a static website using **Amazon S3**. The project includes an `index.html` file which is deployed and publicly accessible using the S3 Static Website Hosting feature.
## 🚀 Final Deployed Website

🔗 [Click here to view the hosted website](http://blackbucks-s3-project-1.s3-website.eu-north-1.amazonaws.com/)  

---

## 📄 Project Overview

This static website hosting project aims to demonstrate how to:

- Create and configure an S3 bucket for website hosting
- Upload static files (HTML, CSS, JS)
- Set permissions using Bucket Policy and/or ACL
- Deploy and access a public-facing website using AWS

---

## 📁 Project Structure

.
├── index.html
└── README.md

yaml
Copy
Edit

---

## 🧑‍💻 Steps to Run Locally

### 1. Clone this Repository

```bash
git clone https://github.com/Vishwa5395/Static-Website-Hosting-using-S3.git
cd static-website-hosting-s3
```
### 2. Open in Browser
Just open the index.html file directly in your browser:

bash
Copy
Edit
start index.html  # Windows
open index.html   # macOS
xdg-open index.html  # Linux
Or use VS Code:

bash
Copy
Edit
code .
Then open index.html and use Live Server extension to preview.

🪜 How to Deploy on AWS S3
Create an S3 Bucket

Go to AWS S3 console

Create a new bucket (disable "Block all public access")

Upload Files

Upload index.html file into your bucket

Enable Static Website Hosting

Go to Properties → Static website hosting

Enable it and specify index.html as the index document

Set Bucket Policy (for public access)

json
Copy
Edit
```bash
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}
```
Access Your Site

Use the S3 Static Website Endpoint provided in the properties

📌 Notes
You can update the index.html file later and re-upload it to reflect changes on the same URL.

Make sure to set correct permissions for public access.

If you face errors like “Policy has invalid resource”, double-check your bucket name and policy syntax.

📧 Contact
For queries or suggestions, feel free to contact Me.

