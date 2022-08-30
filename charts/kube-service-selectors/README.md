Helm chart for Kubernetes services selectors exporter
====
Exports Kubernetes services selectors as metrics.

[Source Code](https://github.com/hystax/kube-service-selectors) |  [Docker Image](https://hub.docker.com/r/hystax/kube-service-selectors)

```bash
helm3 install --namespace <namespace> monitoring .
```

#### Configuration
Available options are in [values.yaml](values.yaml). Alternatively run
```bash
helm show values .
```
