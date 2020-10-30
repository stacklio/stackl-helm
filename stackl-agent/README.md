# stackl-agent

![Version: v0.2.5](https://img.shields.io/badge/Version-v0.2.5-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v0.2.5](https://img.shields.io/badge/AppVersion-v0.2.5-informational?style=flat-square)

Stackl description

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"Always"` |  |
| imagePullSecrets | list | `[]` |  |
| log_level | string | `"debug"` |  |
| mode | string | `"prod"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| stacklAgent.agentName | string | `"common"` |  |
| stacklAgent.agentType | string | `"kubernetes"` |  |
| stacklAgent.image | string | `"stacklio/stackl-agent:v0.2.2"` |  |
| stacklAgent.name | string | `"stackl-agent"` |  |
| stacklAgent.redisHost | string | `"stackl-redis"` |  |
| stacklAgent.redisPort | int | `6379` |  |
| stacklAgent.replicaCount | int | `1` |  |
| stacklAgent.secretHandler | string | `"base64"` |  |
| stacklAgent.stacklCliImage | string | `"stacklio/stackl-cli:v0.2.2"` |  |
| stacklAgent.stacklHost | string | `"http://stackl-core:8080"` |  |
| tolerations | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.4.0](https://github.com/norwoodj/helm-docs/releases/v1.4.0)