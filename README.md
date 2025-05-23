# 🍯 HoneyPot Kubernetes Cluster
*A sweet home for containerized workloads*

Welcome to the **HoneyPot** cluster - where applications buzz with productivity and infrastructure flows as smooth as honey!

## 🏠 The Hive Architecture

### Worker Bees (Cluster Nodes)
| Role      | Hostname     | Location      | OS           | CPU  | RAM  | Machine |
|-----------|--------------|---------------|--------------|------|------|---------|
| Queen     | honeypie     | Hetzner Cloud | Fedora Cloud | Intel Xeon (Skylake) 2x2.10GHz | 4GB  | CX22    |
| Worker    | honeybee     | Hetzner Cloud | Fedora Cloud | Intel Xeon (Skylake) 4x2.10GHz | 8GB  | CX32    |

## 🏗️ Base Infrastructure (The Heart)

Essential services that keep the hive running smoothly:

- **ArgoCD** - GitOps operator managing all deployments with pre/post configurations
- **cert-manager** - Automatic TLS certificate management and wildcard certificates  
- **Longhorn** - Distributed storage system for persistent volumes
- **MetalLB** - Load balancer for bare metal Kubernetes clusters
- **Traefik** - Reverse proxy and ingress controller

## 🍯 Sweet Applications (The Honeys)

### Productivity & Knowledge
- **Anki Sync** - Self-hosted spaced repetition flashcards
- **Memos** - Lightweight note-taking and knowledge base
- **Nextcloud** - File sharing, calendar, and collaboration platform

### Security & Access
- **Vaultwarden** - Self-hosted Bitwarden compatible password manager
- **OAuth2 Proxy** - Authentication proxy for applications
- **Kubernetes Reflector** - Secret and ConfigMap synchronization

### AI & Modern Tools
- **Open WebUI** - Beautiful interface for AI language models
- **Stirling PDF** - Powerful PDF manipulation tools

### Networking & Connectivity
- **Tailscale Operator** - Zero-config VPN with subnet routing

### Monitoring & Observability
- **Prometheus** - Metrics collection and monitoring
- **Gatus** - Service health monitoring and status page
- **Umami** - Privacy-focused web analytics

### Utilities
- **Bin** - Minimal pastebin for quick text sharing

## 🚀 Getting Started

### Prerequisites
- `kubectl` configured to access your cluster
- `kustomize` for manifest management
- ArgoCD for GitOps deployment management

### Deploy the Cluster
```bash
# Deploy base infrastructure first
kubectl apply -k hive/base/

# Deploy specific applications manually if needed
kubectl apply -k hive/honeys/nextcloud/
kubectl apply -k hive/honeys/vaultwarden/
kubectl apply -k hive/honeys/memos/
```

### 📁 Repository Structure
```
honeypot-k8s/
├── hive/
│   ├── base/                    # Core infrastructure
│   │   ├── argocd/             # GitOps operator (pre/post config)
│   │   ├── cert-manager/       # Certificate management (pre/post)
│   │   ├── longhorn/           # Storage system
│   │   ├── metallb/            # Load balancer
│   │   └── traefik/            # Ingress controller
│   └── honeys/                 # Sweet applications
│       ├── anki-sync/          # Flashcard system
│       ├── bin/                # Pastebin utility
│       ├── gatus/              # Health monitoring
│       ├── kubernetes-reflector/ # Secret sync
│       ├── memos/              # Note-taking
│       ├── nextcloud/          # File sharing
│       ├── oauth2-proxy/       # Authentication
│       ├── open-webui/         # AI interface
│       ├── prometheus/         # Metrics
│       ├── stirling-pdf/       # PDF tools
│       ├── tailscale-operator/ # VPN
│       ├── umami/              # Analytics
│       └── vaultwarden/        # Password manager
└── README.md
```
### 🙏 Acknowledgments 

Special thanks to these amazing bee-keepers who inspired this setup: 

     Kreato's K8S Repository: https://github.com/kreatoo/bouquet2/ 
     mt190502's K8S Repository: https://github.com/mt190502/k8s/ 
---
"Like bees creating honey, this cluster transforms simple containers into sweet, productive applications" 
