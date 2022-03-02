# The chart for Modsecurity-crs

---
## Modsecurity-crs
The Official OWASP Core Rule Set Docker Image (ModSecurity+Core Rule Set)

---

### Installing the Chart

---

Before the chart can be installed the repo needs to be added to Helm, run the following commands to add the repo.
```shell
helm repo add kqlll https://raw.githubusercontent.com/KqLLL/helm-charts/main
helm repo update
```
The installation command example is as below.
```shell
helm install owasp-modsecurity kqlll/owasp-modsecurity
```

---

### Uninstall release
```shell
helm uninstall owasp-modsecurity
```

---

### Values

| Key      | Type | Default |
| :----------- | :-----------: | :-------- |
| service.type | string | "ClusterIP" |
| serverApp    | string | "nginx"     |
| service.port | int | 80 |
| image.pullPolicy | string | "IfNotPresent" |
| image.repository | string | owasp/modsecurity-crs |
| image.tag | string | "" |
| imagePullSecrets | list | [] |
| autoscaling.enabled| bool | false |
| autoscaling.minReplicas | int | 1 |
| autoscaling.maxReplicas | int | 3 |
| affinity | object | {} |
| resources | object | {} |
| nodeSelector | object | {} |
| tolerations | list | [] |
---

