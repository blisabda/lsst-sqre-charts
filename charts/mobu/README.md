# mobu

![Version: 1.5.0](https://img.shields.io/badge/Version-1.5.0-informational?style=flat-square) ![AppVersion: 2.4.0](https://img.shields.io/badge/AppVersion-2.4.0-informational?style=flat-square)

Generate system load by pretending to be a random scientist

**Homepage:** <https://github.com/lsst-sqre/mobu>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| cbanek |  |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` | Affinity rules for the mobu frontend pod |
| autostart | list | `[]` | Autostart specification. Must be a list of mobu flock specifications. Each flock listed will be automatically started when mobu is started. |
| environmentUrl | string | None, must be set | Base URL used to find other services in the environment such as Nublado and TAP |
| fullnameOverride | string | `""` | Override the full name for resources (includes the release name) |
| image.pullPolicy | string | `"IfNotPresent"` | Pull policy for the mobu image |
| image.repository | string | `"lsstsqre/mobu"` | mobu image to use |
| image.tag | string | The appVersion of the chart | Tag of mobu image to use |
| imagePullSecrets | list | `[]` | Secret names to use for all Docker pulls |
| ingress.annotations."nginx.ingress.kubernetes.io/auth-method" | string | `"GET"` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/auth-url" | string | `"http://gafaelfawr.gafaelfawr.svc.cluster.local:8080/auth?scope=exec:admin&auth_type=basic"` |  |
| ingress.enabled | bool | `true` | Whether to create an ingress |
| ingress.host | string | None, must be set if the ingress is enabled | Hostname for the ingress |
| ingress.tls | list | `[]` | Configures TLS for the ingress if needed. If multiple ingresses share the same hostname, only one of them needs a TLS configuration. |
| nameOverride | string | `""` | Override the base name for resources |
| nodeSelector | object | `{}` | Node selector rules for the mobu frontend pod |
| podAnnotations | object | `{}` | Annotations for the mobu frontend pod |
| resources | object | `{}` | Resource limits and requests for the mobu frontend pod |
| tolerations | list | `[]` | Tolerations for the mobu frontend pod |
| vaultSecretsPath | string | None, must be set | Path to the Vault secret containing the Slack alert hook |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)