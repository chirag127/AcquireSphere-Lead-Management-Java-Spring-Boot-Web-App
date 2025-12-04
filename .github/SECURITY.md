# Security Policy for AcquireSphere-Lead-Management-Java-Spring-Boot-Web-App

As an Apex Technical Authority project, we treat security with the highest priority, adhering to Zero-Defect principles and current 2026 security hardening standards for enterprise Java applications.

## Supported Versions

This project uses **Java 17 LTS** and **Spring Boot 3.x**. We actively maintain and patch the main branch (`main`). Security updates for older, unmaintained branches are not guaranteed.

## Reporting a Vulnerability

We welcome responsible disclosure of security vulnerabilities. To maintain operational integrity and protect our users, please follow these steps:

1.  **Do Not Create a Public Issue:** Reporting vulnerabilities via public GitHub Issues is strictly prohibited to prevent exposure to malicious actors.
2.  **Contact Securely:** Please email our dedicated security team immediately at: `security+acuiresphere@[your-organization-domain].com`. (Replace `[your-organization-domain].com` with the appropriate domain for the project owner, `chirag127`).
3.  **Provide Details:** In your email, please include:
    *   A clear, step-by-step description of how to reproduce the vulnerability.
    *   The affected component(s) (e.g., specific REST endpoint, data validation layer).
    *   The potential impact of the vulnerability.

## Our Response Policy

Upon receiving a report, we commit to the following timeline:

1.  **Acknowledgement:** We will acknowledge receipt of your report within **48 hours**.
2.  **Triage & Analysis:** We will triage the issue severity within **5 business days**.
3.  **Remediation:** We aim to deploy a security patch to a private branch within **14 days** for high-severity issues.
4.  **Disclosure:** Following successful patch deployment and confirmation, we will coordinate a public disclosure timeline with the reporter, adhering to responsible disclosure best practices.

## Security Practices & Hardening (2026 Standard)

This Spring Boot backend is designed with the following security controls in place:

*   **Input Validation:** Comprehensive validation enforced on all API inputs using Bean Validation (JSR 380) and service-layer checks.
*   **Data Access:** Strict adherence to JPA/Hibernate best practices to prevent SQL Injection (e.g., parameterized queries).
*   **Authentication/Authorization:** Uses Spring Security configured for OAuth 2.0/JWT token validation. Hardcoded credentials are **FORBIDDEN**.
*   **Dependency Management:** Regular scans are performed using GitHub Dependabot (and/or OWASP Dependency-Check) integrated into our `ci.yml` workflow. Critical CVEs will trigger immediate pipeline failure.
*   **Secrets Management:** Environment variables and external secret stores (e.g., Vault/AWS Secrets Manager) are mandatory for production deployments. **No secrets stored in Git.**

## Development Environment Security

Developers must adhere to the following standards when working on this repository:

*   **Static Analysis:** All code must pass checks enforced by Ruff (if Python context applies) or SonarQube integration (Java context), configured to flag common OWASP Top 10 risks.
*   **Testing:** Integration tests must include negative test cases targeting common exploits (e.g., boundary testing, malicious input).

For more information on development standards, please consult our contributing guidelines:

[CONTRIBUTING.md](./CONTRIBUTING.md)