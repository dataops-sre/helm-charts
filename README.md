# Helm-charts
Mrmuggymuggy's public helm charts repository

## TL;TR
To install charts in this repository with command line:

```bash
helm repo add mrmuggymuggy https://mrmuggymuggy.github.io/helm-charts/
helm repo update
helm install airflow mrmuggymuggy/airflow --wait --timeout 600s
```

with terraform:
```yaml
resource "helm_release" "aiflow" {
  name       = "airflow"
  repository = "https://mrmuggymuggy.github.io/helm-charts/"
  chart      = "airflow"
  namespace  = "default"
}
```