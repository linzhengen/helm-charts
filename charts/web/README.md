# web

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.1.0](https://img.shields.io/badge/AppVersion-0.1.0-informational?style=flat-square)

A web server Helm chart for Kubernetes

## How to install this chart

Add Delivery Hero public chart repo:

```console
helm repo add linzhengen https://linzhengen.github.io/helm-charts
```

A simple install with default values:

```console
helm install linzhengen/web
```

To install the chart with the release name `my-release`:

```console
helm install my-release linzhengen/web
```

To install with some set values:

```console
helm install my-release linzhengen/web --set values_key1=value1 --set values_key2=value2
```

To install with custom values file:

```console
helm install my-release linzhengen/web -f values.yaml
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| containerPort | int | `80` |  |
| env.hogeEnvKey | string | `"hogeEnvValue"` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"nginx"` |  |
| image.tag | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| livenessProbe.path | string | `"/"` |  |
| livenessProbe.port | int | `80` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| readinessProbe.path | string | `"/"` |  |
| readinessProbe.port | int | `80` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |

