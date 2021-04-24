# ghcr-auth

![Version: 0.1.2](https://img.shields.io/badge/Version-0.1.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.1.0](https://img.shields.io/badge/AppVersion-0.1.0-informational?style=flat-square)

A ghcr.io registory auth Helm chart for Kubernetes

## How to install this chart

Add Delivery Hero public chart repo:

```console
helm repo add linzhengen https://linzhengen.github.io/helm-charts
```

A simple install with default values:

```console
helm install linzhengen/ghcr-auth
```

To install the chart with the release name `my-release`:

```console
helm install my-release linzhengen/ghcr-auth
```

To install with some set values:

```console
helm install my-release linzhengen/ghcr-auth --set values_key1=value1 --set values_key2=value2
```

To install with custom values file:

```console
helm install my-release linzhengen/ghcr-auth -f values.yaml
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| github.token | string | `""` |  |
| github.userName | string | `""` |  |

