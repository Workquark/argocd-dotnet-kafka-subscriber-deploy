# Argocd Usage and repository settings 
## Argocd - Installation - Usage

- Please refer to :
    - https://argo-cd.readthedocs.io/en/stable/cli_installation/
    - https://argo-cd.readthedocs.io/en/stable/getting_started/#2-download-argo-cd-cli

## Argocd application deploy-

- Production flow is to place CD (continueous delivery code) into a separate repo.
- `argocd app create argocd-dotnet-kafka-subscriber --repo https://github.com/Workquark/argocd-dotnet-kafka-subscriber-deploy.git --path deploy-manifests --dest-server https://1A7D10E99776E7F40B923C80A35E3E70.gr7.eu-west-1.eks.amazonaws.com --dest-namespace argocd-kafka --auth-token <github token or repo token>` 


## For development brance 

- Place the deployment.yaml into the same as the code itself . See - https://github.com/Workquark/argocd-dotnet-kafka-subscriber.git
- For Eg - `argocd app create argocd-dotnet-kafka-subscriber-dev --repo https://github.com/Workquark/argocd-dotnet-kafka-subscriber.git --path Kafka-Subscriber/deploy-manifests --dest-server "https://kubernetes.default.svc"` 