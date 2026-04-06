# `sg-gitops`

GitOps repository for the SmartGenie local and multi-environment Flux experiments.

## Structure
```text
sg-gitops/
├── clusters/
│   └── minikube/
├── apps/
│   └── base/
└── environments/
    ├── dev/
    ├── qa/
    ├── preprod/
    └── prod/
```

## Purpose
- `clusters/` -> cluster-level Flux entrypoints and Git sources
- `apps/base/` -> shared `HelmRelease` definitions for SmartGenie services
- `environments/` -> environment-specific overlays and namespace scoping

## Current model
- Flux syncs this repo
- the app deployments are defined as `HelmRelease` resources
- the charts come from the separate repo `sg-helm-charts`
- each environment overlays the same services with env-specific values

