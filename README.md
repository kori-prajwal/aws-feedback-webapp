# AWS Feedback WebApp

A simple, serverless feedback web application built with HTML, JavaScript, AWS Lambda, API Gateway, and DynamoDB.  
The frontend is hosted on Amazon S3 as a static website.

## 🌐 Live Demo
👉 [Hosted S3 Website URL Here](https://your-s3-site.amazonaws.com/index.html)  
*(Replace with your actual URL once hosted)*

---

## 🛠️ Tech Stack

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: AWS Lambda (Node.js)
- **API**: AWS API Gateway
- **Database**: AWS DynamoDB
- **Hosting**: Amazon S3 (Static Website Hosting)

---

## 📸 Features

- User submits their Name, Email, and Feedback
- Data is sent to an AWS Lambda function via API Gateway
- Lambda writes data into DynamoDB
- Success message shown to the user
- Fully serverless & cost-effective architecture

---

## 🚀 Architecture Diagram

```txt
+-------------+       POST        +-------------+       Write       +-------------+
|   Frontend  | --------------->  |  API Gateway| --------------->  |  Lambda     |
|  (S3 HTML)  |                  |  (REST API) |                  |  Function   |
+-------------+                  +-------------+                  +-------------+
                                                                          |
                                                                          v
                                                                 +----------------+
                                                                 |  DynamoDB      |
                                                                 |  (NoSQL DB)    |
                                                                 +----------------+
