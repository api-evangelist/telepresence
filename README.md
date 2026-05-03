# Telepresence

Telepresence is a Cloud Native Computing Foundation (CNCF) Sandbox open source tool that enables fast local development for Kubernetes and OpenShift microservices. It creates a bidirectional network bridge between a developer's local machine and a remote Kubernetes cluster, allowing services to run locally while connecting to remote dependencies. Originally created by Ambassador Labs, Telepresence lets developers intercept traffic destined for specific cluster workloads and route it to their local environment for testing and debugging.

**Website:** https://telepresence.io/

**GitHub:** https://github.com/telepresenceio/telepresence

**License:** Apache 2.0

**Governance:** CNCF Sandbox

## Key Features

- Bidirectional networking between local machine and Kubernetes cluster
- Traffic intercept for individual services (global and personal intercepts)
- DNS resolution of cluster services on the local machine
- Sidecar Traffic Agent injection via Traffic Manager
- Works with Kubernetes and OpenShift clusters
- CLI-driven workflow (`telepresence connect`, `telepresence intercept`)

## Architecture

| Component | Location | Description |
|-----------|----------|-------------|
| **Traffic Manager** | Cluster (ambassador namespace) | Central communication hub, manages intercepts |
| **Traffic Agent** | Cluster (sidecar) | Injected into pods to capture and proxy traffic |
| **Daemon** | Local workstation | Manages VPN tunnel and DNS routing locally |

## Links

- [Website](https://telepresence.io/)
- [GitHub Repository](https://github.com/telepresenceio/telepresence)
- [GitHub Organization](https://github.com/telepresenceio)
- [Changelog](https://github.com/telepresenceio/telepresence/blob/main/CHANGELOG.yml)
- [Security](https://github.com/telepresenceio/telepresence/blob/main/SECURITY.md)

## Artifacts

| Artifact | Description |
|----------|-------------|
| [apis.yml](apis.yml) | API catalog index |
| [vocabulary/telepresence-vocabulary.yml](vocabulary/telepresence-vocabulary.yml) | Domain vocabulary |
| [json-ld/telepresence-context.jsonld](json-ld/telepresence-context.jsonld) | JSON-LD context |
