# Karmabot

Deploys karmabot https://github.com/kamaln7/karmabot

# Deployment
1. Update karmabot-secret.yaml, replacing the token value with a valid slack token
2. kubectl create namespace sadevs
3. kubectl apply -f karmabot-secret.yaml
4. kubectly apply -f karmabot.yaml
