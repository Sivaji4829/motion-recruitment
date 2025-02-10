A)
1. Create the new repository name motion-recruitment
2. Clone-> git clone https://github.com/Vikku03/motion-recruitment-devops.git
3. Change the directory-> cd motion-recruitment-devops

B)
AWS Deployment Steps:
1. Create and Merge feature-aws-setup Branch: git checkout -b feature-aws-setup
2. Create the md file:

# AWS Setup Guide

## Step 1: Create an AWS Account
1. Go to [AWS Sign-up](https://aws.amazon.com/).
2. Follow the instructions to create an account and set up billing.

## Step 2: Launch an EC2 Instance
1. Go to **AWS Management Console** > **EC2**.
2. Click **Launch Instance** and choose:
   - **Amazon Linux 2 AMI**
   - **Instance Type**: t2.micro (Free tier eligible)
   - **Key Pair**: Create/download key pair.
   - **Security Group**: Allow SSH (port 22).

## Step 3: Deploy a Python Script
1. Connect via SSH:
   ```sh
   ssh -i your-key.pem ec2-user@your-ec2-ip

#### **Commit and Merge**
```sh
git add aws-setup.md
git commit -m "Added AWS setup documentation"
git checkout main
git merge feature-aws-setup
git push origin main


C)
Azure Deployment Steps
# Repeat the same for Azure as aws 
# Azure Setup Guide

## Step 1: Create an Azure Account
1. Go to [Azure Sign-up](https://portal.azure.com/).
2. Follow the steps to create a free-tier account.

## Step 2: Create a Virtual Machine
1. Navigate to **Azure Portal** > **Virtual Machines**.
2. Click **Create VM**, choose:
   - Image: Ubuntu 20.04 LTS
   - Size: Standard_B1s
   - Authentication: SSH key

## Step 3: Deploy a Python Script
1. Connect to VM:
   ```sh
   ssh azure-user@your-vm-ip

# Repeat the commit same as aws

D)
GCP:
# Repeat the same
# GCP Setup Guide

## Step 1: Create a GCP Account
1. Sign up at [Google Cloud Console](https://console.cloud.google.com/).
2. Set up a free-tier project.

## Step 2: Create a Compute Engine Instance
1. Navigate to **Compute Engine** > **VM instances**.
2. Click **Create Instance**, choose:
   - Machine Type: e2-micro (Free tier)
   - OS: Debian-based

## Step 3: Deploy a Python Script
1. Connect via SSH:
   ```sh
   gcloud compute ssh your-instance-name

# Repeat the commit same for gcp as azure and aws

E)Final Step:

git branch  
echo "Add Description according to the task" > README.md  
git add README.md  
git commit -m "Initial commit"  
git branch -m master main  
git push -u origin main  
git remote -v  
git push -u origin HEAD  

