# Kubernetes Threats

| Threat                     | Risk   | Mitigation                            | Validation                 | Detection and Reporting                                                       |
| -------------------------- | ------ | ------------------------------------- | -------------------------- | ----------------------------------------------------------------------------- |
| RBAC Misconfiguration      | High   | Least privilege roles                 | RBAC audit                 | CI security workflows. Periodic access review                                 |
| Malicious Container Images | High   | Image scanning with Trivy             | CI workflow reports        | Daily security scan. Weekly security report. Alert issue on critical findings |
| Lateral Movement           | Medium | Network policies, namespace isolation | Cluster policy enforcement | Cluster policy checks. Manual review                                          |
