# Installing Grafana with Helm

```bash
# Add Grafana Helm Repository
helm repo add grafana https://grafana.github.io/helm-charts

# Update repo
helm repo update

# Install Grafana
helm install grafana grafana/grafana

# Expose Grafana Service
kubectl expose service grafana --type=NodePort --target-port=3000 --name=grafana-ext
