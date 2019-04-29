# Helm Shared Chart

## Test the Chart

```bash
helm template . -f values.yaml --debug
```

## Package and Deploy

```bash
helm package . --version 1.0.0

az acr helm push shared-chart-1.0.0.tgz --name cdwms --force

az acr helm list --name cdwms

# Optionally, you can then download and use the chart from within helm
az acr helm repo add --name cdwms
helm install cdwms/shared-chart
```