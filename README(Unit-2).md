# 🧩 UNIT II – Image Building & Container Management (Docker)

---

## 🏗️ Dockerfile Core Concepts

### 📦 Build Context

* The directory sent to the Docker daemon during the build process.
* Includes all files needed to create the image.

### 🚫 .dockerignore

* Used to exclude unnecessary files from the build context.
* Helps reduce image size and speeds up builds.

---

## 📝 Dockerfile Instructions

| Instruction  | Purpose                                        |
| ------------ | ---------------------------------------------- |
| `FROM`       | Specifies the base image                       |
| `RUN`        | Executes commands during build                 |
| `COPY`       | Copies files from host to container            |
| `ADD`        | Copies files + supports extraction             |
| `CMD`        | Default command when container starts          |
| `ENTRYPOINT` | Fixed executable (cannot be overridden easily) |
| `WORKDIR`    | Sets working directory inside container        |
| `ENV`        | Defines environment variables                  |
| `EXPOSE`     | Documents container ports                      |
| `VOLUME`     | Creates persistent storage                     |

---

## ⚙️ Image Creation Process

### 🔨 Build Command

```bash
docker build -t myimage:v1 .
```

### 🚀 Features

* Layer caching (reuses unchanged layers)
* Faster rebuilds
* Efficient image creation

---

## 🏷️ Image Tagging & Versioning

### 📌 Format

```
image:tag
```

### 📌 Example

```
nginx:v1
```

* Tags help manage versions of images.

---

## 🔍 Inspecting Images

```bash
docker history image_name
docker inspect image_name
```

* `history` → shows layers
* `inspect` → detailed metadata

---

## 🌐 Docker Networking

### 🔗 Types of Networks

* **Bridge** (default)
* **Host**
* **Overlay** (multi-host setups)

### 🔌 Port Mapping

```bash
docker run -p 8080:80 nginx
```

👉 Maps:

```
Host:8080 → Container:80
```

---

## 🔗 Linking Containers

* ❌ Old Method: `--link`
* ✅ Modern Method: Custom Docker networks

---

## 💾 Docker Storage

### 📦 Volumes

* Managed by Docker
* Best for production
* Persistent and secure

### 🔗 Bind Mounts

* Linked to host filesystem
* Best for development

---

## 🧠 Copy-on-Write Mechanism

* Base image remains unchanged
* Changes are stored in a separate container layer
* Improves efficiency and storage usage

---

## 📦 Container Registries

* Docker Hub
* GitHub Container Registry (GHCR)
* Private registries

---

## 🔐 Authentication & Access

* Required for private registries
* Uses:

  * Credentials
  * Access tokens

---

## 🧪 Important Docker Commands

### ▶️ Run Container

```bash
docker run -d -p 8080:80 nginx
```

### 📋 List Containers

```bash
docker ps
docker ps -a
```

### 💻 Execute Inside Container

```bash
docker exec -it container_id bash
```

### ❌ Remove Resources

```bash
docker rm container_id
docker rmi image_id
```

---

## ✅ Key Takeaways

* Dockerfile is used to build images
* Images are versioned using tags
* Networking enables container communication
* Volumes provide persistent storage

---

## 🎯 Final Summary

* **Docker** → Core DevOps tool
* **Containers** → Lightweight, fast, portable
* **Images** → Blueprint
* **Containers** → Running instances
* **Networking + Storage** → Production-ready systems

---
