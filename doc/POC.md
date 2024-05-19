# Install ArgoCD
```bash
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

# Access The ArgoCD API Server
```bash
kubectl port-forward svc/argocd-server -n argocd 8080:443
```

# Get secret to the admin user
```bash
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
```

# Install ArgoCD CLI
https://argo-cd.readthedocs.io/en/stable/cli_installation/

# DEMO
[![asciicast](https://asciinema.org/a/660081.svg)](https://asciinema.org/a/660081)
