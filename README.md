# Akeyless Kubernetes Authentication Demo

This project demonstrates how to authenticate a Python application within a Kubernetes cluster using an Akeyless Gateway.

## 📂 File Descriptions
| File | Function |
| :--- | :--- |
| get_akeyless_secret.py | Core Python logic with Base64 encoding. |
| serviceaccount.yaml | K8s Identity for the Pod. |
| deployment.yaml | Application Pod management. |
| dockerfile | Containerization config. |

## 🚀 Quick Start Guide

### 1. Build and Push
```bash
docker build -t leon-maister/akeyless-k8s-demo:4.3 .
docker push leon-maister/akeyless-k8s-demo:4.3
```

### 2. Deploy
```bash
kubectl apply -f serviceaccount.yaml
kubectl apply -f deployment.yaml
```

### 3. Logs
```bash
kubectl logs -f deployment/akeyless-kubernetes-authentication-app -n akeyless-kubernetes-authentication-demo
```

---
**Maintained by**: [leon-maister](https://github.com/leon-maister)
