# My Infrastructure as Code (IaC) Portfolio

Welcome to my **IaC Portfolio**, a comprehensive showcase of my expertise in DevOps and cloud automation using:

* **Terraform** for infrastructure provisioning
* **Ansible** for configuration management
* **Kubernetes** for orchestration
* **Python AWS Lambda** for serverless tasks
* **GitHub Actions** for CI/CD pipelines
* **New Relic** for observability and APM

> This project is structured to be modular, reproducible, scalable, and observable.

## Repository Structure

```plaintext
├── terraform/
│   ├── modules/
│   ├── environments/
│   └── main.tf
├── ansible/
│   ├── playbooks/
│   ├── roles/
├── k8s/
│   ├── manifests/
│   └── helm-charts/
├── lambda/
│   └── my_lambda_function/
│       ├── app.py
│       └── requirements.txt
├── .github/
│   └── workflows/
│       ├── terraform.yml
│       ├── ansible.yml
│       ├── lambda-deploy.yml
│       └── k8s-deploy.yml
├── dashboards/
│   └── newrelic/
│       ├── alerts.json
│       └── dashboards.json
├── README.md
└── LICENSE
```

## What's Included

| Component           | Description                                                        |
| ------------------- | ------------------------------------------------------------------ |
| **Terraform**       | Provisions VPC, EKS cluster, RDS, S3, Lambda, IAM                  |
| **Ansible**         | Installs and configures monitoring agents and OS tuning            |
| **Kubernetes**      | Manages workloads via Helm, including autoscaling and service mesh |
| **Lambda (Python)** | Automates tasks (e.g., backup, notifications, health checks)       |
| **GitHub Actions**  | End-to-end CI/CD: test, build, deploy, notify                      |
| **New Relic**       | Full stack observability: APM, logs, infra, custom dashboards      |

## GitHub Actions CI/CD Workflows

* `terraform.yml`: Runs `plan` and `apply` on PR and merge
* `ansible.yml`: Connects to EC2 and applies playbooks
* `lambda-deploy.yml`: Zips and deploys Python Lambda to AWS
* `k8s-deploy.yml`: Applies manifests or Helm charts to EKS

## Observability (New Relic)

This repo includes:

* Application dashboards
* Infrastructure alert policies
* Custom metrics (Lambda + K8s)
* Integration with CI to notify on deployments

## Requirements

* AWS CLI and credentials
* Terraform ≥ 1.4
* Ansible ≥ 2.10
* Python ≥ 3.9 (for Lambda)
* kubectl + Helm
* GitHub Actions runners with AWS IAM permissions

## Advanced Project Ideas

### 1. Cloud Native Portfolio Manager

Spin up and monitor EKS clusters for demo apps.

* Stack: Terraform + Helm + GitHub Actions + New Relic + EKS Fargate
* Features: Self-healing, ephemeral TTL, event-driven automation

### 2. Lambda-Powered Auto Remediator

Auto-remediate issues triggered by alerts.

* Stack: Python Lambda + GitHub Actions + Terraform + New Relic + SSM
* Features: Lambda remediations via Ansible triggered by New Relic

### 3. K8s Chaos Engineering Lab

Controlled chaos experiment lab with GitHub Actions.

* Stack: Kubernetes + Terraform + LitmusChaos + New Relic
* Features: Chaos injection and monitoring via dashboards

### 4. Fullstack Observability Pipeline

End-to-end monitoring for IaC-managed workloads.

* Stack: New Relic + Lambda (custom metrics) + Ansible + Terraform
* Features: Dashboards as code, auto-alert sync with commits

### 5. GitOps Platform Bootstrapping

Spin up a GitOps-ready K8s cluster from a single GitHub repo.

* Stack: Terraform + ArgoCD + GitHub Actions + Kustomize + Helm + New Relic
* Features: Canary deploys, PR-based GitOps, automated rollback
