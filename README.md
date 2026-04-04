# `sg-gitops` Local POC Skeleton

This folder is the starting point for the SmartGenie GitOps repository structure used in the local Minikube experiment.

## Intended structure
```text
sg-gitops/
├── clusters/
│   └── minikube/
├── base/
│   └── sample-service/
└── environments/
    ├── dev/
    ├── qa/
    ├── preprod/
    └── prod/
```

## Purpose
- `clusters/` -> cluster-level Flux entrypoints
- `base/` -> reusable application manifests
- `environments/` -> environment-specific overlays

## Next action
Use this structure with a test GitHub repo, then bootstrap Flux to it and let Flux reconcile the manifests into Minikube.
