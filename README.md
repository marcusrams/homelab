# homelab
 
My homelab — built on a dedicated PC running Proxmox. Documenting everything as I set it up.
 
I'm using this to learn the things I need for a DevOps role — Linux, Docker, Kubernetes, Terraform. Everything is set up manually using official documentation. If something breaks I fix it myself before asking for help.
 
---
 
## Hardware
 
| Component | Spec |
|-----------|------|
| Machine | Dell Optiplex 3080 SFF |
| CPU | Intel Core i5-10500 |
| RAM | 16GB |
| Storage A — Boot/Hot | 256GB M.2 NVMe SSD — Proxmox OS + VM root partitions (IOPS) |
| Storage B — Capacity/Cold | 1TB SATA HDD — ISOs, VZDump backups, long-term storage |
| Hypervisor | Proxmox VE |
 
---
 
## Current setup
 
```
Proxmox host
├── VM: ubuntu-server-01
├── VM: ubuntu-server-02   (planned)
└── VM: ubuntu-server-03   (planned)
```
 
---
 
## Status
 
| Component | Status |
|-----------|--------|
| Proxmox VE | ✅ Running |
| Ubuntu Server VM | 🔄 Setting up |
| Docker | 📅 Next |
| Terraform — Proxmox provider | 📅 Planned |
| K3s Kubernetes cluster | 📅 Planned |
| Prometheus + Grafana | 📅 Planned |
| Loki logging | 📅 Planned |
| Ansible | 📅 Planned |
 
---
 
## Docs
 
| Section | Description |
|---------|-------------|
| [Proxmox](./proxmox/README.md) | Install, config, decisions |
| [Linux](./linux/README.md) | VM setup, what I learned |
| [Docker](./docker/README.md) | Services, compose files |
| [Terraform](./terraform/README.md) | Proxmox + Azure |
| [Kubernetes](./kubernetes/README.md) | K3s cluster |
| [Monitoring](./monitoring/README.md) | Prometheus, Grafana, Loki |
 
---
 
## Mistakes log
 
| Date | What broke | How I fixed it |
|------|-----------|----------------|
| — | Just starting | — |
 
---
 
## Certs I'm working toward
 
AZ-900 ✅ → AZ-104 🔄 → Terraform Associate → AZ-400 → CKA
