# S3-file-upload-trigger
# 🛠️ AWS S3-Lambda-CloudWatch-SNS Email Notification Workflow

## 📌 Project Overview

This project implements a **serverless AWS workflow** that sends an **email notification** when a file is uploaded to an **S3 bucket**. The architecture is event-driven, using **Lambda**, **CloudWatch Logs & Metrics**, and **SNS (Simple Notification Service)** to deliver real-time alerts to your email.

---

## 🚀 Architecture Flow

[S3 Bucket]
↓
[Lambda Function: File Handler]
↓
[CloudWatch Logs]
↓
[Log Metric Filter]
↓
[CloudWatch Alarm]
↓
[SNS Topic]
↓
[Email Notification]


## 🎯 Why This Architecture?

- 🔔 **Real-Time Alerts**: Get notified instantly when critical events (e.g., file upload, errors) occur.
- ☁️ **Serverless**: Scalable, low-cost, and easy to maintain.
- 🧠 **Learning Opportunity**: Understand how multiple AWS services interact together in an event-driven way.

---

## 📦 Services Used

| AWS Service | Purpose |
|-------------|---------|
| **Amazon S3** | Store uploaded files |
| **AWS Lambda** | Process uploaded files and log outcomes |
| **CloudWatch Logs** | Store Lambda logs |
| **Metric Filters** | Identify specific log patterns (e.g., "Upload Complete") |
| **CloudWatch Alarms** | Trigger on matched patterns |
| **SNS** | Send email alerts |
| **IAM** | Manage access between services |


🧩 Learning Value
Concept	Gained Knowledge
Event-driven workflows	Understand AWS’s serverless model
Log analytics	Use CloudWatch log filters for automation
Alerting systems	Implement scalable alert solutions
IAM Policies	Learn how services communicate securely
Modular architecture	Replace or extend components easily

🔄 Alternative Approaches
Use Case	Alternative
Email alert without logs	Trigger SNS directly from Lambda
Realtime dashboards	Use Amazon EventBridge + Lambda + DynamoDB
Complex monitoring	AWS CloudTrail + SecurityHub
Business logic + logs	Use Step Functions instead of Lambda only
Low-code approach	Use AWS Amplify and Amazon AppFlow

🧪 Sample Output
If a file customer-data.csv is uploaded:

CloudWatch Log: Upload Complete: customer-data.csv uploaded to my-upload-bucket

Email: 📩 “Upload Complete Detected for customer-data.csv in my-upload-bucket”
