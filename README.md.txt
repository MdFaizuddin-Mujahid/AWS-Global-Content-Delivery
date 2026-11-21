
# AWS Global Content Delivery

A hands-on AWS cloud infrastructure project demonstrating global content delivery using Amazon CloudFront, an Application Load Balancer, and multiple Amazon EC2 web servers.

## Project Overview

This project demonstrates how to distribute website traffic through Amazon CloudFront and an Application Load Balancer to two EC2 web servers deployed across separate Availability Zones in the AWS Mumbai Region (`ap-south-1`).

## AWS Services Used

- **Amazon CloudFront** – Content delivery and HTTPS access for website visitors.
- **Application Load Balancer (ALB)** – Distributes incoming requests across EC2 instances.
- **Amazon EC2** – Hosts the static Lantern River website.
- **Amazon Machine Image (AMI)** – Used to launch the second web server.
- **Amazon VPC** – Provides network infrastructure.
- **Target Groups** – Manage and monitor registered EC2 targets.

## Architecture

See [Architecture Diagram](architecture/architecture-diagram.md).

## Implementation Highlights

- Hosted a static website on Amazon Linux 2023 EC2 instances using Apache.
- Created an AMI from the configured web server.
- Launched a second EC2 instance in a separate Availability Zone.
- Configured an Application Load Balancer and registered both EC2 instances.
- Verified that both targets became healthy.
- Configured Amazon CloudFront with the ALB as its origin.
- Tested website access through the CloudFront distribution from multiple devices.

## Screenshots

Project implementation screenshots are available in the [`screenshots/`](screenshots/) directory.

## Documentation

Additional project documentation is available in the [`documentation/`](documentation/) directory.

## Deployment Status

The AWS infrastructure was deployed and tested successfully. The resources were subsequently deleted to avoid ongoing AWS charges.

This repository preserves the project architecture, implementation documentation, and screenshots.

## Region

AWS Asia Pacific (Mumbai) – `ap-south-1`

## Author

Md Faizuddin
