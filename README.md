# AWS-Secure-High-Availability-Architecture-with-Observability
This project demonstrates a production-style AWS cloud architecture focused on security,
high availability, and operational observability.

The goal was to design and implement a realistic system that mirrors how modern cloud
environments are architected, secured, and operated in real-world organizations.

list of the core application platforms/services your project touched
Networking & Traffic Management

Amazon VPC

Public & Private Subnets (Multi-AZ)

Internet Gateway

Security Groups

Application Load Balancer (ALB)

Compute & Scaling

Amazon EC2

EC2 Launch Templates

Auto Scaling Groups (ASG)

EC2 Instance Refresh

Security & Identity

AWS IAM (Roles & Policies)

AWS Secrets Manager

Security Group–based segmentation

Observability & Monitoring

Amazon CloudWatch Metrics

CloudWatch Dashboards

ALB Metrics (RequestCount, RequestCountPerTarget, TargetResponseTime)

Per-AZ Metric Analysis

Application Integration

ALB Target Groups

Health Checks

Listener Rules

Operations & Lifecycle

Rolling updates via ASG Instance Refresh

Resource teardown & cost control

Operational validation via metrics
