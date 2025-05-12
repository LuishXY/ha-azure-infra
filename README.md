
# 🌐 Multi-Region High Availability on Azure with Terraform

This project provisions a **highly available, multi-region Azure infrastructure** using Terraform. It demonstrates cloud-native design principles with **active-active deployment**, **global load balancing**, and **resilient service architecture** using Azure Front Door and App Services.

---

## 🧠 Key Concepts

| Concept                   | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| 🌍 Multi-Region Deployments | Services are deployed in `East US` and `West Europe`                       |
| ⚖️ Global Load Balancing  | Azure Front Door distributes traffic with health probes and failover       |
| ☁️ App Services (Linux)   | Stateless web apps hosted in App Service Plans in both regions              |
| 🛡️ Highly Available Design | Resilient to regional failures using native Azure redundancy mechanisms     |
| 🔐 Terraform Best Practices | Modular, clean codebase with providers split by region                      |

---

## 🏗️ Architecture

```
graph TD
  user[User Request] --> AFD[Azure Front Door]
  AFD --> EAST[App Service - East US]
  AFD --> WEST[App Service - West Europe]
```


multi-region-ha/
├── main.tf         # Resources: App Services, Front Door, Plans, Groups
├── providers.tf    # Multi-region provider aliases
├── variables.tf    # Parameterized values
├── outputs.tf      # Output URLs, IDs
├── README.md       # You're here
