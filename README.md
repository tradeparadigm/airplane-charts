# Airplane Helm Charts

This repository stores helm charts (currently just airplane-agent) and also serves as as a helm
repo.

The helm repo is served via the gh-pages branch, e.g.:

```
helm repo add airplane https://airplanedev.github.io/charts
helm install -f your-values.yaml RELEASE_NAME airplane-agent
```
