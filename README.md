# 🚀 DevOps Learning Journey

Welcome to my **DevOps Learning Journey** repository — a curated, step-by-step path to mastering DevOps from the ground up. This guide is structured as both a self-study curriculum and a portfolio of practical projects, broken down into folders for each key topic.

Whether you're just starting or want to solidify your skills, this repo will help you understand and apply DevOps principles with real-world tools and use cases.

---

## 📚 Why DevOps?

DevOps bridges the gap between **development** and **operations**, emphasizing **collaboration**, **automation**, and **continuous delivery**. It’s not just about tools—it's a mindset shift. Mastering DevOps allows you to:
- Ship faster and more reliably
- Reduce human error
- Scale systems efficiently
- Automate everything

---

## 🗺️ Roadmap Overview

Each section below corresponds to a folder in this repo (e.g., `01-linux-basics/`, `02-git-basics/`...), containing detailed examples, mini-projects, and notes.

---

### ✅ `01-linux-basics/` — Master the Command Line

DevOps runs on Linux. You need to be fluent in the terminal.

#### Topics:
- Navigating the filesystem (`cd`, `ls`, `pwd`, `tree`)
- Managing files (`cp`, `mv`, `rm`, `touch`, `cat`, `nano`)
- Permissions (`chmod`, `chown`)
- Networking (`ping`, `netstat`, `ss`, `curl`)
- Background jobs & processes (`top`, `htop`, `ps`, `kill`)
- Shell scripting basics

> 📁 This folder will include example shell scripts and cheat sheets.

---

### ✅ `02-git-basics/` — Version Control with Git & GitHub

Understand version control workflows and collaboration.

#### Topics:
- Git basics (`clone`, `add`, `commit`, `push`, `pull`)
- Branching strategies (`feature`, `main`, `hotfix`)
- Merging, rebasing, resolving conflicts
- Writing good commit messages
- Using GitHub Issues, PRs, and Projects
- Intro to GitOps (versioning your infrastructure)

> 📁 This folder will simulate a team environment with sample PRs, merge conflicts, and review examples.

---

### ✅ `03-docker/` — Containerization with Docker

Learn how to package applications and environments into containers.

#### Topics:
- What is Docker and why use it?
- Images vs Containers
- Writing a `Dockerfile`
- Building and tagging images
- Using Docker Compose
- Pushing to Docker Hub
- Common Docker CLI commands

> 📁 This folder will include containerized Node.js, Python, and static apps.

---

### ✅ `04-github-actions-cicd/` — Continuous Integration & Delivery

Automate your testing and deployment workflows.

#### Topics:
- What is CI/CD?
- Writing GitHub Actions workflows (`.github/workflows/`)
- Linting, testing, and building on push
- Secrets management
- Deploying to a cloud server
- Matrix builds and job strategies

> 📁 Sample workflows for JS, Python, and Docker apps will be included.

---

### ✅ `05-infrastructure-as-code/` — IaC with Terraform

Manage infrastructure through code. No more clicking through cloud UIs.

#### Topics:
- Terraform basics: providers, resources, variables
- Provisioning EC2, S3, VPC on AWS
- Reusable modules
- State files and remote backends
- Plan, apply, and destroy safely

> 📁 Examples will include AWS deployments (with `terraform.tf` files and diagrams).

---

### ✅ `06-cloud-platforms/` — Getting Hands-On with the Cloud

Choose a cloud platform: AWS (recommended), Azure, or GCP.

#### Topics:
- Compute (EC2, Lambda)
- Storage (S3, EBS)
- IAM (users, roles, permissions)
- VPC & Networking (subnets, security groups)
- Billing and cost estimation

> 📁 This folder will contain provisioning scripts and cloud setup examples.

---

### ✅ `07-kubernetes-basics/` — Orchestration with Kubernetes

Master container orchestration with K8s.

#### Topics:
- Pods, Deployments, ReplicaSets
- Services and Ingress
- ConfigMaps and Secrets
- Minikube or KIND for local clusters
- Helm basics

> 📁 Example K8s deployments and real-world cluster setups.

---

### ✅ `08-monitoring-logging/` — Observability Stack

Keep your systems healthy and traceable.

#### Topics:
- Metrics with Prometheus
- Visualization with Grafana
- Logs with Loki or ELK
- Health checks, alerts, uptime tracking

> 📁 Example dashboards, Prometheus scrapers, and Grafana templates.

---

## 🌟 Bonus Projects (Coming Soon)

| Folder | Project |
|--------|---------|
| `projects/static-site-cicd/` | Deploy a static site with CI/CD and custom domain |
| `projects/infra-code-saas/` | Full-stack app deployed via Terraform |
| `projects/k8s-observability/` | Monitor a K8s cluster using Prometheus & Grafana |

---

## 🛠️ Tooling Checklist

Here are the tools you'll use throughout the journey:

| Category | Tool |
|----------|------|
| OS / Shell | Linux, Bash |
| VCS | Git, GitHub |
| Containers | Docker, Docker Compose |
| CI/CD | GitHub Actions |
| IaC | Terraform |
| Cloud | AWS (EC2, S3, IAM, etc.) |
| Orchestration | Kubernetes |
| Monitoring | Prometheus, Grafana, Loki |

---

## 👨‍💻 Contribution & Updates

I’m actively working through these steps, committing progress as I go. You can fork this repo to follow along or adapt it to your own journey.

> 💬 PRs, suggestions, and issues welcome!

---

## 🧠 Stay Connected

If you’re following along or building your own DevOps journey, let’s connect!  
Find me on [LinkedIn](#), [X](#), or [Dev.to](#) and tag your repo/blog with **#DevOpsJourney**.

---

## 🚀 Let's Go!

Check out the first step: [`01-linux-basics/`](./01-linux-basics/)

---

