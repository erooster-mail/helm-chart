# erooster

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.0.0](https://img.shields.io/badge/AppVersion-0.0.0-informational?style=flat-square)

A Helm chart for the erooster mailserver

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| fullnameOverride | string | `""` | Override the full name of the installed chart. |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.pullSecrets | list | `[]` | Optionally specify an array of imagePullSecrets. Secrets must be manually created in the namespace. ref: https://kubernetes.io/docs/tasks/configure-pod-container/pull-image-private-registry/ |
| image.repository | string | `"mtrnord/erooster"` | Image location to download erooster from |
| image.tag | string | `"main"` | Overrides the image tag whose default is the chart appVersion. |
| ingress.annotations | object | `{}` | Annotations to apply to the created ingress resource. |
| ingress.className | string | `""` | Set the name of the IngressClass cluster resource (optional) |
| ingress.enabled | bool | `false` | Enable the ingress |
| ingress.hosts | list | `[{"host":"chart-example.local","paths":[{"path":"/","pathType":"ImplementationSpecific"}]}]` | Hosts to listen on. |
| ingress.tls | list | `[]` | TLS Secrets for this domain. This is required to match the tls secret for the server itself. |
| mailService.imapEncryptedPort | int | `993` | Port for the imap server (encrypted) |
| mailService.imapPort | int | `143` | Port for the imap server (unencrypted) |
| mailService.smtpEncryptedPort | int | `465` | Port for the smtp server (encrypted) |
| mailService.smtpPort | int | `25` | Port for the smtp server (unencrypted) |
| mailService.type | string | `"Loadbalancer"` | Type of the Mail Service |
| nameOverride | string | `""` | Override part of the installed name, will still keep release name. |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` | Additional annotations for the pods |
| podSecurityContext | object | `{}` | Security context for the pods |
| replicaCount | int | `1` | Amount of replicas. WARNING: Currently erooster doesnt support horizontal scaling properly. |
| resources | object | `{}` | Setup resource limits and requests |
| securityContext | object | `{}` | Security context for the deployment |
| service.httpPort | int | `80` | Port for the http server |
| service.type | string | `"ClusterIP"` | Type of the HTTP Service |
| tolerations | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)
