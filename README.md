# helm-charts

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
