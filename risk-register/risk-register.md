# Risk Register

| ID | Area | Risk | Impact | Mitigation | Status | Validation/Evidence |
| ---- | ------ | ------ | -------- | ----------- | -------- | ------------------ |
| R001 | CI Pipeline | Secret leakage | High | Gitleaks, masked secrets | Mitigated | CI logs |
| R002 | Kubernetes | Privilege escalation | High | RBAC least privilege | Mitigated | Cluster audit |
| R003 | Frontend | Dependency vulnerabilities | Medium | npm audit, SBOM | Mitigated | CI workflow report |
| R004 | Frontend | XSS | High | Input validation, CSP | Mitigated | CI SAST |
| R005 | Kubernetes | Malicious container images | High | Trivy scanning, image signing | Mitigated | CI image scan reports |
