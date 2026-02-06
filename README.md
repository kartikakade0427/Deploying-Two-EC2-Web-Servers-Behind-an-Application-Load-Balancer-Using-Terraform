# Deploying Two EC2 Web Servers Behind an Application Load Balancer Using Terraform
## _Highly Available AWS Infrastructure using IaC_

[![Terraform](https://img.shields.io/badge/Terraform-IaC-blueviolet)](https://www.terraform.io/)
[![AWS](https://img.shields.io/badge/AWS-Cloud-orange)](https://aws.amazon.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

This project demonstrates how to deploy a highly available web infrastructure on AWS using Terraform. It provisions a custom VPC, public subnets across multiple Availability Zones, EC2 instances running Nginx, and an Application Load Balancer (ALB) that distributes HTTP traffic between servers.

- Infrastructure as Code using Terraform
- Custom VPC and public subnets
- Two EC2 instances with Nginx
- Application Load Balancer with health checks
- Secure networking using security groups
- High availability architecture

---

## Architecture

Internet
|
Application Load Balancer
|
Target Group
|
EC2 (AZ-1) EC2 (AZ-2)
| |
Public Subnet-1 Public Subnet-2
|
Route Table → Internet Gateway 


---

## Tech

This project uses a number of open source technologies:

- [Terraform] - Infrastructure as Code tool
- [AWS EC2] - Virtual Servers
- [AWS VPC] - Networking
- [AWS ALB] - Load Balancer
- [Nginx] - Web Server
- [Linux] - Operating System

---

## Installation

Terraform and AWS CLI must be installed.

Verify:

```sh
terraform --version
aws --version
git --version

## Configure AWS Credentials
aws configure

## Project Structure

.
├── main.tf
├── variables.tf
├── terraform.tfvars
├── outputs.tf
├── .gitignore
└── README.md

## Clone Repository
git clone https://github.com/kartikakade0427/Deploying-Two-EC2-Web-Servers-Behind-an-Application-Load-Balancer-Using-Terraform.git
cd Deploying-Two-EC2-Web-Servers-Behind-an-Application-Load-Balancer-Using-Terraform


## Create terraform.tfvars
nano terraform.tfvars

aws_region    = "us-east-1"
ami_id        = "ami-0532be01f26a3de55"
instance_type = "t2.micro"

## Deployment

##Initialize Terraform:
terraform init

##Validate:
terraform validate

##Plan:
terraform plan

##Apply:
terraform apply

##Verify Deployment
Get ALB DNS:
