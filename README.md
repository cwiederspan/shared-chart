# Helm Shared Chart

## Package and Deploy

```bash
helm package . --version 1.0.0

az acr helm push shared-chart-1.0.0.tgz --name cdwms

az acr helm list --name cdwms
```