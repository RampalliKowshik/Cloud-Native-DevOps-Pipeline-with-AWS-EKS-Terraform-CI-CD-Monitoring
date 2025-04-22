# Cloud-Native-DevOps-Pipeline-with-AWS-EKS-Terraform-CI-CD-Monitoring
Cloud-Native DevOps Pipeline with AWS, EKS, Terraform, CI/CD &amp; Monitoring

Project Overview

Build and deploy a secure, observable, and cost-optimized 3-tier web application infrastructure on AWS using:

Terraform
EKS
Jenkins or GitHub Actions for CI/CD
AWS Secrets Manager
Prometheus & Grafana
CloudWatch


GitHub Repo (Source Code)
      ↓
CI/CD Pipeline (Jenkins / GitHub Actions)
      ↓
Docker Build → Test → Push to ECR → Deploy to EKS
      ↓
EKS Cluster (3-tier App)
  ├── App Pods
  ├── Secrets via Secrets Manager
  ├── Monitoring with Prometheus + Grafana
  └── Logs to CloudWatch


Infrastructure Modules (Terraform)

VPC with public/private subnets
EKS Cluster + Node Groups
RDS MySQL
ALB (Ingress)
S3 with versioning
DynamoDB for state locking
IAM roles and policies

CI/CD Pipeline Steps

Trigger pipeline on code push/PR
Build and test app
Push Docker image to ECR
Deploy to EKS using kubectl

Secrets Management

Use AWS Secrets Manager to store DB credentials
Inject secrets using CSI driver and SecretProviderClass

Monitoring & Logging

Prometheus + Grafana for cluster monitoring
CloudWatch Agent as DaemonSet for logs
CloudWatch alarms with SNS/Slack notifications

Security Hardening

IAM Access Analyzer, MFA, AWS Config
Bucket versioning, encryption, and auditing

 Cost Optimization

AWS Cost Explorer + Budgets
Trusted Advisor recommendations
S3 lifecycle policies

Backups

RDS snapshots exported to S3
Lifecycle rules for old backup management
