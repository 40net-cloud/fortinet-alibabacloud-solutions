# Alibaba Cloud FortiGate-VM Deployment with Terraform

This repository contains Terraform configurations for deploying a FortiGate-VM instance with the required infrastructure. It includes VPC, VSwitches, Route Tables, Security Groups, and FortiGate instance provisioning.

## 📋 Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Pre-requisites](#pre-requisites)
- [Configuration](#configuration)
- [Variables](#variables)
- [Usage](#usage)
- [Resources Created](#resources-created)

## 📖 Overview

This Terraform configuration automates the setup of a secure VPC environment on Alibaba Cloud. It creates the following components:

- A VPC with an external and internal VSwitch.
- Security groups with rules for both ingress and egress traffic.
- Route tables and entries for traffic routing.
- A FortiGate instance with 2x ENIs (Elastic Network Interface).
- User data configuration for FortiGate initial setup.

## 🛠️ Architecture

coming soon

## ✅ Pre-requisites

- Terraform installed (version >= 1.0)
- Alibaba Cloud account with API credentials configured
- FortiGate image ID and license details
- Valid Alibaba Cloud Access Key and Secret Key
- Properly configured terraform.tfvars file

## 📝 Configuration

Create a terraform.tfvars file to specify your configuration. You can check "terraform.tfvars.example" for guidance.

## 🚀 Usage

Follow these steps to deploy the infrastructure using Terraform:

### 1. Initialize Terraform

Run the following command to initialize the Terraform environment:

```bash
terraform init
```
### 2. Plan the Deployment

Review the changes that Terraform will make without applying them yet:

```bash
terraform plan
```

### 3. Apply the Configuration

Deploy the infrastructure with:

```bash
terraform apply -auto-approve
```

The -auto-approve flag automatically approves the changes, so you don't have to confirm them manually.

## 📦 Resources Created

This Terraform configuration creates the following Alibaba Cloud resources:

- VPC: A new VPC with a specified CIDR block.
- VSwitches: External and internal VSwitches for network segmentation.
- Security Groups: Rules for allowing all ingress and egress TCP traffic.
- Route Table: A route table with a default route pointing to the FortiGate instance.
- FortiGate Instance: A FortiGate-VM instance with attached ENIs for inspecting traffic.
- ENI: 2x Elastic Network Interfaces attached to the FortiGate for internal and external network traffic.
