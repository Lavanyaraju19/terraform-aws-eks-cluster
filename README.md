# terraform-aws-eks-cluster
Project Overview
Provisioning an Amazon EKS (Elastic Kubernetes Service) cluster using Terraform, this project leverages Infrastructure as Code (IaC) to automate scalable Kubernetes deployments on AWS. It follows a modular approach that cleanly separates networking, cluster, and provider configurations.

🚀 Perfect for learning, demos, and setting up real-world container orchestration systems.


---

Tools & Technologies
Terraform (Infrastructure as Code)

AWS EKS (Managed Kubernetes)

kubectl (Kubernetes CLI)

AWS CLI (Cloud provisioning interface)


## 📁 Project Structure
EKS-CLUSTER-TERRAFORM/
├── modules/
│   ├── eks/                  # Handles EKS cluster setup
│   │   ├── main.tf
│   │   ├── outputs.tf
│   │   └── variables.tf
│   ├── vpc/                  # Manages VPC & subnets
│   │   ├── main.tf
│   │   ├── outputs.tf
│   │   └── variables.tf
├── main.tf                   # Root module entry point
├── provider.tf               # AWS provider settings
├── outputs.tf                # Global outputs
├── kubernetes.tf             # (Optional) Kubernetes workload setup
├── .terraform.lock.hcl       # Provider dependency lock file
├── kubectl.sha256            # Kubectl checksum
├── .gitignore                # Git ignored files
├── LICENSE                   # MIT License
└── README.md                 # You're here!

🎯 Why Use Terraform for EKS?
✅ Automates Cluster Deployment — Save time and reduce manual errors
✅ Modular & Scalable — Reuse code across environments (dev, staging, prod)
✅ Cloud-Native — Integrates with AWS IAM, VPC, and Kubernetes
✅ Trackable — All infra changes are version-controlled

⚙️ Prerequisites
Before getting started, ensure the following are installed:

Terraform

AWS CLI

kubectl

An active AWS Account

(Optional) VS Code for code editing

🚀 Getting Started
1️⃣ Clone the Repository
git clone https://github.com/Lavanyaraju19/terraform-aws-eks-cluster.git
cd terraform-aws-eks-cluster

 Initialize and Apply Terraform
 terraform init
terraform plan
terraform apply

Expected Outputs:

EKS Cluster Name

Node Group IPs

VPC ID

3️⃣ Connect with kubectl
aws eks update-kubeconfig --name <CLUSTER_NAME> --region <AWS_REGION>
kubectl get nodes

Destroy the Cluster (Cleanup)
terraform destroy

 Contribute & Star
If this helped you learn or build something awesome, consider starring ⭐ this repo or sharing feedback! Contributions and suggestions are always welcome.
👩‍💻 Author
Lavanya J
DevOps Engineer | AWS Enthusiast
GitHub · LinkedIn

📜 License
This project is open source and available under the MIT License.

