# eks-httpd-loadbalancer-demo

eks-httpd-loadbalancer-demo/
├── deployment.yaml
├── service.yaml
├── README.md

# 🚀 Deploying Apache HTTPD on AWS EKS using Kubernetes

This repository demonstrates how to deploy an **Apache HTTPD web server** on **AWS EKS** using Kubernetes **Deployment** and **Service (LoadBalancer)** resources, executed via **AWS CloudShell**.

---

## 📌 Architecture Overview

- AWS EKS Cluster
- Kubernetes Deployment (2 replicas)
- Apache HTTPD container (`httpd:trixie`)
- Kubernetes Service of type **LoadBalancer**
- AWS Elastic Load Balancer (ELB) auto-provisioned

---

## 🧾 Prerequisites

- AWS account with EKS cluster configured
- `kubectl` configured to access the EKS cluster
- AWS CloudShell (or local terminal with AWS CLI)

---

## 📂 Kubernetes Manifests

### 🔹 Deployment (`deployment.yaml`)
- Runs **2 replicas** of Apache HTTPD
- Exposes container on port **80**
- Uses label-based pod selection

### 🔹 Service (`service.yaml`)
- Type: **LoadBalancer**
- Exposes application publicly using AWS ELB
- Routes traffic to HTTPD pods on port **80**

---

## 🚀 Deployment Steps

```bash
# Apply Deployment
kubectl apply -f deployment.yaml

# Apply Service
kubectl apply -f service.yaml
**

## Author:**
Rohit Kumar
