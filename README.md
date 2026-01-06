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
Instance..
<img width="1914" height="1003" alt="instance" src="https://github.com/user-attachments/assets/5eea44bb-368a-4468-94bb-9034296e71e8" />
Security Group..
<img width="1689" height="442" alt="security group" src="https://github.com/user-attachments/assets/7ba9279c-4f60-4aa3-898e-0d11712eb4ac" />

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

### ✅ Step 3: Database Configuration (RDS)

- Launched **Amazon RDS / Aurora MySQL**
- Created database and table
<img width="1919" height="1029" alt="rds" src="https://github.com/user-attachments/assets/53986f51-160d-48d2-bd79-595422474f48" />


### ✅ Step 4: Application Tier Setup

- Installed Node.js & PM2  
- Deployed backend  
- Verified `/health` endpoint  
<img width="1919" height="773" alt="pm 2" src="https://github.com/user-attachments/assets/53e67a8a-37ed-4c50-90d7-ed6d6b2b7b29" />
<img width="1323" height="891" alt="pm 1" src="https://github.com/user-attachments/assets/d6f06d29-bfa8-4d71-971f-7ea6e5fc6542" />
<img width="1919" height="768" alt="other" src="https://github.com/user-attachments/assets/8cdb4361-3435-416e-9165-d7b7a4c94fca" />


### ✅ Step 5: Internal Load Balancer (App Tier)

- Created **Internal Application Load Balancer**  
- Registered App Tier EC2 in Target Group  
<img width="1912" height="1022" alt="target group" src="https://github.com/user-attachments/assets/4b1d205c-5b21-4de2-a069-64f20a3ad063" />
<img width="1919" height="1024" alt="load balance" src="https://github.com/user-attachments/assets/8ed9a0e0-3620-4653-9580-c0b028133630" />


### ✅ Step 6: Application Testing

- Opened Web Tier public IP  
- Inserted data into UI  
- Verified records in RDS  
<img width="1918" height="1033" alt="o 2" src="https://github.com/user-attachments/assets/a3bd4d33-3130-4807-9be3-0611fb6c567f" />
<img width="1919" height="1026" alt="o 1" src="https://github.com/user-attachments/assets/91237853-041a-4aa3-801d-23d847b7d6e6" />
