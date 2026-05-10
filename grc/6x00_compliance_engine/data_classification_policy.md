# MedDefense Data Classification Policy

**Policy number:** SEC-DCP-001
**Effective date:** 2026-05-10
**Review date:** 2027-05-10 (Annual)
**Owner:** IT Security
**Approved by:** CISO

## Purpose and scope
This policy establishes a standardized framework for categorizing and protecting information to ensure compliance with healthcare regulations. It applies to all data created, stored, transmitted, or processed by or on behalf of MedDefense. By defining clear handling requirements for every sensitivity level, we ensure patient safety and organizational security.

## Classification tiers

**Tier 1: Public**
Data approved for release to the general public.
*Examples:* MedDefense public website content, marketing brochures, published clinic hours.

**Tier 2: Internal**
Data for MedDefense employees and authorized contractors only. Unauthorized exposure causes operational inconvenience, not regulatory or patient harm.
*Examples:* Internal company newsletters, cafeteria menus, generic IT onboarding guides.

**Tier 3: Confidential**
Data where exposure could cause financial, legal, or reputational harm. Includes employee records, financial data, contracts, strategic plans, security configurations.
*Examples:* Staff salary reports, vendor service level agreements, network topology maps.

**Tier 4: Restricted / ePHI**
Highly sensitive data subject to the HIPAA Security Rule and Breach Notification Rule. Any unauthorized access triggers the four-factor breach risk assessment.
*Examples:* Patient medical records, laboratory test results, clinical imaging data.

## Handling matrix

| Tier | Storage | Transmission | Internal sharing | External sharing | Disposal |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Tier 1 | Standard network drives | Standard HTTP or SMTP | Standard email | Public website posting | Standard recycle bin |
| Tier 2 | Internal access-controlled SharePoint | SMTP over TLS 1.2 | Internal email only | Not permitted without approval | Standard logical delete |
| Tier 3 | AES-256 encrypted file servers | TLS 1.2 or higher with server certificate verification | Encrypted internal messaging | Secure portal with active NDA | Secure software wiping |
| Tier 4 | AES-256 encrypted databases with strict IAM | TLS 1.2 or higher with server certificate verification | Role-based clinical portals | Encrypted portal with approved BAA | NIST SP 800-88 media sanitization or equivalent for electronic media; secure cross-cut shred for paper |

## Classification responsibility
The data owner or creator classifies data at the time of creation. If the classification level is unclear, the data defaults to Tier 3 until formally reviewed. Only the IT Security department, in consultation with the Data Owner, holds the authority to reclassify data.

## Exceptions process
Exceptions to this policy must be formally granted by the CISO. All exceptions are documented in the IT Security risk register with a valid business justification. The maximum duration before re-review for any exception is 90 days.

## Review cycle
This policy is reviewed annually and following any incident that exposed data handling as a control gap.
