# Kubernetes Threats

| Threat | Risk | Mitigation | Validation |
| --------- | ------ | ----------- | ------------ |
| RBAC Misconfiguration | High | Least privilege roles | RBAC audit |
| Malicious Container Images | High | Image scanning (Trivy) | CI workflow reports |
| Lateral Movement | Medium | Network policies, namespace isolation | Cluster policy enforcement |
