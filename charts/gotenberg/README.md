# Gotenberg

---

Gotenberg provides a developer-friendly API to interact with powerful tools like Chromium and LibreOffice for converting numerous document formats (HTML, Markdown, Word, Excel, etc.) into PDF files, and more!

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
helm install gotenberg kqlll/gotenberg
```

---

### Uninstall release
```shell
helm uninstall <Release name>
```

---

### Values

| Key      | Type | Default |
| :----------- | :-----------: | :-------- |
| service.type | string | "ClusterIP" |
| service.port | int | 80 |
| image.pullPolicy | string | "IfNotPresent" |
| image.repository | string | gotenberg/gotenberg |
| image.tag | string | "7.5.0" |
| imagePullSecrets | list | [] |
| ingress.enabled | bool | false |
| autoscaling.enabled| bool | false |
| autoscaling.minReplicas | int | 1 |
| autoscaling.maxReplicas | int | 3 |
| affinity | object | {} |
| resources | object | {} |
| nodeSelector | object | {} |
| tolerations | list | [] |
---

