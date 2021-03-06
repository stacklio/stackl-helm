# stackl

![Version: v0.3.0](https://img.shields.io/badge/Version-v0.3.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v0.3.0](https://img.shields.io/badge/AppVersion-v0.3.0-informational?style=flat-square)

Stackl Helm chart

## Maintainers

| Name    | Email                       | Url                        |
| ------- | --------------------------- | -------------------------- |
| GBrawl  | frederic.vanreet@icloud.com | https://github.com/gbrawl  |
| stgrace | stefgraces@hotmail.com      | https://github.com/stgrace |

## Values

| Key                                 | Type   | Default                                                                                 | Description                                           |
| ----------------------------------- | ------ | --------------------------------------------------------------------------------------- | ----------------------------------------------------- |
| affinity                            | object | `{}`                                                                                    |                                                       |
| datastore.path                      | string | `"/lfs_store"`                                                                          | Datastore path. Only applicable when datastore is LFS |
| datastore.type                      | string | `"Redis"`                                                                               | Datastore type. Options are [Redis, LFS]              |
| fullnameOverride                    | string | `""`                                                                                    |                                                       |
| image.pullPolicy                    | string | `"Always"`                                                                              |                                                       |
| imagePullSecrets                    | list   | `[]`                                                                                    | example imagePullSecrets: [name: pull-secret-name]    |
| log_level                           | string | `"debug"`                                                                               |                                                       |
| mode                                | string | `"prod"`                                                                                |                                                       |
| nameOverride                        | string | `""`                                                                                    |                                                       |
| nodeSelector                        | object | `{}`                                                                                    |                                                       |
| stacklCore.image                    | string | `"stacklio/stackl-core:v0.3.0"`                                                         | Stackl-core image                                     |
| stacklCore.ingress.annotations      | string | `nil`                                                                                   | Ingress annotation                                    |
| stacklCore.ingress.enabled          | bool   | `true`                                                                                  | Enable ingress creation                               |
| stacklCore.ingress.hostname         | string | `"stackl.example.com"`                                                                  | Ingress hostname                                      |
| stacklCore.ingress.tls              | string | `nil`                                                                                   |                                                       |
| stacklCore.ingressRoute.annotations | object | `{}`                                                                                    | Ingress route annotations                             |
| stacklCore.ingressRoute.enabled     | bool   | `false`                                                                                 | Enable ingress route creation                         |
| stacklCore.ingressRoute.host        | string | `"stackl.example.com"`                                                                  | Ingress route hostname                                |
| stacklCore.ingressRoute.tls         | object | `{"secretName":"stackl"}`                                                               | Ingress route TLS configuration                       |
| stacklCore.name                     | string | `"stackl-core"`                                                                         | Stackl core name                                      |
| stacklCore.replicaCount             | int    | `1`                                                                                     | Stackl core replicas                                  |
| stacklCore.resources                | object | `{"limits":{"cpu":"300m","memory":"256Mi"},"requests":{"cpu":"200m","memory":"256Mi"}}` | Stackl resource limits and requests                   |
| stacklCore.resources.limits         | object | `{"cpu":"300m","memory":"256Mi"}`                                                       | Stackl resource limits                                |
| stacklCore.resources.requests       | object | `{"cpu":"200m","memory":"256Mi"}`                                                       | Stackl resource requests                              |
| stacklCore.serviceType              | string | `"NodePort"`                                                                            | Stackl core service type                              |
| stacklOpa.image                     | string | `"stacklio/opa:v0.21.1"`                                                                | Stackl OPA image                                      |
| stacklOpa.ingress.annotations       | string | `nil`                                                                                   | Ingress annotation                                    |
| stacklOpa.ingress.enabled           | bool   | `true`                                                                                  | Enable ingress route creation                         |
| stacklOpa.ingress.hostname          | string | `"opa.example.com"`                                                                     | Ingress hostname                                      |
| stacklOpa.ingress.tls               | string | `nil`                                                                                   |                                                       |
| stacklOpa.ingressRoute.annotations  | object | `{}`                                                                                    | Ingress route annotations                             |
| stacklOpa.ingressRoute.enabled      | bool   | `false`                                                                                 | Enable ingress route creation                         |
| stacklOpa.ingressRoute.host         | string | `"opa.example.com"`                                                                     | Ingress route hostname                                |
| stacklOpa.ingressRoute.tls          | string | `nil`                                                                                   | Ingress route TLS configuration                       |
| stacklOpa.name                      | string | `"stackl-opa"`                                                                          | Stackl OPA deployment name                            |
| stacklOpa.replicaCount              | int    | `1`                                                                                     | Stackl OPA replicas                                   |
| stacklRedis.image                   | string | `"stacklio/redis:v5.0.3"`                                                               | Stackl redis image                                    |
| stacklRedis.name                    | string | `"stackl-redis"`                                                                        | Stackl redis deployment name                          |
| stacklRedis.replicaCount            | int    | `1`                                                                                     | Stackl redis replicas                                 |
| stacklRedis.securityContext         | object | `{}`                                                                                    | Security context for Stackl-Redis                     |
| storage.nfs.enabled                 | bool   | `false`                                                                                 | Use NFS                                               |
| storage.nfs.path                    | string | `nil`                                                                                   | NFS path                                              |
| storage.nfs.server                  | string | `nil`                                                                                   | NFS server                                            |
| storage.nfs.subPath                 | string | `nil`                                                                                   | Subpath for the volume mount                          |
| storage.pvc.size                    | string | `"1Gi"`                                                                                 | PVC size                                              |
| storage.pvc.storageClassName        | string | `nil`                                                                                   | StorageClassName for PVC                              |
| tolerations                         | list   | `[]`                                                                                    |                                                       |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.4.0](https://github.com/norwoodj/helm-docs/releases/v1.4.0)
