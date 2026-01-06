# 🌐 3-Tier Architecture on AWS

This project demonstrates a **highly available, fault-tolerant 3-tier architecture** using:

- **Web Tier (React + Nginx)**
- **Application Tier (Node.js + PM2)**
- **Database Tier (Amazon RDS / Aurora MySQL)**

---

## 🧩 Architecture Diagram

📸 **Screenshot to Add:**  
<img width="1280" height="582" alt="image" src="https://github.com/user-attachments/assets/b388de83-2d4e-451b-a07e-34a42c0cb645" />


---

## 🛠️ AWS Services Used

- VPC  
- EC2  
- Application Load Balancer (ALB)  
- Target Groups  
- IAM  
- S3  
- RDS (MySQL / Aurora)  
- Route 53  
- ACM (SSL)

---


### ✅ Step 1: VPC Creation

Created a custom **VPC with Public & Private Subnets**, Internet Gateway, and NAT Gateway.
<img width="1919" height="1030" alt="Screenshot 2026-01-05 192504" src="https://github.com/user-attachments/assets/83bf8d12-f484-4d29-8844-7aa6c46a57f7" />
<img width="1919" height="1027" alt="Screenshot 2026-01-05 192530" src="https://github.com/user-attachments/assets/302d5182-25d9-45a9-93d5-5714a0c8b88e" />
<img width="1919" height="566" alt="route" src="https://github.com/user-attachments/assets/c2c03b0f-03b7-46fa-b9c0-e68ee3f408a1" />
<img width="1909" height="984" alt="subnets" src="https://github.com/user-attachments/assets/aa6f648d-fd28-4973-9709-02c36b6892a8" />


### ✅ Step 2: S3 Bucket & IAM Role Setup

- Created S3 bucket to store application code  
- Attached IAM role to EC2 for S3 access  
<img width="1918" height="1024" alt="s3 1" src="https://github.com/user-attachments/assets/1eaec46b-f628-462a-95cc-b56668ae00d0" />
<img width="1637" height="503" alt="s3 2" src="https://github.com/user-attachments/assets/62c4e772-8db0-4590-a58f-816b312fd729" />
<img width="1641" height="490" alt="iam roles" src="https://github.com/user-attachments/assets/6fa36699-854b-4454-875a-42d813034dc0" />


