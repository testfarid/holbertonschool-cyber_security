# MedDefense Vendor Management Policy

**Policy number:** SEC-VMP-001
**Effective date:** 2026-05-10
**Review date:** 2027-05-10 (Annual)
**Owner:** IT Security and Procurement jointly
**Approved by:** CISO

## Purpose and scope
This policy establishes enforceable security requirements for every third party with access to MedDefense systems or data. It strictly applies to all third parties with access to MedDefense systems, networks, or data: SaaS providers, managed service providers, cloud infrastructure providers, medical device vendors with network-connected products, and staffing agencies with IT system access. By enforcing these rules, we protect patient data and prevent supply chain compromises.

## Vendor risk tiers
Vendors are categorized into three tiers based on access and data exposure:

* **Tier A (Critical):** Vendors with access to ePHI or clinical systems. Examples: scheduling platforms, imaging vendors, backup providers with PHI, Epic integration partners.
* **Tier B (Standard):** Vendors with access to MedDefense internal systems or networks, but not ePHI.
* **Tier C (Low):** Vendors with no system or data access. Physical vendors, office suppliers, facilities contractors.

## Pre-engagement requirements by tier
Tier A vendors must provide all of the following before any data access is permitted:
* SOC 2 Type II report or HITRUST CSF certification, current within 12 months.
* Completed MedDefense vendor security questionnaire.
* Penetration test results dated within 12 months, with a summary of critical findings and remediation status.
* Identification of all sub-processors that will handle MedDefense data, with their jurisdictions.
* An executed Business Associate Agreement before any ePHI access begins, with no exceptions.

## BAA requirements
A Business Associate Agreement (BAA) is unconditionally required for any Tier A vendor; any vendor whose service may incidentally expose ePHI. The BAA requirement is unconditional: no Tier A vendor onboards without an executed BAA. The BAA must include standard minimum required content and a specific incident notification SLA: the vendor must notify MedDefense within 24 hours of a confirmed or suspected security incident affecting MedDefense data.

## Incident notification obligations
Beyond the BAA, the vendor notifies MedDefense within 24 hours of confirmed or suspected breach. Under these obligations, MedDefense retains the right to conduct its own investigation independent of the vendor's.

## Ongoing monitoring
Tier A vendors reviewed annually. Material changes (ownership transfer, new sub-processors, data center relocation, significant security incidents) trigger an immediate out-of-cycle review.

## Vendor offboarding
Upon termination of the relationship, access revoked within 24 hours of contract termination. Vendors must ensure data return or certified destruction within 30 days. All associated risk and engagement documentation retained for six years per HIPAA.
