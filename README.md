# argotest

```
apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: bszeti-app
spec:
  destination:
    namespace: openshift-gitops
    server: 'https://kubernetes.default.svc'
  project: default
  source:
    path: app
    repoURL: 'https://github.com/bszeti/argotest.git'
    targetRevision: mybranch
```