# sadevbot

Deploys SaDevbot to a k8s cluster

# Deployment
1. Update sadevbot-secret.yaml to update the slack token value with a valid slack token
1. kubectl create namespace sadevbot
1. kubectl apply -f sadevbot-secret.yaml
1. kubectl apply -f sadevbot-configmap.yaml
1. kubectl apply -f sadevbot-deployment.yaml

# Operations
## Updating Config
Config is passed to errbot via environment variables. See the errbot-k8s repo 
for more info on config options. If you're adding something totally new, you 
may need to do a PR to config.py in errbot-k8s before adding it to k8s.

Config is setup in sadevbot-configmap.yaml. This allows you to do simple
environment variables as config or more complex data written to files.

1. Add your config to sadevbot-configmap.yaml
1. Add your environment variable or volume mount to sadevbot-deployment.yaml
