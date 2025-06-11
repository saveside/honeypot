# 🐝 Honeypot — A Honey‑Soaked Kubernetes Cluster

## 🍯 What Is Honeypot?

A honey soaked Kubernetes configuration which provides simplicty and advanced usability with many services and tools

---

## 🐝 Hive Architecture

### Cluster Overview

| Role        | Hostname    | Location         | OS            | CPU              | RAM | Machine   |
|-------------|-------------|------------------|---------------|------------------|-----|-----------|
| Queen       | honeypie    | Hetzner Cloud    | Fedora        | 4×2.10 GHz Xeon  | 8 GB | CX32      |
| Worker Bee  | honeybee    | Hetzner Cloud    | Fedora        | 4×2.10 GHz Xeon  | 8 GB | CX32      |

---

## 🌼 Core Infrastructure — Base Apps

These essential services keep your hive buzzing smoothly:

- **cert‑manager** – TLS certificate automation  
- **Longhorn** – Distributed storage for PVs  
- **MetalLB** – Bare‑metal load balancing  
- **Traefik** – Ingress and reverse proxy  

---

## 🍯 The Honeyplace — Apps

Sweet, useful services that do real work—but quietly entice accidental visitors:

- **Memos** – Lightweight note-taking  
- **Kubernetes Reflector** – Secrets/ConfigMaps sync  
- **Open WebUI** – UI for LLMs  
- **Stirling PDF** – PDF processing tools  
- **Tailscale Operator** – Zero-config VPN  
- **Umami** – Privacy-first web analytics  
- **Bin** – Super-minimal pastebin
-- **n8n** - Automation workflow platform

---

## 🚀 Get Started — Deploy the Hive

### Prerequisites

- `kubectl` access  
- `kustomize` for manifest templating  

### Manual Steps

```sh
# Set up core infrastructure
kubectl apply -k manifests/base/

# Deploy honey applications
kubectl apply -k manifests/apps/n8n/
kubectl apply -k manifests/apps/umami/
```

---

Special thanks to these amazing bee-keepers who inspired this setup: 

     Kreato's K8S Repository: https://github.com/kreatoo/bouquet2/ 
     mt190502's K8S Repository: https://github.com/mt190502/k8s/

---

Happy buzzing! 🐝
