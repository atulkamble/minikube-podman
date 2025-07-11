# 📄 Minikube with Podman Driver Setup on macOS

Author: `@atulkamble`

---

## 📌 Prerequisites

* macOS (Apple Silicon or Intel)
* [Homebrew](https://brew.sh/) installed
* Internet connectivity

---

## 📥 Install Podman

Official website: [https://podman.io/](https://podman.io/)

```bash
brew install podman
```

---

## 🔧 Initialize Podman Machine

Before using Podman as a driver, initialize the Podman virtual machine:

```bash
podman machine init
```

> ✅ **Tip:**
> If you already have a Podman machine, you can skip this. To check:

```bash
podman machine list
```

---

## 🧹 (Optional) Remove Existing Minikube Setup

If you have an existing Minikube cluster you want to delete:

```bash
minikube delete
```

---

## ▶️ Start Podman Machine

Start the Podman machine so it can act as the container runtime for Minikube:

```bash
podman machine start
```

---

## 📦 Install Minikube

```bash
brew install minikube
```

---

## 🚀 Start Minikube with Podman Driver

```bash
minikube start --driver=podman
```

Check status:

```bash
minikube status
```

---

## 📡 Check Kubernetes Cluster Info

Confirm your cluster is up:

```bash
kubectl cluster-info
```

---

## 📊 Manage Minikube

Stop Minikube:

```bash
minikube stop
```

Delete Minikube cluster:

```bash
minikube delete
```

---

## 📓 Summary

| Command                          | Description                       |
| :------------------------------- | :-------------------------------- |
| `brew install podman`            | Install Podman                    |
| `podman machine init`            | Initialize Podman VM              |
| `podman machine start`           | Start Podman VM                   |
| `brew install minikube`          | Install Minikube                  |
| `minikube start --driver=podman` | Start Minikube with Podman driver |
| `minikube status`                | Check Minikube cluster status     |
| `kubectl cluster-info`           | View cluster details              |
| `minikube stop`                  | Stop Minikube                     |
| `minikube delete`                | Delete Minikube cluster           |

---

✅ Now your **local Kubernetes cluster using Podman as a driver on macOS** is ready for deployments!
