# Kubernetes & Terraform

### Install
```sh
brew tap hashicorp/tap
brew install hashicorp/tap/terraform
terraform --version
```

### Azure
```sh
az login
az account set --subscription "66389d29-a9b6-425b-b699-f6894520d87d"
az vm list-sizes --location east_us2
```

### Provision
```sh
terraform init
terraform plan
terraform apply -auto-approve

az aks get-credentials --resource-group rg-owshq-orion-ws-dev --name owshq-orion-ws-dev --overwrite-existing
```

### Destroy
```sh
terraform destroy -auto-approve
```
