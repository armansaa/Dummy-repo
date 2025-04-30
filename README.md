# GitOps for nn-id-dev GKE cluster

Directory structure:
```
root
├── deployment
│   ├── <deployment name>               # such as `rumah123portal`, `99idportal`, ...
│   │   ├── <environment>               # such as `develop`, `feature`
│   │   └── ...
│   └── ...
└── flux
    ├── kustomizations
    ├── gitSource
    └── ...
```

# Sealed Secret
```bash
cat secret.yaml | kubeseal --controller-namespace kubeseal --controller-name kubeseal-sealed-secrets --format yaml > sealedconfig.yaml
```