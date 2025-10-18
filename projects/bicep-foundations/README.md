# 🧱 Azure Bicep Foundations

A collection of **reusable Infrastructure as Code (IaC)** templates built with **Azure Bicep** to deploy core Azure resources in a consistent, modular, and automated way.

---

## 🎯 Objective
Learn, practice, and demonstrate Azure Bicep fundamentals through small, modular deployments that form the foundation for larger cloud projects.

---

## 🧰 Technologies
- **Azure Bicep** (IaC language)
- **Azure CLI**
- **Resource Groups**
- **Virtual Networks (VNets)**
- **Storage Accounts**
- **Key Vaults**

---

## ⚙️ Project Overview
1. Create a modular folder structure for reusable templates  
2. Use parameters and variables for flexible deployments  
3. Validate and deploy resources with Azure CLI  
4. Document each module and link it to higher-level projects (e.g., AKS or CS2 Server)  

---

## 📂 Folder Structure
```bash
bicep-foundations/
├── main.bicep
├── modules/
│   ├── storage.bicep
│   ├── vnet.bicep
│   └── keyvault.bicep
├── parameters/
│   └── main.parameters.json
└── docs/
