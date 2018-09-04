# PHP-FPM



## Configuration

The following table lists the configurable parameters of the PHP-FPM chart and their default values.



| Parameter            | Description                                                  | Default         |
| -------------------- | ------------------------------------------------------------ | --------------- |
| `replicaCount` | Number of replicas | 3     |
| `image.repository` | PHP-FPM Image name | `klgd/php-fpm72` |
| `image.tag` | PHP-FPM Image tag | `1.0.0` |
| `image.pullPolicy` | Image pull policy | `IfNotPresent` |
| `service.type` | Kubernetes Service type | `ClusterIP` |
| `service.port` | Service Port | 9000 |
| `persistence.enabled` | Create a volume to application data | true |
| `persistence.size` | Size of persistent volume claim | 8Gi RW |
| `persistence.storageClass` | Type of persistent volume claim | nil |
| `persistence.accessMode` | ReadWriteOnce or ReadOnly | ReadWriteOnce |
| `persistence.existingClaim` | Name of existing persistent volume | `nil` |
| `resources` | CPU/Memory resource requests/limits | Memory: `256Mi`, CPU: `100m` |
| `nodeSelector` | Node labels for pod assignment | `{}` |
| `tolerations` | Toleration labels for pod assignment | `[]` |
| `affinity` | Affinity settings for pod assignment | `{}` |



