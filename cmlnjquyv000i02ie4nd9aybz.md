---
title: "Hands-on with AWS EKS & Kubernetes | Apache HTTPD Deployment"
datePublished: Sun Feb 15 2026 09:32:07 GMT+0000 (Coordinated Universal Time)
cuid: cmlnjquyv000i02ie4nd9aybz
slug: hands-on-with-aws-eks-and-kubernetes-apache-httpd-deployment
tags: aws, devops

---

I deployed an Apache HTTPD application on AWS EKS using Kubernetes, entirely via AWS CloudShell, and exposed it publicly using a Service of type LoadBalancer.  
🔹 What I implemented  
Kubernetes Deployment with 2 replicas  
Apache HTTPD container (httpd:trixie)  
LoadBalancer Service that auto-provisioned an AWS ELB  
Verified pod availability and external access via ELB DNS  
  
🔹 GitHub workflow followed  
Created a new feature branch from main  
Added/updated Kubernetes manifests (deployment.yaml, service.yaml)  
Updated documentation  
Pushed changes and merged back to main  
  
🔗 GitHub Repository:  
[**https://lnkd.in/g79FnWdR**  
  
This pro](https://lnkd.in/g79FnWdR)ject helped reinforce core Kubernetes & EKS concepts:  
• Deployments & replica management  
• Label-based service discovery  
• How EKS integrates with AWS networking (ELB)  
• Clean Git branching & version control practices  
  
📌 Next steps: Ingress with ALB, HPA, HTTPS, and CI/CD integration.  
Always learning by building 🚀  
Happy to connect with fellow DevOps & Cloud enthusiasts