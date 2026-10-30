# Threat Model

## Scope

This threat model covers the OWASP Juice Shop application, CI/CD pipeline, container infrastructure, Kubernetes manifests and supporting DevSecOps processes.

## Assets

- Source Code
- GitHub Repository
- GitHub Actions Workflows
- Docker Images
- Kubernetes Manifests
- Terraform Configurations

## Threat Actors

### External Attacker

Goals:

- Exploit application vulnerabilities
- Gain unauthorized access
- Execute malicious code

### Malicious Contributor

Goals:

- Introduce vulnerable code
- Bypass security controls
- Manipulate CI/CD processes

### Supply Chain Attacker

Goals:

- Compromise third-party dependencies
- Exploit vulnerable container images

## Attack Surface

- Web Application
- GitHub Actions
- Docker Images
- Dependencies
- Kubernetes Configuration
- Infrastructure as Code

## Security Controls

- Semgrep (SAST)
- OWASP Dependency Check (SCA)
- Trivy (Container Security)
- Checkov (Kubernetes Security)
- Security Gate