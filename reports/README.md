# Security Reports

This directory contains security reports and findings generated throughout the DevSecOps pipeline.

## Available Reports

- trivy-findings.md
- checkov-findings.md
- Dependency Check HTML Report (GitHub Artifact)

## Purpose

These reports document the results of automated security controls implemented throughout the CI/CD pipeline.

### Covered Security Controls

- Semgrep (SAST)
- OWASP Dependency Check (SCA)
- Trivy (Container Security)
- Checkov (Kubernetes Security)
- Security Gate Validation

## Notes

OWASP Juice Shop is intentionally vulnerable.

Security findings documented within this directory are expected and demonstrate the effectiveness of automated DevSecOps security controls.