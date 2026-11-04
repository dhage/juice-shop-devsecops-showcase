# Secure Software Development Lifecycle

## Overview

This project follows a Secure SDLC approach by integrating security controls throughout the software delivery lifecycle.

## Development Phase

- Source code management via GitHub
- Pull request validation
- Automated security scanning

## Build Phase

- Docker image creation
- Dependency analysis
- Container security scanning

## Deployment Phase

- Kubernetes manifests
- Infrastructure as Code
- Kubernetes security validation

## Security Controls

| Phase | Control |
|---------|---------|
| Development | Semgrep |
| Build | Dependency Check |
| Containerization | Trivy |
| Deployment | Checkov |
| Governance | Security Gate |