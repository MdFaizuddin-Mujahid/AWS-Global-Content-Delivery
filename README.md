
# AWS Global Content Delivery

A hands-on AWS project demonstrating website delivery through Amazon CloudFront, an Application Load Balancer, and multiple Amazon EC2 web servers deployed across different Availability Zones.

## Project Overview

The objective was to host a static website on AWS and build a content delivery architecture using Amazon CloudFront and an Application Load Balancer.

The website was hosted on two EC2 instances across separate Availability Zones in the AWS Mumbai Region.

## AWS Services Used

- **Amazon CloudFront** – Content delivery and HTTPS viewer access.
- **Application Load Balancer** – Distributes incoming requests across EC2 instances.
- **Amazon EC2** – Hosts the static website using Apache HTTP Server.
- **Amazon Machine Image (AMI)** – Used to launch the second web server.
- **Amazon VPC** – Network infrastructure.
- **Target Groups** – Register EC2 instances and monitor their health.

## Architecture

```text
Users / Browsers
       |
       v
Amazon CloudFront
       |
       | HTTP Origin Connection
       v
Application Load Balancer
       |
       v
Target Group
      / \
     /   \
    v     v
  EC2-1  EC2-2
  AZ-1a  AZ-1b
```

## Implementation Highlights

- Launched Amazon Linux 2023 EC2 instances.
- Installed and configured Apache HTTP Server.
- Hosted the Lantern River static website.
- Created an AMI from the configured web server.
- Launched a second EC2 instance using the AMI.
- Deployed web servers across two Availability Zones.
- Configured an Application Load Balancer and target group.
- Verified both EC2 targets were healthy.
- Configured Amazon CloudFront with the ALB as its origin.
- Tested website access through CloudFront from multiple devices.

## Testing and Validation

- Verified website access through EC2.
- Tested the Application Load Balancer DNS endpoint.
- Confirmed both target group instances were healthy.
- Tested website delivery through CloudFront.
- Verified access from multiple devices.

## Project Structure

```text
AWS-Global-Content-Delivery/
│
├── architecture/
│   └── architecture-diagram.md
│
├── documentation/
│   └── project-documentation.md
│
└── screenshots/
```

## Deployment Details

| Configuration | Details |
|---|---|
| AWS Region | ap-south-1 (Mumbai) |
| Operating System | Amazon Linux 2023 |
| Web Server | Apache HTTP Server |
| Load Balancer | Application Load Balancer |
| Content Delivery | Amazon CloudFront |
| EC2 Instances | 2 |
| Availability Zones | ap-south-1a, ap-south-1b |
| Website | Lantern River (TemplateMo) |

## Resource Cleanup

After successful testing and capturing project screenshots, the AWS infrastructure was deleted to avoid ongoing charges.

This repository preserves the architecture, documentation, and implementation evidence.

## Author

Md Faizuddin
