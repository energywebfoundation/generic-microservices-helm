# generic-microservice-helm

![Version: 1.3.1](https://img.shields.io/badge/Version-1.3.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.16.0](https://img.shields.io/badge/AppVersion-1.16.0-informational?style=flat-square)

Generic helm chart for Energy Web Foundation microservices

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| EWF DevOps Team | <devops@energyweb.org> |  |

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | common | 2.2.2 |

## Installing the chart

This helm chart is published in [GitHub Packages](https://github.com/features/packages) OCI registry.
Beginning in Helm v3.8.0, OCI support is [enabled by default](https://helm.sh/docs/topics/registries/).

```
helm install oci://ghcr.io/energywebfoundation/generic-microservice-helm --generate-name
```

### Pre-commit hook

Make sure you [install the pre-commit binary](https://pre-commit.com/#install). Then run:

```
pre-commit install
pre-commit install-hooks
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| configFiles | object | `{}` |  |
| configFilesMountPath | string | `"/usr/share/config"` |  |
| container.ports.http | int | `80` |  |
| deploymentStrategy | string | `"RollingUpdate"` |  |
| env | object | `{}` |  |
| envFrom | object | `{}` |  |
| extraLabels | object | `{}` | Extra lables to be added to all resources |
| extraVolumeMounts | list | `[]` |  |
| extraVolumes | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| image.args | list | `[]` |  |
| image.command | list | `[]` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"nginx"` |  |
| image.tag | string | `""` |  |
| image.tty.enabled | bool | `false` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| initContainers | object | `{}` |  |
| livenessProbe.enabled | bool | `false` |  |
| livenessProbe.httpGet.path | string | `"/"` |  |
| livenessProbe.httpGet.port | string | `"http"` |  |
| livenessProbe.httpGet.scheme | string | `"HTTP"` |  |
| livenessProbe.initialDelaySeconds | int | `60` |  |
| livenessProbe.periodSeconds | int | `10` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `10` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| pdb.enabled | bool | `false` |  |
| pdb.minAvailable | int | `1` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| pvc.accessModes | string | `"ReadWriteOnce"` |  |
| pvc.enabled | bool | `false` |  |
| pvc.mountPath | string | `"/tmp"` |  |
| pvc.storage | string | `"20Gi"` |  |
| pvc.storageClassName | string | `"default"` |  |
| readinessProbe.enabled | bool | `false` |  |
| readinessProbe.httpGet.path | string | `"/"` |  |
| readinessProbe.httpGet.port | string | `"http"` |  |
| readinessProbe.httpGet.scheme | string | `"HTTP"` |  |
| readinessProbe.initialDelaySeconds | int | `60` |  |
| readinessProbe.periodSeconds | int | `10` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `10` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| restartPolicy | string | `"Always"` |  |
| sealedSecret.annotations | object | `{}` |  |
| sealedSecret.enabled | bool | `false` |  |
| sealedSecret.encryptedData | object | `{}` |  |
| securityContext | object | `{}` |  |
| service.portName | string | `""` |  |
| service.ports[0].name | string | `"http"` |  |
| service.ports[0].port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| sidecars | list | `[]` |  |
| terminationGracePeriodSeconds | int | `30` |  |
| tolerations | list | `[]` |  |