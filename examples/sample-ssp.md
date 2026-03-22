# Sample SSP Extract

## AC-2 Account Management

The platform uses ticket-based provisioning and deprovisioning for workforce accounts.
Managers approve access changes in Jira Service Management. User accounts are reviewed
quarterly by the platform team. Break-glass accounts exist for incident response.

## IA-5 Authenticator Management

Administrators authenticate with SSO and MFA. Workforce users authenticate through
the corporate identity provider, but service accounts still rely on long-lived shared
secrets rotated manually by operators during monthly maintenance.

## AU-6 Audit Review, Analysis, and Reporting

Application and infrastructure logs are aggregated into a centralized logging pipeline.
The on-call engineer reviews alert-driven events daily. A broader manual audit review
of the log backlog occurs weekly and exceptions are tracked in Jira.

## CM-6 Configuration Settings

Terraform modules define baseline infrastructure settings and container hardening.
Golden image configuration is documented in the engineering handbook. Drift detection
is not yet enforced across all production namespaces.

