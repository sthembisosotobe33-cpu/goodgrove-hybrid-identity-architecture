# Goodgrove Bank – Hybrid Identity Architecture Overview

## 1. Project Background

Goodgrove Bank is a financial services organisation with 8,000 employees across 12 offices.

The organisation operates a hybrid identity environment consisting of Windows Server 2019 Active Directory Domain Services, Microsoft Entra ID and Microsoft 365.

The existing Active Directory environment contains one forest and three domains.

## 2. Business Challenges

The current identity environment presents several security and operational risks:

- Excessive permanent Global Administrator privileges.
- Overprivileged service accounts.
- Insufficient detection of compromised identities.
- Weak password protection.
- Former contractors retaining active accounts.
- Legacy applications dependent on Kerberos authentication.

## 3. Architecture Goals

The proposed architecture aims to:

- Establish secure hybrid identity integration.
- Centralise cloud identity management through Microsoft Entra ID.
- Reduce standing privileged access.
- Strengthen authentication and access controls.
- Improve identity threat detection and response.
- Introduce identity lifecycle governance.
- Protect existing Kerberos-dependent applications.

## 4. High-Level Architecture

The proposed identity architecture consists of:

1. On-premises Active Directory Domain Services.
2. Microsoft Entra Connect Sync.
3. Microsoft Entra ID.
4. Password Hash Synchronisation.
5. Privileged Identity Management.
6. Conditional Access and multifactor authentication.
7. Microsoft Entra ID Protection.
8. Microsoft Entra Password Protection.
9. Microsoft Entra ID Governance.

## 5. Hybrid Identity Strategy

Active Directory Domain Services will remain the authoritative identity source for synchronised users.

Microsoft Entra Connect Sync will provide identity synchronisation between the three on-premises domains and the Microsoft Entra tenant.

Password Hash Synchronisation is the proposed cloud authentication method.

Legacy applications requiring Kerberos will continue to authenticate against on-premises Active Directory.

## 6. Security Strategy

The architecture will introduce:

- Just-in-time privileged access through PIM.
- Multifactor authentication.
- Conditional Access policies.
- Risk-based identity detection.
- Least-privilege service account management.
- Password protection.
- Access reviews and lifecycle governance.

## 7. Architecture Status

This document describes the proposed target architecture.

Design decisions, implementation activities and validation evidence will be documented separately.

