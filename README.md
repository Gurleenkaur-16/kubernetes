# ☸️ Kubernetes Practice Notes

> A collection of my Kubernetes learning notes, hands-on practice, YAML manifests, and mini projects.
>
> This repository documents my journey of learning Kubernetes from the fundamentals to deploying real-world applications.

---

## 📖 Table of Contents

- 📚 Learning Topics
- 🚀 Cluster Setup
- 📂 Namespaces
- 📦 Pods
- 🚀 Deployments
- 🌐 Services
- ⚙️ ConfigMaps & Secrets
- 💾 Storage
- 🌍 Ingress
- 📦 Helm
- 🔄 Sidecar Containers
- ⏳ Init Containers
- 🛠️ Troubleshooting Commands
- 💻 Practice Projects
- 🎯 Goal

---

# 📚 Learning Topics

✔ Kubernetes Architecture

✔ Kind Cluster

✔ Minikube

✔ Pods

✔ Namespaces

✔ Labels & Selectors

✔ ReplicaSets

✔ Deployments

✔ Services

✔ ConfigMaps

✔ Secrets

✔ Volumes

✔ Persistent Volumes (PV)

✔ Persistent Volume Claims (PVC)

✔ Ingress

✔ Helm

✔ Sidecar Containers

✔ Init Containers

✔ Troubleshooting Kubernetes Applications

---

# 🚀 Cluster Setup

## Create a Kind Cluster

```bash
kind create cluster --name tws-cluster
```

Check Cluster

```bash
kubectl get nodes
```

Delete Cluster

```bash
kind delete cluster --name tws-cluster
```

---

## Start Minikube

```bash
minikube start
```

Check Status

```bash
minikube status
```

---

# 📂 Namespaces

Create Namespace

```bash
kubectl create namespace dev
```

View Namespaces

```bash
kubectl get ns
```

---

# 📦 Pods

Create Pod

```bash
kubectl run nginx --image=nginx
```

View Pods

```bash
kubectl get pods
```

Describe Pod

```bash
kubectl describe pod nginx
```

View Logs

```bash
kubectl logs nginx
```

---

# 🚀 Deployments

Create Deployment

```bash
kubectl apply -f deployment.yml
```

View Deployments

```bash
kubectl get deployments
```

Scale Deployment

```bash
kubectl scale deployment nginx-deployment --replicas=3
```

---

# 🌐 Services

Create Service

```bash
kubectl apply -f service.yml
```

View Services

```bash
kubectl get svc
```

---

# ⚙️ ConfigMaps & Secrets

Create ConfigMap

```bash
kubectl create configmap app-config --from-file=config.properties
```

Create Secret

```bash
kubectl create secret generic app-secret \
--from-literal=password=admin123
```

---

# 💾 Storage

Create Persistent Volume

```bash
kubectl apply -f pv.yml
```

Create Persistent Volume Claim

```bash
kubectl apply -f pvc.yml
```

Check Storage Resources

```bash
kubectl get pv
kubectl get pvc
```

---

# 🌍 Ingress

Enable Ingress

```bash
minikube addons enable ingress
```

Apply Ingress

```bash
kubectl apply -f ingress.yml
```

Check Ingress

```bash
kubectl get ingress
```

---

# 📦 Helm

Create Helm Chart

```bash
helm create my-chart
```

Install Chart

```bash
helm install my-app my-chart
```

View Releases

```bash
helm list
```

Uninstall Release

```bash
helm uninstall my-app
```

---

# 🔄 Sidecar Containers

Deploy Sidecar Container

```bash
kubectl apply -f sidecar-container.yml
```

---

# ⏳ Init Containers

Deploy Init Container

```bash
kubectl apply -f init-container.yml
```

---

# 🛠️ Troubleshooting Commands

Check Cluster

```bash
kubectl get nodes
```

View All Pods

```bash
kubectl get pods -A
```

Describe Pod

```bash
kubectl describe pod <pod-name>
```

View Logs

```bash
kubectl logs <pod-name>
```

Access Running Container

```bash
kubectl exec -it <pod-name> -- sh
```

View Cluster Events

```bash
kubectl get events
```

---

# 💻 Practice Projects

- 🚀 Nginx Application Deployment
- 📝 Notes App Deployment
- 💬 Chat Application Deployment
- 📦 Helm Chart Deployment
- 🌍 Ingress Setup
- 🔄 Multi-Container Pod Practice

---

# 🎯 Goal

Build a strong foundation in Kubernetes through hands-on practice, understand core concepts, deploy containerized applications, manage workloads efficiently, and gain confidence in troubleshooting Kubernetes clusters.

---

## ⭐ If you find this repository useful, don't forget to star it!

Happy Learning! 🚀
