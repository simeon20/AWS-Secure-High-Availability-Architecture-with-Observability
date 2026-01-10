
# Architecture Overview

This solution is deployed across multiple AWS Availability Zones and is designed to reflect a production-grade, secure, and highly available cloud architecture.

## Core Components

- **Custom VPC** with public and private subnets
- **Internet-facing Application Load Balancer (ALB)**
- **Auto Scaling Group (ASG)** running application instances in private subnets
- **PostgreSQL RDS** database in private subnets (no public access)
- **AWS Secrets Manager** for secure credential handling
- **IAM roles and SSM Session Manager** (no direct SSH access)
- **CloudWatch dashboards** for traffic, health, and latency visibility

## Traffic Flow

Traffic flows from the internet-facing ALB to application instances over private subnets, ensuring backend services are never directly exposed.

## High Availability Design

- Application instances are distributed across multiple Availability Zones
- The ALB automatically routes traffic only to healthy targets
- Auto Scaling Group supports instance replacement and rolling refreshes without downtime

## Observability

- ALB request counts and latency tracked via CloudWatch
- Per–Availability Zone metrics used to validate HA behavior
- Target health and response time monitored at the target group level

## Design Decisions

- Public access is limited strictly to the ALB to minimize attack surface
- Backend services operate exclusively in private subnets
- IAM roles and SSM are used instead of SSH for secure access
- Observability is implemented at the load balancer and target group levels to validate availability and performance

