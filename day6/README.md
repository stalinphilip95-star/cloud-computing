
EC2 Auto Scaling using CloudWatch, Launch Template and Auto Scaling Group
Project Flow Diagram

CloudWatch Alarm
        ↓
Auto Scaling Policy
        ↓
Auto Scaling Group
        ↓
Launch Template
        ↓
EC2 Instances (Auto Scale)
        ↓
Load + CPU Metrics
        ↓
CloudWatch Dashboard (Graph View)
Step 1: Launch Template Create Pannunga
Path:
EC2 → Launch Templates → Create
Settings:
AMI: Amazon Linux 2
Instance type: t2.micro
Security Group: HTTP + SSH allow
Key Pair: select your key
 Save Launch Template
 Step 2: Auto Scaling Group Create
Path:
EC2 → Auto Scaling Groups → Create
Steps:
Select Launch Template
Choose VPC + Subnets
Attach Load Balancer (optional but recommended)
Capacity:
Desired = 1
Min = 1
Max = 3
 Step 3: Scaling Policy + CloudWatch Alarm
Scale Out (CPU > 70%)
Create CloudWatch Alarm
Metric: CPUUtilization
Condition: > 70% for 5 min
Action: Add 1 instance
Scale In (CPU < 30%)
Condition: < 30%
Action: Remove instance
 Step 4: CloudWatch Dashboard Create
Path:
CloudWatch → Dashboards → Create dashboard
Add Widget:
Select: Line graph
Metric:
EC2 → CPUUtilization
Auto Scaling Group metrics
 Save dashboard
 Step 5: EC2 Connect & Load Generate
Connect:
Bash
ssh -i your-key.pem ec2-user@<public-ip>
Install stress tool:
Bash
sudo yum install stress -y
Generate CPU load:
Bash
stress --cpu 2 --timeout 300
 This will increase CPU → trigger scaling
 Step 6: Graph View Check
Go to: CloudWatch Dashboard
# AWS Auto Scaling Project

## Overview
This project demonstrates AWS Auto Scaling using EC2, CloudWatch, Launch Templates, and Auto Scaling Groups.

## Architecture
CloudWatch Alarm → Auto Scaling Policy → Auto Scaling Group → Launch Template → EC2 Instances

## Services Used
- Amazon EC2
- Auto Scaling Group
- Launch Template
- CloudWatch
- Security Groups

## Steps Performed
1. Created Launch Template
2. Created Auto Scaling Group
3. Configured scaling policies
4. Set CloudWatch alarms
5. Created CloudWatch dashboard
6. Generated CPU load using stress tool

## Scaling Conditions
- Scale Out: CPU > 70%
- Scale In: CPU < 30%

## Result
- Instances automatically scale based on CPU load
- CloudWatch dashboard shows real-time metrics

## Commands Used
```bash
sudo yum install stress -y
stress --cpu 2 --timeout 300
