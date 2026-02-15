---
title: "CI/CD Pipeline Project | Jenkins → AWS EKS"
datePublished: Sun Feb 15 2026 09:31:07 GMT+0000 (Coordinated Universal Time)
cuid: cmlnjpl7a000102jpds8vd6qm
slug: cicd-pipeline-project-jenkins-aws-eks
tags: aws, devops

---

I recently completed a hands-on DevOps project where I designed and deployed an end-to-end CI/CD pipeline using Jenkins, GitHub, Docker, Amazon ECR, and Amazon EKS on AWS ☁️  
  
The goal was to build a production-style CI/CD workflow where every code commit automatically builds, containerizes, and deploys an application to Kubernetes.  
  
🔧 What I built  
✅ Jenkins installed on Amazon EC2  
✅ Pipeline as Code using Jenkinsfile  
✅ GitHub Webhook–based automatic triggers  
✅ Docker image build & push to Amazon ECR  
✅ Kubernetes deployment on Amazon EKS  
✅ Secure access using IAM Roles (no hard-coded AWS keys 🔐)  
  
🔄 CI/CD Workflow  
1️⃣ Code pushed to GitHub (main)  
2️⃣ Webhook triggers Jenkins  
3️⃣ Jenkins builds Docker image  
4️⃣ Image pushed to Amazon ECR  
5️⃣ Jenkins deploys to Amazon EKS  
6️⃣ App exposed via AWS LoadBalancer  
  
🏗️ Architecture (High-Level)  
  
┌────────────┐  
│ Developer │  
└─────┬──────┘  
│ git push  
▼  
┌──────────────┐  
│  GitHub   │  
│ (Repository) │  
└─────┬────────┘  
│ Webhook Trigger  
▼  
┌─────────────────────────┐  
│ Jenkins Server     │  
│ (EC2 - Ubuntu)     │  
│             │  
│ • Checkout Code     │  
│ • Build Docker Image  │  
│ • Push Image to ECR   │  
│ • Deploy to EKS     │  
└─────┬───────────────────┘  
│ Docker Image  
▼  
┌─────────────────────────┐  
│ Amazon ECR       │  
│ (Container Registry)  │  
└─────┬───────────────────┘  
│ Image Pull  
▼  
┌─────────────────────────┐  
│ Amazon EKS       │  
│ (Kubernetes Cluster)  │  
│             │  
│ • Deployment      │  
│ • Service (LB)     │  
└─────┬───────────────────┘  
│  
▼  
┌─────────────────────────┐  
│ AWS LoadBalancer    │  
└─────┬───────────────────┘  
│  
▼  
┌─────────────────────────┐  
│ End Users / Browser   │  
└─────────────────[────────┘  
  
  
🌐 Project L](https://lnkd.in/g9ebn-Xv)inks  
🔗 GitHub Repo: [**https://lnkd.in/g9ebn-Xv**  
  
🧠](https://lnkd.in/g9ebn-Xv￼￼🧠) Key Learnings  
Real-world CI/CD pipeline design  
Jenkins + Kubernetes integration  
Secure AWS authentication with IAM Roles  
Container lifecycle automation  
Debugging CI/CD & Kubernetes deployments  
  
This project significantly strengthened my DevOps, AWS, and Kubernetest Fundamentals.

[  
  
](https://www.linkedin.com/search/results/all/?keywords=%23aws&origin=HASH_TAG_FROM_FEED)