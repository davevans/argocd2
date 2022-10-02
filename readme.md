#ArgoCD
## ArgoCD login
- start proxy: `kubectl port-forward svc/argocd-server -n argocd 8080:443`
- login: `argocd login localhost:8080`

## Add Repo
```
argocd repo add https://github.com/davevans/argocd2.git
```

## Create app-of-apps
```
argocd app create apps \
    --dest-namespace argocd \
    --dest-server https://kubernetes.default.svc \
    --repo https://github.com/davevans/argocd2.git \
    --path apps \
    --revision master \
    --sync-policy automated
```
