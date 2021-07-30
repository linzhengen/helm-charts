# helm-charts
[![Helm docs](https://github.com/linzhengen/helm-charts/actions/workflows/helm-docs.yml/badge.svg)](https://github.com/linzhengen/helm-charts/actions/workflows/helm-docs.yml)
[![Lint and Test Charts](https://github.com/linzhengen/helm-charts/actions/workflows/lint-test.yaml/badge.svg)](https://github.com/linzhengen/helm-charts/actions/workflows/lint-test.yaml)
[![Release Charts](https://github.com/linzhengen/helm-charts/actions/workflows/release.yaml/badge.svg)](https://github.com/linzhengen/helm-charts/actions/workflows/release.yaml)
## TLDR

```console
helm repo add linzhengen https://linzhengen.github.io/helm-charts
helm search repo linzhengen
helm install my-release linzhengen/<chart>
```

## Chart list
[![Artifact HUB](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/linzhengen)](https://artifacthub.io/packages/search?repo=linzhengen)

- [cronjob](https://artifacthub.io/packages/helm/linzhengen/cronjob)
- [ghcr-auth](https://artifacthub.io/packages/helm/linzhengen/ghcr-auth)
- [web](https://artifacthub.io/packages/helm/linzhengen/web)

### Running CI tests locally
`helm-docs`:

  To generate chart `README.md` files from the [template](ci/README.md.gotmpl):

  ```console
  docker run --rm -v "$PWD:/helm-docs" jnorwood/helm-docs:v1.5.0 --template-files ./ci/README.md.gotmpl
  ```
