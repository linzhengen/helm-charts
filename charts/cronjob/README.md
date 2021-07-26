# cronjob

![Version: 0.1.3](https://img.shields.io/badge/Version-0.1.3-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.1.0](https://img.shields.io/badge/AppVersion-0.1.0-informational?style=flat-square)

A CronJob Helm chart for Kubernetes

## How to install this chart

Add Delivery Hero public chart repo:

```console
helm repo add linzhengen https://linzhengen.github.io/helm-charts
```

A simple install with default values:

```console
helm install linzhengen/cronjob
```

To install the chart with the release name `my-release`:

```console
helm install my-release linzhengen/cronjob
```

To install with some set values:

```console
helm install my-release linzhengen/cronjob --set values_key1=value1 --set values_key2=value2
```

To install with custom values file:

```console
helm install my-release linzhengen/cronjob -f values.yaml
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| annotations | object | `{}` |  |
| args[0] | string | `"-c"` |  |
| args[1] | string | `"echo $(date)"` |  |
| command[0] | string | `"/bin/sh"` |  |
| concurrencyPolicy | string | `"Forbid"` |  |
| env | list | `[]` |  |
| failedJobsHistoryLimit | int | `5` |  |
| image.imagePullPolicy | string | `"Always"` |  |
| image.imagePullSecret | string | `""` |  |
| image.repository | string | `"busybox"` |  |
| image.tag | string | `"latest"` |  |
| nodeSelector | object | `{}` |  |
| resources | object | `{}` |  |
| restartPolicy | string | `"Never"` |  |
| schedule | string | `"*/15 * * * *"` |  |
| securityContext | object | `{}` |  |
| startingDeadlineSeconds | int | `240` |  |
| successfulJobsHistoryLimit | int | `3` |  |
| tolerations | list | `[]` |  |

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| linzhengen |  |  |
