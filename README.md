# helm-chart-qbittorrent

Helm chart to install [qbittorrent](https://www.qbittorrent.org/)

The qBittorrent project aims to provide an open-source software alternative to µTorrent.

# Introduction

This chart deploys Qbittorrent to your Kubernetes cluster. It's mostly based off the
[docker-compose](https://github.com/linuxserver/docker-qbittorrent?tab=readme-ov-file#docker-compose-recommended-click-here-for-more-info) file
available at [qbittorrent's GitHub repository](https://github.com/linuxserver/docker-qbittorrent).

## Configuration

The following table lists common configurable parameters of the Qbittorrent chart and their recommended values.
See values.yaml for a more complete listing.

| Parameter                               | Description    | Recommended     |
|-----------------------------------------|----------------|--------------|
| <span style="font-family: monospace">image.repository</span>        | Image repository | <span style="font-family: monospace">linuxserver/qbittorrent </span> |
| <span style="font-family: monospace">image.tag</span>               | Image tag | <span style="font-family: monospace">4.6.5-r0-ls334</span> |
| <span style="font-family: monospace">image.pullPolicy</span>        | Image pull policy | <span style="font-family: monospace">IfNotPresent</span> |
| <span style="font-family: monospace">namespace.name</span>          | The namespace to deploy objects | qbittorrent |
| <span style="font-family: monospace">persistence.volumeMounts</span>| VolumeMounts for Qbittorrent | See <span style="font-family: monospace">values.yaml</span> |
| <span style="font-family: monospace">persistence.volumes</span>    | Volumes for Qbittorrent | See <span style="font-family: monospace">values.yaml</span> |
| <span style="font-family: monospace">service.type</span>           | Qbittorrent service type | <span style="font-family: monospace">ClusterIP</span> |
| <span style="font-family: monospace">service.port</span>           | HTTP to expose service | <span style="font-family: monospace">80</span> |
| <span style="font-family: monospace">ingress.enabled</span>        | Enable ingress rules | <span style="font-family: monospace">false</span> |
| <span style="font-family: monospace">ingress.annotations</span>    | Annotations for ingress | <span style="font-family: monospace">{}</span> |
| <span style="font-family: monospace">ingress.host</span>           | Host to respond | See <span style="font-family: monospace">values.yaml</span> |
| <span style="font-family: monospace">ingress.tls.secretName</span> | Ingress TLS secret name | <span style="font-family: monospace">qbittorrent-cert</span> |
| <span style="font-family: monospace">resources.requests.cpu</span> | Doesn't requires lof of cpu | <span style="font-family: monospace">100</span> |
| <span style="font-family: monospace">resources.requests.memory</span> | Doesn't requires lof of memory | <span style="font-family: monospace">256Mi</span> |