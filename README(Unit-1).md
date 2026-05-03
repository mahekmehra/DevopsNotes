# 📘 Unit I – Basics of DevOps Infrastructure

---

## 🚀 Introduction to Containers
Containers are lightweight environments used to package applications with dependencies.

### Evolution
- Physical Servers → Virtual Machines → Containers
- Containers solve:
  - High resource usage
  - Slow startup
  - Portability issues

### Benefits
- Fast startup (seconds)
- Lightweight (shared OS)
- Scalable
- Ideal for microservices

---

## ⚙️ Container Runtime
Container runtime runs containers from images.

### Types
- High-level: Docker Engine, containerd
- Low-level: runc

### Functions
- Start/stop containers
- Manage lifecycle
- Apply isolation

---

## 🔐 Process Isolation & Namespaces
Namespaces isolate containers.

### Types
- PID → Process isolation
- Network → Separate IP/ports
- Mount → Filesystem isolation
- UTS → Hostname isolation
- User → Security

---

## ⚡ Control Groups (cgroups)
Control resource usage.

### Controls
- CPU
- Memory
- Disk I/O

Prevents one container from consuming all resources.

---

## 📦 Container Images & Layers
- Image = Read-only template
- Built using layers

### Features
- Immutable
- Cached
- Reusable

---

## 🌐 Image Registries
Store and distribute images.

### Types
- Public (Docker Hub)
- Private (Enterprise)

### Benefits
- Version control
- Sharing
- CI/CD integration

---

## 🐳 Introduction to Docker
Docker is a containerization platform.

### Features
- Build → Ship → Run
- Simplifies deployment

---

## 🏗️ Docker Architecture
Components:
- Docker Client
- Docker Daemon
- Images
- Containers
- Registry

---

## 📦 Docker Object Types
- Image → Blueprint
- Container → Running instance
- Network → Communication
- Volume → Storage

---

## 🧱 Docker Layering & Filesystem
- Uses layered filesystem
- Supports copy-on-write

---

## ✅ Key Takeaways
- Containers are lightweight and portable
- Namespaces isolate
- cgroups control resources
- Docker simplifies DevOps workflows