# Terraform Multi‑Cloud Infrastructure Demo

[![Terraform](https://img.shields.io/badge/Terraform-v1.x-blue)](https://www.terraform.io/)
[![AWS](https://img.shields.io/badge/AWS-Deployed-orange)](https://aws.amazon.com/)
[![Azure](https://img.shields.io/badge/Azure-Deployed-blue)](https://azure.microsoft.com/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

Infrastructure as Code demo using **Terraform** to provision workloads across **AWS** and **Azure**.  
This project showcases multi‑cloud engineering skills, networking/security best practices, and clean repo organization.

## 🚀 Features
### ![AWS Logo](https://img.shields.io/badge/AWS-Cloud-orange?logo=amazon-aws&logoColor=white)
- VPC + Public Subnet  
- Internet Gateway + Route Table  
- Security Group (SSH + HTTP)  
- EC2 Instance (Amazon Linux)  

### ![Azure Logo](https://img.shields.io/badge/Azure-Cloud-blue?logo=microsoft-azure&logoColor=white)
- Resource Group  
- Virtual Network + Subnet  
- Network Security Group (SSH + HTTP)  
- Linux Virtual Machine (Ubuntu)  

## 📂 Repository Structure
```bash
terraform-multi-cloud-infra-demo/
│── aws/
│   └── main.tf        # AWS VPC, Subnet, IGW, Route Table, Security Group, EC2
│── azure/
│   └── main.tf        # Azure Resource Group, VNet, Subnet, NSG, VM
│── README.md          # Project overview and usage
│── LICENSE
│── .gitignore


## ⚡ Quickstart

### Deploy AWS Infrastructure
```bash
cd aws
terraform init
terraform plan
terraform apply


**### Deploy Azure Infrastructure**
cd azure
terraform init
terraform plan
terraform apply

## 🏗️ Architecture (Box Style)

Below is a high‑level ASCII diagram of the AWS and Azure infrastructure provisioned by Terraform:
## 🏗️ Architecture (Box Style)

### ☁️🔶 AWS Cloud
┌───────────────────────────────┐
│   ┌───────────────┐           │
│   │ VPC           │           │
│   └───────────────┘           │
│       │                       │
│   ┌───────────────┐           │
│   │ Subnet        │           │
│   └───────────────┘           │
│       │                       │
│   ┌───────────────┐           │
│   │ Internet GW   │           │
│   └───────────────┘           │
│       │                       │
│   ┌───────────────┐           │
│   │ Route Table   │           │
│   └───────────────┘           │
│       │                       │
│   ┌───────────────┐           │
│   │ Security Group│           │
│   └───────────────┘           │
│       │                       │
│   ┌───────────────┐           │
│   │ EC2 Instance  │           │
│   └───────────────┘           │
└───────────────────────────────┘


### ☁️🔷 Azure Cloud
┌───────────────────────────────┐
│   ┌───────────────┐           │
│   │ Resource Group│           │
│   └───────────────┘           │
│       │                       │
│   ┌───────────────┐           │
│   │ Virtual Net   │           │
│   └───────────────┘           │
│       │                       │
│   ┌───────────────┐           │
│   │ Subnet        │           │
│   └───────────────┘           │
│       │                       │
│   ┌───────────────┐           │
│   │ NSG           │           │
│   └───────────────┘           │
│       │                       │
│   ┌───────────────┐           │
│   │ NIC           │           │
│   └───────────────┘           │
│       │                       │
│   ┌───────────────┐           │
│   │ Linux VM      │           │
│   └───────────────┘           │
└───────────────────────────────┘

## 🔄 Workflow
- Initialize Terraform → terraform init
- Plan Infrastructure → terraform plan
- Apply Changes → terraform apply
- Destroy Resources → terraform destroy (when cleaning up)

## 📖 Learning Outcomes
- Demonstrates multi‑cloud provisioning with Terraform.
- Shows understanding of networking, security, and compute across providers.
- Provides a recruiter‑ready portfolio project with clean structure and documentation.

## 🔮 Future Work
- Add variables.tf and outputs.tf for parameterization  
- Integrate Terraform modules for reusability  
- Expand with load balancers, storage, and monitoring  
- Add CI/CD pipeline for automated deployments  
- Extend to GCP for full tri‑cloud demo  
```

## 🏗️ Architecture (Mermaid)
```mermaid
%% AWS Diagram
flowchart LR
  subgraph AWS["☁️ AWS Cloud"]
    VPC --> Subnet --> IGW --> RT --> SG --> EC2
  end

  %% AWS colors
  style VPC fill:#4CAF50,stroke:#333,stroke-width:2px,color:#fff
  style Subnet fill:#2196F3,stroke:#333,stroke-width:2px,color:#fff
  style IGW fill:#FF9800,stroke:#333,stroke-width:2px,color:#fff
  style RT fill:#9C27B0,stroke:#333,stroke-width:2px,color:#fff
  style SG fill:#00BCD4,stroke:#333,stroke-width:2px,color:#fff
  style EC2 fill:#F44336,stroke:#333,stroke-width:2px,color:#fff
```
```mermaid
%% Azure Diagram
flowchart TD
  subgraph Azure["☁️ Azure Cloud"]
    RG --> VNet --> SubnetA --> NSG --> NIC --> VM
  end

  %% Azure colors
  style RG fill:#8BC34A,stroke:#333,stroke-width:2px,color:#fff
  style VNet fill:#03A9F4,stroke:#333,stroke-width:2px,color:#fff
  style SubnetA fill:#FF5722,stroke:#333,stroke-width:2px,color:#fff
  style NSG fill:#673AB7,stroke:#333,stroke-width:2px,color:#fff
  style NIC fill:#009688,stroke:#333,stroke-width:2px,color:#fff
  style VM fill:#E91E63,stroke:#333,stroke-width:2px,color:#fff

```



