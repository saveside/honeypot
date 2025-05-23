<img src="https://raw.githubusercontent.com/saveside/k8s/refs/heads/main/assets/honey-k8s.png" height="100">

# 🍯 HoneyPot Kubernetes Cluster
*A sweet home for containerized workloads*

Welcome to the **HoneyPot** cluster - where applications buzz with productivity and infrastructure flows as smooth as honey! 🐝

## 🏠 The Hive Architecture

### 🐝 Worker Bees (Cluster Nodes)
| Role      | Hostname     | Location      | OS           | CPU  | RAM  | Machine |
|-----------|--------------|---------------|--------------|------|------|---------|
| Queen  | honeypie     | Hetzner Cloud | Fedora Cloud | Intel Xeon (Skylake) 2x2.10GHz | 4GB  | CX22    |
| Worker | honeybee     | Hetzner Cloud | Fedora Cloud | Intel Xeon (Skylake) 4x2.10GHz | 8GB  | CX32    |

### 🍯 Sweet Applications (The Honey Collection)

#### 🛡️ **Platform Layer** (The Protective Wax)
- **Traefik** - Gateway guardian, routes traffic like a skilled bee
- **cert-manager** - Certificate keeper for secure HTTPS nectar
- **Longhorn** - Persistent storage hives for data
- **Tailscale Operator** - Private tunnel network for the colony

#### 📱 **Productivity Hive**
- **Nextcloud** - File sharing and collaboration sweetness
- **Vaultwarden** - Password vault, as secure as a bee's secret recipe
- **n8n** - Workflow automation, connecting services like pollination
- **Anki Sync** - Self-hosted flashcard learning system

#### 🤖 **AI & Intelligence**
- **Open WebUI** - Beautiful interface for AI interactions

#### 🔍 **Observability & Monitoring**
- **Gatus** - Health checker, monitors the hive's wellness
- **Umami** - Analytics without the sting of privacy invasion

#### 🌐 **Social & Communication**
- **Mastodon** - Decentralized social networking

#### 🧰 **Utilities**
- **Bin** - Minimal pastebin for quick sharing
- **Kubernetes Reflector** - Secret synchronization across namespaces

## 🚀 Getting Started

### Prerequisites
- `kubectl` configured to access your cluster

### Deploy the Entire Hive
```bash
coming soon
