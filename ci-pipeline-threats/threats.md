# CI Pipeline Threats

| Threat | Risk | Mitigation | Validation |
| --------- | ------ | ----------- | ----------- |
| Secret Leakage | High | Masked secrets, Gitleaks | CI logs |
| Malicious PR | Medium | Required reviews, branch protection | PR audit |
| Action Tampering | Medium | Pinned versions, least privilege | Workflow audit |
