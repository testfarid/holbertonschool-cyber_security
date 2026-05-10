# CloudVault Medical - Vendor Risk Assessment

## Vendor overview
* **Vendor name:** CloudVault Medical
* **Service type:** Cloud Storage and Data Backup
* **Proposed Tier classification:** Tier A (Critical)
* **ePHI processing:** ePHI will be explicitly stored and processed within this environment.

## Findings table

| Item number | Finding | Risk rating | Gap description | Required action |
| :--- | :--- | :--- | :--- | :--- |
| 1 | SOC 2 Type II (11 months) | Pass | N/A | None required. |
| 2 | HITRUST CSF (No) | Acceptable | Vendor lacks HITRUST but satisfies the baseline with a current SOC 2 Type II report. | None required. |
| 3 | Encryption at rest (AES-256) | Pass | N/A | None required. |
| 4 | Encryption in transit (TLS 1.2) | Pass | N/A | None required. |
| 5 | Pen test (22 months ago) | Critical Concern | Policy strictly requires a penetration test within the last 12 months with a remediation summary. 22 months leaves MedDefense blind to recent exploitation paths. | Provide a new penetration test report (< 12 months) and remediation summary. |
| 6 | Sub-processors (US CDN, EU Analytics) | Concern | EU-based data analytics firm introduces international data transfer and sovereignty risks for ePHI. | Vendor must verify if ePHI is processed in the EU and provide BAA flow-down agreements. |
| 7 | Datacenters (DR site undisclosed) | Critical Concern | Failure to disclose the Disaster Recovery site prevents accurate physical security and jurisdictional risk assessment for ePHI. | Disclose the exact geographical location of the DR site handling MedDefense ePHI. |
| 8 | Incident SLA (72 hours) | Critical Concern | Vendor policy (72 hours) directly violates MedDefense policy (24 hours). This delays our HIPAA Breach Notification timeline. | Contractually amend the incident notification SLA to strictly 24 hours. |
| 9 | Data deletion (90 days) | Critical Concern | Vendor policy (90 days) directly violates MedDefense policy (30 days), extending the risk window for compromised dormant data. | Contractually amend the data deletion timeline to occur within 30 days of termination. |
| 10 | Background checks (At hire only) | Acceptable | Standard industry practice, though recurring checks are preferred for Tier A. | None required for onboarding. |
| 11 | MFA (Yes, TOTP) | Pass | N/A | None required. |
| 12 | Vuln management (Quarterly criticals) | Critical Concern | Allowing critical vulnerabilities to remain unpatched for up to 90 days in an ePHI environment is an unacceptable technical risk. | Amend patching SLA to remediate critical vulnerabilities within 14 days maximum. |
| 13 | Right-to-audit (60 days notice) | Concern | 60 days notice is excessively long if a suspected breach requires rapid verification. | Negotiate audit notice period down to 14 days for security incidents. |
| 14 | BAA (Willing to execute) | Pass | N/A | Execute BAA prior to data transfer. |
| 15 | PHI training (Annual online) | Pass | N/A | None required. |

## Critical findings
**Item 5 (Outdated Penetration Test):** The lack of a current penetration test exposes MedDefense to critical technical vulnerabilities. Under HIPAA, relying on two-year-old security validations for ePHI systems is negligent. The vendor must provide a penetration test report dated within the last 12 months, including evidence that all critical findings have been remediated, before any system access is approved.

**Item 7 (Undisclosed DR Site Location):** Failing to identify the disaster recovery site creates immediate regulatory exposure regarding data sovereignty and physical security compliance. MedDefense cannot sign a BAA without knowing exactly where ePHI physically resides. The vendor must formally disclose this location.

**Item 8 (Incident Notification SLA Non-Compliance):** The vendor's 72-hour notification SLA directly violates the MedDefense Vendor Management Policy requiring a 24-hour notification. This gap heavily damages MedDefense's ability to respond to and contain a breach, creating severe financial and regulatory exposure under the HIPAA Breach Notification Rule. The vendor must amend the contract to guarantee a 24-hour notification SLA.

**Item 9 (Data Deletion Non-Compliance):** The vendor's 90-day retention post-termination violates the MedDefense 30-day requirement. Retaining ePHI for an extra 60 days after the business relationship ends creates unnecessary risk of post-contract exposure. The vendor must formally agree to a 30-day certified destruction timeline.

**Item 12 (Unacceptable Vulnerability Remediation SLA):** A quarterly remediation target for critical vulnerabilities means an active exploit could exist for 90 days before patching. This severely violates standard cybersecurity operational expectations. The vendor must contractually commit to patching critical findings within a maximum of 14 days.

## Recommendation
**Approve with Conditions**
The core service architecture (AES-256, TLS 1.2, MFA) and the active SOC 2 Type II report indicate a fundamentally sound security posture. However, the operational SLAs (penetration testing cadence, patching timelines, and incident notification) fall below MedDefense's strict Tier A regulatory requirements. Do not sign the contract until these specific gaps are closed.

## Contract conditions
1. Vendor must provide a penetration test report dated within the last 12 months and evidence that all critical findings identified therein have been remediated, prior to any ePHI access.
2. Vendor must formally disclose the geographic location of all Disaster Recovery facilities storing MedDefense data.
3. Vendor must sign a contractual addendum explicitly agreeing to a 24-hour incident notification SLA.
4. Vendor must sign a contractual addendum explicitly agreeing to certified data destruction within 30 days of contract termination.
5. Vendor must commit in writing to a 14-day maximum remediation SLA for all critical vulnerabilities affecting the MedDefense environment.
