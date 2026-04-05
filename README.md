🚀 Full DevOps Automation Platform (AWS)
📌 Overview

This project implements a fully automated end-to-end DevOps pipeline that provisions infrastructure, builds containerized applications, and deploys them to AWS — all triggered by a single code push.

The system integrates Infrastructure as Code (Terraform) with CI/CD (GitHub Actions) and containerized deployment (Docker + ECR + EC2) to eliminate manual intervention.

🧱 Architecture
Developer → GitHub → GitHub Actions (CI/CD)
                     ↓
              Terraform (Infra Provisioning)
                     ↓
              AWS EC2 + IAM Role
                     ↓
Docker Build → AWS ECR → EC2 Pull → Container Run
                     ↓
               Live Application
⚙️ Tech Stack
Cloud: AWS (EC2, ECR, IAM)
Infrastructure as Code: Terraform
CI/CD: GitHub Actions
Containerization: Docker
Backend: Node.js (Express)
OS: Linux (Amazon Linux)
🔄 Workflow
Developer pushes code to GitHub
GitHub Actions pipeline is triggered
Terraform provisions:
EC2 instance
Security groups
IAM roles
Docker image is built
Image is pushed to AWS ECR
EC2 instance:
Pulls latest image
Stops old container
Runs updated container
Application becomes live via EC2 public IP
🔐 Security
IAM roles used for secure AWS access
GitHub Secrets used for credentials
No hardcoded secrets
Secure SSH-based deployment
🚀 Key Features
✅ Fully automated CI/CD pipeline
✅ Infrastructure provisioning using Terraform
✅ Zero manual deployment
✅ Docker-based container deployment
✅ Secure AWS integration
✅ Automatic cleanup on pipeline failure
📸 Output

Application successfully deployed and accessible via:

http://<EC2-PUBLIC-IP>
🧠 Key Learnings
Terraform state management in CI/CD
IAM roles and instance profiles
Debugging GitHub Actions pipelines
SSH-based automated deployments
End-to-end cloud automation
📈 Future Improvements
🔹 Add Load Balancer (ALB)
🔹 Enable HTTPS with custom domain
🔹 Use S3 backend for Terraform state
🔹 Deploy using AWS ECS or Kubernetes
🔹 Multi-user deployment support
👨‍💻 Author

Saksham Rai
