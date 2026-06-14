# 🚀 Full DevOps Automation Platform (AWS)

## 📌 Overview

This project implements a fully automated end-to-end DevOps pipeline that provisions infrastructure, builds containerized applications, and deploys them to AWS using GitHub Actions and Terraform.

The platform automates the complete deployment lifecycle—from infrastructure creation to application deployment—enabling seamless delivery with minimal manual intervention.

---

## 🧱 Architecture

```text
Code → GitHub → GitHub Actions → Terraform
                                  ↓
                          AWS EC2 + IAM
                                  ↓
Docker Build → AWS ECR → EC2 Deployment
                                  ↓
                         Live Application
```

---

## ⚙️ Tech Stack

* **Cloud:** AWS (EC2, ECR, IAM)
* **Infrastructure as Code:** Terraform
* **CI/CD:** GitHub Actions
* **Containerization:** Docker
* **Backend:** Node.js (Express)
* **OS:** Linux (Amazon Linux)

---

## 🔄 Workflow

1. Developer pushes code to GitHub
2. GitHub Actions pipeline is triggered automatically
3. Terraform provisions AWS infrastructure:
   - EC2 Instance
   - Security Groups
   - IAM Roles & Instance Profiles
4. Docker image is built automatically
5. Image is pushed to AWS ECR
6. EC2 instance authenticates with ECR using IAM roles
7. Latest container image is pulled and deployed
8. Application becomes accessible through the EC2 public IP

---

## 🔐 Security

* IAM role-based authentication for AWS services
* Secrets managed using GitHub Secrets
* No hardcoded AWS credentials
* Secure SSH-based deployment
* Principle of least privilege for infrastructure access

---

## 🚀 Features

* Fully automated CI/CD pipeline
* Infrastructure provisioning using Terraform
* Docker-based containerization
* Dynamic EC2 deployment
* AWS ECR integration
* IAM role-based authentication
* Automated application updates on every code push
* Infrastructure cleanup on deployment failures

---

## 📸 Output

Application successfully deployed and accessible through the public IP of the provisioned EC2 instance.

---

## 📈 Future Improvements

* Remote Terraform State (S3 + DynamoDB)
* Manual infrastructure destroy workflow
* Application Load Balancer (ALB)
* HTTPS with custom domain (Route53 + ACM)
* Blue-Green Deployments
* Kubernetes (EKS) integration
* Multi-user deployment platform with dynamic repository support

---

## 👨‍💻 Author

**Saksham Rai**
