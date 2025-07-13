# Medusa Backend Deployment to AWS ECS

This project automates the deployment of the [Medusa](https://medusajs.com/) backend to **Amazon ECS (Fargate)** using **Terraform** and **GitHub Actions**.

---

## 🚀 Tech Stack

- **AWS ECS (Fargate)**
- **Terraform**
- **GitHub Actions**
- **Amazon ECR**
- **Docker**

---

## 📁 Project Structure

```bash
.
├── docker/
│   └── medusa-backend/      # Medusa backend source code
├── .github/
│   └── workflows/
│       └── deploy.yml       # GitHub Actions CI/CD pipeline
├── main.tf                  # Terraform infrastructure definition
├── variables.tf             # Terraform variables
├── terraform.tfvars         # Terraform values
├── outputs.tf               # Terraform outputs
└── README.md

🧩 Features
Infrastructure as Code using Terraform

Push to main branch triggers:

Docker image build

Push to Amazon ECR

Auto deployment to ECS Fargate

Auto provisioning:

VPC, Subnet, Internet Gateway

ECS Cluster, Task Definition, and Service

IAM Role for ECS task execution

Security Group for port 9000

⚙️ How to Use
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/medusa-ecs-deploy.git
cd medusa-ecs-deploy
2. Configure Secrets in GitHub
Go to your GitHub repo → Settings → Secrets and variables → Actions, and add the following:

Secret Name	Description
AWS_ACCESS_KEY_ID	Your AWS access key
AWS_SECRET_ACCESS_KEY	Your AWS secret key
ECR_REGISTRY	AWS ECR registry URL (e.g. 123456789012.dkr.ecr.us-east-2.amazonaws.com)
ECR_REPOSITORY	Your ECR repository name (e.g. medusa-backend)

3. Initialize and Apply Terraform
bash
Copy
Edit
terraform init
terraform apply
This will:

Provision your ECS infrastructure on AWS

Create ECR, ECS Cluster, Task Definition, and Service

4. Push Your Code to Deploy
bash
Copy
Edit
git add .
git commit -m "Initial commit with deploy workflow"
git push origin main
GitHub Actions will:

Build Docker image

Push to ECR

Trigger ECS deployment


Results:

<img width="1920" height="1080" alt="Screenshot (314)" src="https://github.com/user-attachments/assets/28850fc1-3c15-43b2-9407-4be97b8d86ce" />
