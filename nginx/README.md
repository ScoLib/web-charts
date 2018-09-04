# Nginx



## Configuration

The following table lists the configurable parameters of the Nginx chart and their default values.



| Parameter            | Description                                                  | Default         |
| -------------------- | ------------------------------------------------------------ | --------------- |
| `replicaCount` | Number of replicas | 1     |
| `image.repository` | Nginx Image name | `nginx` |
| `image.tag` | Nginx Image tag | `alpine` |
| `image.pullPolicy` | Image pull policy | `IfNotPresent` |
| `service.type` | Kubernetes Service type | `ClusterIP` |
| `service.httpPort` | Service Http Port | 80 |
| `service.httpsPort` | Service Https Port | 443 |
| `service.httpNodePort` | Service Http NodePort(when `service.type` is `NodePort`) | `nil` |
| `service.httpsNodePort` | Service Https NodePort(when `service.type` is `NodePort`) | `nil` |
| `ingress.enabled`           | If true, Artifactory Ingress will be created | `false` |
| `ingress.annotations`       | Artifactory Ingress annotations     | `{}` |
| `ingress.hosts`             | Artifactory Ingress hostnames       | `[]` |
| `ingress.path`             | Artifactory Ingress path       | `/` |
| `ingress.tls`               | Artifactory Ingress TLS configuration (YAML) | `[]` |
| `persistence.enabled` | Create a volume to application data | true |
| `persistence.size` | Size of persistent volume claim | 8Gi RW |
| `persistence.storageClass` | Type of persistent volume claim | nil |
| `persistence.accessMode` | ReadWriteOnce or ReadOnly | ReadWriteOnce |
| `persistence.existingClaim` | Name of existing persistent volume | `nil` |
| `resources` | CPU/Memory resource requests/limits | Memory: `256Mi`, CPU: `100m` |
| `nodeSelector` | Node labels for pod assignment | `{}` |
| `tolerations` | Toleration labels for pod assignment | `[]` |
| `affinity` | Affinity settings for pod assignment | `{}` |
