# interview-iac-repo

# GitHub Infrastructure as Code using CDKTF (TypeScript)

This repository demonstrates managing GitHub resources as **Infrastructure as Code (IaC)** using **CDK for Terraform (CDKTF)** with **TypeScript**.

The project was implemented as part of an interview assignment to showcase real-world DevOps practices, Terraform knowledge, and GitHub automation.

---

## 📌 Project Objective

The goal of this project is to manage GitHub configuration declaratively instead of performing manual setup.  
All resources are defined in code, making the setup **reproducible, auditable, and scalable**.

---

## 🚀 Features Implemented

The following GitHub resources are managed using CDKTF:

- GitHub repository creation
- Branch protection on the `main` branch
- Mandatory pull request review approval
- Force-push prevention
- GitHub Actions secret management
- Terraform outputs for verification

---

## 🧱 Managed GitHub Resources

### 1️⃣ Repository
- Name: `interview-iac-repo`
- Visibility: **Public**
- Automatically initialized with a README

> **Note:** GitHub Free accounts do not allow required pull-request reviews on private repositories.  
> To meet the assignment requirements without upgrading the plan, the repository is created as public.

---

### 2️⃣ Branch Protection
The `main` branch is protected with the following rules:

- At least **1 pull request approval** required
- Force pushes are disabled
- Rules are enforced for administrators

This ensures code quality and prevents accidental or unauthorized changes.

---

### 3️⃣ GitHub Actions Secret
- Secret Name: `APP_ENV`
- Value: `staging`

This demonstrates secure configuration management for CI/CD workflows.

---

### 4️⃣ Terraform Outputs
After deployment, the following outputs are exposed:
- Repository name
- Repository URL

These outputs confirm successful resource creation.

---

## 🛠️ Technology Stack

- **CDK for Terraform (CDKTF)**
- **Terraform**
- **TypeScript**
- **GitHub Terraform Provider**
- **Node.js**

---

## 📦 Prerequisites

Ensure the following are installed:

- Node.js (v18 or later)
- Terraform
- CDKTF CLI
- GitHub Personal Access Token (classic)

---

## 🔐 Authentication

This project uses a **GitHub Personal Access Token (classic)** with the following scopes:

- `repo`
- `admin:repo_hook`
- `workflow`
- `read:org`

Export the token before deployment:

bash
`export GITHUB_TOKEN=ghp_your_token_here`

▶️ Deployment Steps

Clone the repository and run:

npm install
cdktf deploy


Confirm the deployment when prompted.

🧩 Bonus Task Clarification

The optional bonus task required creating a GitHub Team and assigning repository permissions.

GitHub Teams are an organization-level feature. Since this project was implemented using a personal GitHub account, organization-level team management was not applicable.

The same Infrastructure as Code approach can be seamlessly extended to manage teams and permissions within a GitHub organization.

📘 Key Learnings

Managing GitHub as Infrastructure using Terraform

Using CDKTF with TypeScript for declarative automation

Handling provider version compatibility

Understanding GitHub permission scopes and platform limitations

Applying production-grade branch protection practices

