# Airplane Helm Charts

This repository stores helm charts (currently just airplane-agent) and also serves as as a helm
repo.

Here's an example `values.yaml` for configuring your Airplane agents:
```yaml
airplane:
  # See the docs below for instructions on obtaining your API token and team ID
  apiToken: YOUR_API_TOKEN
  teamID: YOUR_TEAM_ID
  # Change this to run pods in a different namespace
  runNamespace: default
  # Optional: attach labels to agents for constraints
  agentLabels: "orchestration:kubernetes"
  # Optional: if set, only allows agents to execute runs from environment
  # with the provided slug
  envSlug: ""
```

For more details on using the helm chart, see the docs on [self-hosted Airplane agents in Kubernetes](https://docs.airplane.dev/self-hosting/kubernetes).

## Installing the chart ##
Add the Airplane chart repo:
```
helm repo add airplane https://airplanedev.github.io/charts
```
Update your chart repos:
```
helm repo update
```
Install the helm chart:
```
helm install -f values.yaml airplane airplane/airplane-agent
```
