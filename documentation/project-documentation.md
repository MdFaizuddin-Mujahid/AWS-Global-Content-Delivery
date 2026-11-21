
# Project Documentation: AWS Global Content Delivery

## 1. Project Objective

To deploy a static website on AWS and configure a content delivery architecture using Amazon CloudFront, an Application Load Balancer, and multiple EC2 web servers across different Availability Zones.

## 2. EC2 Web Server Configuration

- Launched Amazon Linux 2023 EC2 instances.
- Installed and configured Apache HTTP Server.
- Deployed the Lantern River static website.
- Created an AMI from the configured web server.
- Launched a second EC2 instance using the AMI.

## 3. Application Load Balancer Configuration

- Created an internet-facing Application Load Balancer named `Lantern-LB`.
- Configured an HTTP listener on port 80.
- Created a target group named `lantern-river-tg`.
- Registered both EC2 instances.
- Configured HTTP health checks using the `/` path.
- Verified that both registered targets became healthy.

## 4. CloudFront Configuration

- Created an Amazon CloudFront distribution.
- Configured the Application Load Balancer as the origin.
- Configured the origin connection to use HTTP.
- Tested website delivery through the CloudFront distribution.
- Verified website access from multiple devices.

## 5. Deployment Details

| Component | Configuration |
|---|---|
| AWS Region | ap-south-1 |
| Operating System | Amazon Linux 2023 |
| Web Server | Apache |
| EC2 Instances | 2 |
| Availability Zones | ap-south-1a, ap-south-1b |
| Load Balancer | Application Load Balancer |
| Target Group | lantern-river-tg |
| Content Delivery | Amazon CloudFront |

## 6. Testing and Validation

- Verified website access through EC2.
- Tested the Application Load Balancer DNS endpoint.
- Confirmed both target group instances were healthy.
- Tested website access through CloudFront.
- Verified access from multiple devices.

## 7. Key Learnings

- Hosting websites on Amazon EC2.
- Creating and using AMIs.
- Deploying infrastructure across Availability Zones.
- Configuring Application Load Balancers and target groups.
- Understanding target health checks.
- Configuring CloudFront with a custom origin.
- Understanding the CloudFront-to-ALB-to-EC2 delivery flow.

## 8. Resource Cleanup

After completing implementation, testing, and capturing screenshots, the AWS resources were deleted to avoid ongoing charges.

This repository preserves the project documentation, architecture, and implementation evidence.
