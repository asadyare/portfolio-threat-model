# Threat modeling for frontend, CI, and Kubernetes

## Overview

This repository documents threat models and risk analysis for the portfolio platform and Kubernetes workloads. The focus stays on identifying assets, defining trust boundaries, analysing threats, and mapping mitigations directly to CI pipelines and deployment controls.

## Purpose

You use this repository to understand security risks before code reaches production. The documents here guide design decisions, pipeline controls, and runtime protections across the portfolio.

## Scope

- Frontend portfolio application
- Shared CI and security workflows
- Kubernetes clusters and workloads
- Cloudflare edge and DNS layer
- Secrets, credentials, and supply chain inputs

## Assets

- Source code repositories
- CI pipelines and runners
- Container images and registries
- Kubernetes clusters, nodes, and namespaces
- Secrets stored in GitHub and cluster secret stores
- Cloudflare configuration and edge endpoints

## Trust Boundaries

Developer workstation to GitHub
GitHub to CI runners
CI runners to container registry
Registry to Kubernetes cluster
Ingress traffic from Cloudflare to cluster services

Threat Modelling Approach
STRIDE methodology applied per component
Attack surface identification for each boundary
Likelihood and impact scoring using low, medium, high
Mitigation tracking through CI and infrastructure controls

Key Threat Categories

Spoofing
Unauthorised access to GitHub repositories
Compromised CI credentials

Tampering
Malicious code injection through pull requests
Container image modification in registry

Repudiation
Lack of audit logs for pipeline actions
Untracked configuration changes

Information Disclosure
Leaked secrets in source code
Exposed Kubernetes services

Denial of Service
Pipeline abuse through excessive job execution
Ingress flooding against cluster services

Elevation of Privilege
Over permissive GitHub Actions permissions
Misconfigured Kubernetes RBAC

Mitigations Mapped to CI Pipelines

Source Control
Branch protection rules
Required status checks
Mandatory code reviews

CI Security
Reusable security workflows
Secret scanning on pull requests
SAST and dependency scanning
Container image scanning before push

Supply Chain
Pinned action versions
Minimal permissions for workflows
SBOM generation and storage

Kubernetes
Namespace isolation
RBAC with least privilege
Network policies for service access
Admission controls for image validation

Edge and Exposure
HTTPS enforced by Cloudflare
TLS termination and certificate management
Rate limiting at the edge

Risk Tracking
Each threat includes a documented mitigation and validation step. Validation occurs through CI job results, policy enforcement, or runtime configuration checks.

- Directory Structure
- frontend-threats
- kubernetes-threats
- ci-pipeline-threats
- diagrams
- risk-register

## Related Repositories

Frontend Application

1. [Fronteend Application](https://github.com/asadyare/portfolio-frontend)

Shared CI and Security Workflows
2. [CI CD and security pipelines](https://github.com/asadyare/portfolio-ci-cd-security)

Kubernetes Security Projects
3. [Kubernetes Deployment and security](https://github.com/asadyare/portfolio-k8s-microservices-deployment)

## Central Portfolio Reference

Primary portfolio index and documentation
[Central reposittory](https://github.com/asadyare/devsecops-portfolio-asad)

## Contact

You can contact me via [walasaqo@gmail.com](mailto:walasaqo@gmail.com) or connect with me on [LinkedIn](https://www.linkedin.com/in/asad-hassan-20b540313/).

## License

This portfolio is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
