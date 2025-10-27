# aws-iac-terraform-ansible

![Terraform](https://img.shields.io/badge/Terraform-IaC-blue)
![Ansible](https://img.shields.io/badge/Ansible-CM-red)
![AWS](https://img.shields.io/badge/AWS-eu--west--1-orange)
![Status](https://img.shields.io/badge/Status-Ready-success)

## Overview
Example project provisioning a multi-tier environment (VPC, EC2, RDS) using Terraform and configuring it with Ansible.

**Region:** eu-west-1
**Author:** devopsbydhairyashil

## Architecture (ASCII)
```
Internet
   |
+-------+      +-------------+
|  ALB  | ---> | EC2 App     |
+-------+      +-------------+
                  |
                  v
               +--------+
               |  RDS   |
               +--------+
```

## What is included
- `terraform/` - basic VPC + EC2 + RDS example (variables provided)
- `ansible/` - playbook to install app & dependencies on EC2
- `app/` - simple Flask app and Dockerfile (optional)
- `.env.example`, `README.md`, `LICENSE`

## Quick notes
- Terraform files are examples; running them will create real AWS resources.
- Use a separate AWS account or understand cost implications before apply.
