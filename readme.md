#ArgoCD
## ArgoCD login
- start proxy: kubectl port-forward svc/argocd-server -n argocd 8080:443
- login: `argocd login localhost:8080`

## Add Repo
`argocd repo add https://github.com/davevans/argocd2.git`

