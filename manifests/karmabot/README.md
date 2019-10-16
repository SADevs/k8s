# Karmabot

Deploys karmabot https://github.com/kamaln7/karmabot

# Missing Pieces
Missing from this deployment is the secret for the slack token. Add a secret in the sadevs namespace called 
`karmabot-secret` with an entry `token` that has a slack token for the bot

This deployment also depends on persistent storage configured as in Andrew Herrington's cluster. This could be replaced
by an external database (See karmabot docs) or other k8s persistent storage.