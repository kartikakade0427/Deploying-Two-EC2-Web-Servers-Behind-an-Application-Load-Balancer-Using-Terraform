##🚀 Deploying Two EC2 Web Servers Behind an Application Load Balancer Using Terraform**
📌 Project Overview

This project demonstrates how to build a highly available web infrastructure on AWS using Terraform. It provisions a custom VPC, public subnets across multiple availability zones, EC2 instances running Nginx, and an Application Load Balancer (ALB) that distributes HTTP traffic between the servers.

##**🏗 Architecture Diagram**

Internet
   |
Application Load Balancer
   |
Target Group
   |
EC2 (AZ-1)        EC2 (AZ-2)
   |                |
Public Subnet-1   Public Subnet-2
   |
Route Table → Internet Gateway

##**🛠 Prerequisites**

AWS Account

Terraform installed

AWS CLI installed

Git installed

IAM user with required permissions

**📁 Project Structure**

.
├── main.tf
├── variables.tf
├── terraform.tfvars
├── outputs.tf
├── .gitignore
└── README.md

**🔗 Clone Repository**

git clone https://github.com/kartikakade0427/Deploying-Two-EC2-Web-Servers-Behind-an-Application-Load-Balancer-Using-Terraform.git
cd Deploying-Two-EC2-Web-Servers-Behind-an-Application-Load-Balancer-Using-Terraform

