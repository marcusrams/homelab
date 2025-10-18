# 🏆 AKS Leaderboard App

A scalable **leaderboard web application** deployed to **Azure Kubernetes Service (AKS)** using **GitHub Actions CI/CD**.

---

## 🎯 Objective
Deploy and manage a containerized leaderboard app that demonstrates AKS, CI/CD, and container orchestration in a production-like environment.

---

## 🧰 Technologies
- **Azure Kubernetes Service (AKS)**  
- **Azure Container Registry (ACR)**  
- **GitHub Actions (CI/CD)**  
- **Docker & YAML manifests**  
- **Ingress & Load Balancing**  

---

## ⚙️ Project Overview
1. Build and containerize a simple API + web frontend  
2. Push images to Azure Container Registry  
3. Deploy workloads to AKS via YAML or Bicep  
4. Configure GitHub Actions for automated build and deploy  
5. Add monitoring and autoscaling

---

## 📂 Folder Structure
```bash
aks-leaderboard/
├── src/
│   ├── api/
│   └── web/
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml
├── workflows/
└── docs/
