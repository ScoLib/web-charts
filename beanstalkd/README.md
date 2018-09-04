# PHP-FPM



## Configuration

The following table lists the configurable parameters of the PHP-FPM chart and their default values.



| Parameter            | Description                                                  | Default         |
| -------------------- | ------------------------------------------------------------ | --------------- |
| `replicaCount` | Number of replicas | 1     |
| `image.repository` | PHP-FPM Image name | `schickling/beanstalkd` |
| `image.tag` | PHP-FPM Image tag | `latest` |
| `image.pullPolicy` | Image pull policy | `IfNotPresent` |
| `service.type` | Kubernetes Service type | `ClusterIP` |
| `service.port` | Service Port | 11300 |
| `persistence.enabled` | Create a volume to application data | true |
| `persistence.size` | Size of persistent volume claim | 8Gi RW |
| `persistence.storageClass` | Type of persistent volume claim | nil |
| `persistence.accessMode` | ReadWriteOnce or ReadOnly | ReadWriteOnce |
| `persistence.existingClaim` | Name of existing persistent volume | `nil` |
| `resources` | CPU/Memory resource requests/limits | Memory: `256Mi`, CPU: `100m` |
| `nodeSelector` | Node labels for pod assignment | `{}` |
| `tolerations` | Toleration labels for pod assignment | `[]` |
| `affinity` | Affinity settings for pod assignment | `{}` |



