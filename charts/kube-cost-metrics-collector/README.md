OptScale Kubernetes Cost Metrics Collector
====
Ready-to-deploy setup of components necessary for Kubernetes cost management and FinOps in Hystax OptScale.

Components
- [Prometheus](https://github.com/prometheus-community/helm-charts/tree/main/charts/prometheus)
- [kube-state-metrics](https://github.com/kubernetes/kube-state-metrics)
- [kube-service-selectors](https://github.com/hystax/helm-charts/tree/main/charts/kube-service-selectors)

## Prerequisites
Prerequisites are based on dependencies:
- Kubernetes 1.17+
- Helm 3+

## Description
Helm chart for the OptScale Kubernetes Collector project, which is created to collect Kubernetes resources information and share it with OptScale FinOps project - https://hystax.com/optscale/.

## Installation
```bash
helm install kube-cost-metrics-collector hystax/kube-cost-metrics-collector \
--set prometheus.server.dataSourceId=<data-source-id> \
--set prometheus.server.username=<username> \
--set prometheus.server.password=<password> \
--namespace optscale \
--create-namespace
```

## Configuration
The following table lists the commonly used configurable parameters of the Helm chart.

Parameter | Description
--------- | ------------------------------------------------
prometheus.server.dataSourceId | OptScale Kubernetes data source id
prometheus.server.username | username which is used on OptScale Kubernetes data source registration
prometheus.server.password | password which is used on OptScale Kubernetes data source registration

Additional options are in [values.yaml](values.yaml). Alternatively run
```bash
helm show values hystax/kube-cost-metrics-collector
```
