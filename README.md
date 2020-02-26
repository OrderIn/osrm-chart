# helm-chart-osrm

[Helm](https://helm.sh/) chart for [OSRM](https://github.com/Project-OSRM/osrm-backend).

Notable features:

- 🗺 Out-of-the-box map management, allowing to download and persist a map by the URI. Supports HTTP(S) download currently,
others (GCS, S3) incoming.
- 🖴 Runs as a StatefulSet so each instance keeps its own maps in PersistentVolume

By default, this chart deploys [osrm-routed](http://project-osrm.org/docs/v5.22.0/api/) server, but you can replace
it with your own implementation (e.g. based on `libosrm`) if you want. 

## Install

```bash
helm repo add hypnoglow https://hypnoglow.github.io/helm-charts

# For Helm v2
helm install hypnoglow/osrm --name osrm

# For Helm v3
helm install osrm hypnoglow/osrm
```
