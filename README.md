# Amazon RDS Monitoring and Alerting System

This project monitors an Amazon RDS MySQL instance using AWS CloudWatch and triggers alerts via Amazon SNS when performance metrics such as CPU utilization exceed a defined threshold. The system helps ensure high availability, early incident response, and performance visibility for managed database services.

<img width="1019" alt="Screenshot 2025-04-23 at 9 13 23 PM" src="https://github.com/user-attachments/assets/83112ecc-48d0-4f14-8715-8ca04877558d" />


## 🛠️ Technologies & Services Used

- **Amazon RDS** (MySQL)
- **Amazon CloudWatch**
- **Amazon SNS (Simple Notification Service)**
- **IAM Roles & Policies**
- **EC2 (for RDS access and metric simulation)**

---

## 📌 Features

- Monitors **CPU Utilization**, **Database Connections**, and **Storage**.
- Sends **email alerts** when thresholds are breached.
- Supports **Enhanced Monitoring** for detailed system metrics.
- Includes optional **custom CloudWatch dashboard** for visual tracking.

## 🚀 How It Works

1. **Create an RDS MySQL Instance** (Free Tier eligible)
2. **Enable Enhanced Monitoring**
   - Set granularity (1s or 5s)
   - Attach IAM role: `rds-monitoring-role`
3. **Create CloudWatch Alarms**
   - Trigger on `CPUUtilization > 80%`
   - Notify via SNS Topic (email subscription)
4. **Simulate High CPU**
   - Use `BENCHMARK()` in MySQL to test alerting system
5. **(Optional) Build Custom Dashboard**
   - Visualize CPU, connections, and free storage

