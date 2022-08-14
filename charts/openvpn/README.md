# openvpn

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.11.0](https://img.shields.io/badge/AppVersion-2.11.0-informational?style=flat-square)

A openvpn Helm chart for Kubernetes

**Homepage:** <https://github.com/linzhengen/helm-charts/tree/main/charts/openvpn>

## How to install this chart

Add Delivery Hero public chart repo:

```console
helm repo add linzhengen https://linzhengen.github.io/helm-charts
```

A simple install with default values:

```console
helm install linzhengen/openvpn
```

To install the chart with the release name `my-release`:

```console
helm install my-release linzhengen/openvpn
```

To install with some set values:

```console
helm install my-release linzhengen/openvpn --set values_key1=value1 --set values_key2=value2
```

To install with custom values file:

```console
helm install my-release linzhengen/openvpn -f values.yaml
```

## Source Code

* <https://github.com/linzhengen/dockerfiles/openvpn>
* <https://github.com/linzhengen/helm-charts/tree/main/charts/openvpn>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` | Affinity labels for pod assignment |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"Always"` | Image pull policy |
| image.repository | string | `"seion/openvpn"` | Image repository |
| image.tag | string | `"2.11.0"` | Image tag |
| imagePullSecrets | list | `[]` | Registry secret names as an array |
| ingress.admin.annotations | object | `{}` | Ingress annotations |
| ingress.admin.enabled | bool | `true` | Enable ingress resource for Admin GUI |
| ingress.admin.hostName | string | `"admin.openvpn.local"` |  |
| ingress.admin.tls.enabled | bool | `true` | Enable TLS configuration for the hostname defined at ingress.admin.hostname parameter |
| ingress.admin.tls.secretName | string | `"admin.openvpn-tls"` |  |
| ingress.gui.annotations | object | `{}` | Ingress annotations |
| ingress.gui.enabled | bool | `true` | Enable ingress resource for Client GUI |
| ingress.gui.hostName | string | `"client.openvpn.local"` |  |
| ingress.gui.tls.enabled | bool | `true` | Enable TLS configuration for the hostname defined at ingress.gui.hostname parameter |
| ingress.gui.tls.secretName | string | `"client.openvpn-tls"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` | Node labels for pod assignment |
| openvpn.admin.password | string | `"pass123"` | Password for the initial super_user |
| openvpn.admin.user | string | `"rootUser"` | Username for the initial super_user. Cannot be `admin` |
| openvpn.config | object | `{"vpn.client.routing.reroute_dns":"false","vpn.client.routing.reroute_gw":"false"}` | Config settings to apply to the openvpn-as server |
| openvpn.ports.admin | int | `943` | Admin GUI port |
| openvpn.ports.gui | int | `944` | Client GUI port |
| openvpn.ports.tcp | int | `9443` | VPN TCP port |
| openvpn.ports.udp | int | `1194` | VPN UDP port |
| openvpn.timezone | string | `"Asia/Tokyo"` |  |
| openvpn.users | list | `nil` | Additional users to create when non-existent `[{"user":"someuser","password":"somepassword"}]` |
| persistence.accessMode | string | `"ReadWriteOnce"` | PVC Access Mode for volume |
| persistence.annotations | object | `{}` | Annotations for the PVC |
| persistence.backupSubpath | string | `"backup"` | Indicate another subpath for backup storage |
| persistence.enabled | bool | `true` | Enable persistence using PVC |
| persistence.existingClaimName | string | `nil` | used when PVC already created before install |
| persistence.licensesSubpath | string | `"licenses"` | Indicate another subpath for licenses storage |
| persistence.size | string | `"8Gi"` | PVC Storage Request for volume |
| persistence.storageClass | string | `nil` | PVC Storage Class for volume |
| podAnnotations | object | `{}` | Map of annotations to add to the pods |
| podSecurityContext.fsGroup | int | `1000` | Group ID for the pod |
| replicaCount | int | `1` |  |
| resources | object | `{}` | CPU/Memory resource requests/limits |
| securityContext | object | `{"capabilities":{"add":["NET_ADMIN"]}}` | Security Context |
| service.admin.type | string | `"ClusterIP"` | Kubernetes Service type for Admin GUI |
| service.gui.type | string | `"ClusterIP"` | Kubernetes Service type for Client GUI |
| service.tcp.enabled | bool | `true` |  |
| service.type | string | `"ClusterIP"` | Kubernetes Service type for VPN, generally this is "LoadBalancer" |
| service.udp.enabled | bool | `true` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` | Create ServiceAccount |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` | Toleration labels for pod assignment |

