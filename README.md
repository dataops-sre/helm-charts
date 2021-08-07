# Helm-charts
Dataops-sre's public Helm charts repository

## TL;TR
To install charts in this repository with command line:

```bash
helm repo add dataops-sre https://dataops-sre.github.io/helm-charts/
helm repo update
helm install airflow dataops-sre/airflow --wait --timeout 600s
```

with terraform:
```yaml
resource "helm_release" "aiflow" {
  name       = "airflow"
  repository = "https://dataops-sre.github.io/helm-charts/"
  chart      = "airflow"
  namespace  = "default"
}
```