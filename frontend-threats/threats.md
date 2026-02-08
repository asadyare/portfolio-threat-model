# Frontend Threats

| Threat | Risk | Mitigation | Validation |
| --------- | ------- | ------------- | -------------- |
| XSS Injection | High | Input validation, CSP | CI security jobs |
| Dependency Poisoning | Medium | npm audit, SBOM scanning | CI workflow reports |
| Source Exposure | Low | Branch protection, private repos | GitHub actions logs |
