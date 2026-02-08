# CI Pipeline Threats

| Threat           | Risk   | Mitigation                          | Validation                | Detection and Reporting                                                       |
| ---------------- | ------ | ----------------------------------- | ------------------------- | ----------------------------------------------------------------------------- |
| Secret Leakage   | High   | Masked secrets, Gitleaks scanning   | GitHub Actions logs       | Daily security scan. Weekly security report. Alert issue on critical findings |
| Malicious PR     | Medium | Required reviews, branch protection | PR audit and merge checks | Pull request analysis. CI security workflows                                  |
| Action Tampering | Medium | Pinned versions, least privilege    | Workflow audit logs       | Daily security scan. Weekly security report. Alert issue on critical findings |
