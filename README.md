\# Goodgrove Bank - Hybrid Identity Architecture



\## Project Overview



This project documents the design of a secure hybrid identity architecture for Goodgrove Bank, a financial services organisation with 8,000 employees across 12 offices.



The organisation operates a multi-domain Active Directory environment and uses Microsoft Azure and Microsoft 365.



\## Business Challenges



\- Excessive permanent Global Administrator privileges.

\- Overprivileged service accounts.

\- Insufficient identity threat detection.

\- Weak password protection.

\- Inactive contractor accounts remaining enabled.

\- Legacy applications dependent on Kerberos authentication.



\## Architecture Objectives



\- Design secure hybrid identity integration.

\- Implement Microsoft Entra Connect Sync.

\- Improve privileged identity management.

\- Strengthen authentication and access controls.

\- Improve identity threat detection.

\- Establish identity lifecycle governance.

\- Preserve legacy application compatibility.



\## Proposed Technology



\- Windows Server Active Directory Domain Services

\- Microsoft Entra ID

\- Microsoft Entra Connect Sync

\- Password Hash Synchronisation

\- Microsoft Entra Privileged Identity Management

\- Conditional Access

\- Microsoft Entra ID Protection

\- Microsoft Entra ID Governance



\## Repository Structure



\- `docs/` - Project documentation and architecture decisions.

\- `architecture/` - Architecture diagrams and designs.

\- `implementation/` - Implementation plans and configurations.

\- `evidence/` - Screenshots and validation evidence.



\## Project Status



Architecture design in progress.



This repository distinguishes proposed architecture from features actually implemented and validated.


