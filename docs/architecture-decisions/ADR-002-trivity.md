# ADR-002: Container Security Scanning

## Status

Accepted

## Context

Container images must be validated before deployment.

## Decision

Trivy was selected for automated container image scanning.

## Consequences

- CVE detection
- Container hardening visibility
- Integration with GitHub Actions