# Frontend Threats

| Threat               | Risk   | Mitigation                       | Validation          | Detection and Reporting                                                       |
| -------------------- | ------ | -------------------------------- | ------------------- | ----------------------------------------------------------------------------- |
| XSS Injection        | High   | Input validation, CSP            | CI security jobs    | Daily security scan. Weekly security report. Alert issue on critical findings |
| Dependency Poisoning | Medium | npm audit, SBOM scanning         | CI workflow reports | Daily security scan. Weekly security report. Alert issue on critical findings |
| Source Exposure      | Low    | Branch protection, private repos | GitHub Actions logs | CI security workflows. Repository access audits                               |
