
CLI
```
argocd app create --name test \
--repo  \
--dest-server https://kubernetes.default.svc \
--dest-namespace marcel --path kubernetes
```

YAML

```
apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: test
  namespace: marcel
spec:
  project: default
  source:
    repoURL: 
    targetRevision: HEAD
    path: argo/example-app
  destination:
    server: https://kubernetes.default.svc
    namespace: marcel
```

