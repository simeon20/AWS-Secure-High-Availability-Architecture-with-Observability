# Project Title
AWS Secure High Availability Architecture with Observability

# Overview 
This project demonstrates a production-style AWS architecture focused on security, high availability, and operational observability. The system was designed to mirror how modern cloud environments are built, monitored, and validated in real organizations.

# Architecture Highlights

- Multi-AZ VPC with public and private subnets

- Internet-facing Application Load Balancer

- Auto Scaling EC2 application tier

- Secure IAM role-based access and secrets management

- Real-time observability using CloudWatch metrics and dashboards

# Core AWS Services Used:

### Networking & Traffic Management

- Amazon VPC

- Public & Private Subnets (Multi-AZ)

- Internet Gateway

- Security Groups

- Application Load Balancer (ALB)

### Compute & Scaling

- Amazon EC2

- Launch Templates

- Auto Scaling Groups

- Instance Refresh (rolling updates)

### Security & Identity

- AWS IAM (roles and policies)

- AWS Secrets Manager

- Network segmentation via Security Groups

### Observability & Monitoring

- Amazon CloudWatch Metrics

- CloudWatch Dashboards

ALB metrics:

- RequestCount

- RequestCountPerTarget

- TargetResponseTime

- Per-Availability Zone metric analysis

### Application Integration

- ALB Target Groups

- Health Checks

- Listener Rules

### Operations & Lifecycle

- Rolling deployments using ASG Instance Refresh

- Operational validation via metrics

- Cost control through full environment teardown

---

### Key Outcomes

- Validated high availability using multi-AZ traffic distribution

- Observed real application behavior through ALB and target-level metrics

- Demonstrated safe rolling updates without downtime

- Built a secure, observable, and resilient cloud architecture
