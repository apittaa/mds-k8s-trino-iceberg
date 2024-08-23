# GitOps using ArgoCD

### Install
```sh
brew install helm
brew install argocd
```

### Repo
```sh
helm repo add argo https://argoproj.github.io/argo-helm
```

### Build
```sh
terraform init
terraform apply
```

### Configure
```sh
kubectl patch svc argocd-server -n gitops -p '{"spec": {"type": "LoadBalancer"}}'
kubectl get svc argocd-server -n gitops
kubectl -n gitops get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo


argocd login "" --username admin --password "" --insecure
argocd cluster add ""

kubectl apply -f git-repo-con.yaml -n gitops
```
