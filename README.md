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
<img width="1919" height="1027" alt="Screenshot 2026-01-05 192530" src="https://github.com/user-attachments/assets/302d5182-25d9-45a9-93d5-5714a0c8b88e" />
<img width="1919" height="1030" alt="Screenshot 2026-01-05 192504" src="https://github.com/user-attachments/assets/83bf8d12-f484-4d29-8844-7aa6c46a57f7" />


