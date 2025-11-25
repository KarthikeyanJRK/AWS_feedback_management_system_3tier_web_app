# AWS Feedback Management System

A simple 3-tier AWS web application that collects user feedback, analyzes sentiment using Amazon Comprehend, and stores results in a secure RDS MySQL database. The system is designed to be scalable, highly available, and monitored using AWS tools.

## 📌 Overview

The app has:
- **Frontend (Web Tier)** – Users submit feedback through a web form hosted on EC2 behind a Public ALB.
- **Backend (App Tier)** – A Python/Flask API in private subnets, behind an Internal ALB.
- **Database (Data Tier)** – Amazon RDS MySQL storing feedback and sentiment results.

Amazon Comprehend automatically classifies feedback as Positive, Negative, Neutral, or Mixed.

## 🚀 Architecture Components

- **VPC** with public & private subnets  
- **Public ALB** → Web EC2 instances  
- **Internal ALB** → App EC2 instances  
- **RDS MySQL** in private DB subnets  
- **NAT Gateways** for secure outbound traffic  
- **IAM Role** for Comprehend access  
- **Auto Scaling Groups** for both Web & App tiers  
- **CloudWatch Logs & Alarms**  
- **SNS Notifications** for scaling events  
- **QuickSight Dashboard** for visualization  

## 📈 How It Works

1. User submits feedback on the web form.  
2. Backend receives the request via Internal ALB.  
3. Amazon Comprehend analyzes sentiment.  
4. Feedback + sentiment is stored in RDS.  
5. QuickSight connects to RDS to visualize insights.

## 🛠 Technologies Used

- **EC2**, **ALB**, **RDS MySQL**, **VPC**, **NAT**, **Security Groups**  
- **Amazon Comprehend** (sentiment analysis)  
- **Amazon QuickSight** (dashboards)  
- **CloudWatch & SNS** (monitoring/alerts)  
- **IAM Roles**  

## 📂 Project Purpose

This project demonstrates:
- Building a secure 3-tier architecture on AWS  
- Integrating machine learning (Comprehend) into applications  
- Using QuickSight for analytics  
- Implementing Auto Scaling and monitoring best practices  

## 👤 Author

**Karthikeyan Jeyabalasuntharam**

---

If you want, I can also generate a **super-short version**, a **GitHub-ready version**, or a **portfolio-friendly description**.
