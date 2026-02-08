# Risk Register

| ID   | Area        | Risk                       | Impact | Mitigation                    | Status    | Validation and Evidence | Detection and Reporting                                                       |
| ---- | ----------- | -------------------------- | ------ | ----------------------------- | --------- | ----------------------- | ----------------------------------------------------------------------------- |
| R001 | CI Pipeline | Secret leakage             | High   | Gitleaks, masked secrets      | Mitigated | GitHub Actions logs     | Daily security scan. Weekly security report. Alert issue on critical findings |
| R002 | Kubernetes  | Privilege escalation       | High   | RBAC least privilege          | Mitigated | Cluster audit           | CI security workflows. Periodic access review                                 |
| R003 | Frontend    | Dependency vulnerabilities | Medium | npm audit, SBOM               | Mitigated | CI workflow reports     | Daily security scan. Weekly security report. Alert issue on critical findings |
| R004 | Frontend    | XSS                        | High   | Input validation, CSP         | Mitigated | CI SAST results         | Daily security scan. Weekly security report. Alert issue on critical findings |
| R005 | Kubernetes  | Malicious container images | High   | Trivy scanning, image signing | Mitigated | CI image scan reports   | Daily security scan. Weekly security report. Alert issue on critical findings |
