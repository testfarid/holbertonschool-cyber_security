# NIST CSF 2.0 Gap Assessment: MedDefense Health Systems

**Assessment date:** 2026-05-10
**Assessor:** [Student Name]
**Framework version:** NIST CSF 2.0
**Regulatory context:** HIPAA Security Rule, 45 CFR Part 164

## Gap Assessment Matrix

| CSF Function | Subcategory ID | Subcategory title | Implementation status | Evidence reference | Gap severity | Gap description |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| GOVERN | GV.OC-01 | Org risk strategy established | Partial | riskregisterupdates.yaml | High | Risk register exists but officially documents the lack of a board-approved risk appetite statement |
| GOVERN | GV.PO-01 | Cybersecurity policy established | Not Implemented | riskregisterupdates.yaml | Critical | Risk register explicitly documents the complete absence of written AUP, creating a critical organizational risk |
| GOVERN | GV.SC-04 | Suppliers inventoried by criticality | Not Implemented | riskregisterupdates.yaml | High | Risk register findings confirm no formal vendor inventory exists for ePHI vendors like CloudVault |
| GOVERN | GV.SC-07 | Supplier risks in risk register | Not Implemented | riskregisterupdates.yaml | High | Current risk register explicitly omits supply chain and supplier exposure threats |
| IDENTIFY | ID.AM-01 | Asset inventory maintained | Partial | endpoint_hardening_baseline.md | Medium | Baseline covers workstations, but documents a moderate visibility gap regarding cloud assets |
| IDENTIFY | ID.RA-01 | Vulnerabilities identified and recorded | Implemented | riskregisterupdates.yaml | None | Vulnerability identification is fully implemented and evident through incident findings |
| IDENTIFY | ID.RA-06 | Risk responses tracked | Partial | ir_playbooks.md | Medium | IR playbooks track immediate responses, but lack of ongoing tracking creates moderate operational risk |
| PROTECT | PR.AA-01 | Identity and credential management | Partial | playbookcredentialexposure.yaml | High | IR credential procedures exist, but document notes missing proactive IAM program creates high risk |
| PROTECT | PR.AA-05 | Access permissions reviewed | Not Implemented | post-incident forensic report | High | Forensic report confirms unauthorized access occurred specifically due to unreviewed permissions |
| PROTECT | PR.AT-01 | Awareness training provided | Not Implemented | post-incident forensic report | Critical | Forensic report explicitly states users fell for phishing, creating a critical vulnerability |
| PROTECT | PR.DS-01 | Data-at-rest protected | Partial | endpoint_hardening_baseline.md | Medium | Endpoints have BitLocker, but lack of verified cloud database encryption creates moderate risk |
| PROTECT | PR.PS-01 | Configuration baselines managed | Implemented | endpoint_hardening_baseline.md | None | Hardening baselines are successfully deployed, configured, and formally documented |
| PROTECT | PR.PS-04 | Log records generated/managed | Implemented | sigma_detection_rules.yml | None | Sigma rules exist and confirm centralized log collection is active and fully functional |
| DETECT | DE.CM-01 | Networks/environments monitored | Partial | sigma_detection_rules.yml | Medium | Sigma rules deployed for monitoring, but limited subnet scope creates moderate visibility gaps |
| DETECT | DE.CM-06 | Malicious code detected | Implemented | sigma_detection_rules.yml | None | Sigma rules are explicitly configured and active for ongoing malware and ransomware detection |
| DETECT | DE.AE-02 | Anomalous activity analyzed | Implemented | forensic_runbook.md | None | Forensic capabilities fully exist for analyzing suspected anomalous activity accurately |
| RESPOND | RS.MA-01 | Incident response plan exists | Implemented | ir_playbook.md | None | Formalized IR playbooks are available, fully implemented, structurally sound, and tested |
| RESPOND | RS.AN-03 | Incidents analyzed/categorized | Implemented | forensic_runbook.md | None | Post-incident forensic runbooks are established, documented, and consistently utilized |
| RESPOND | RS.CO-02 | Internal/external reporting | Partial | ir_playbook.md | Low | Internal response is dictated, but unclear external reporting policy creates minor compliance friction |
| RECOVER | RC.RP-01 | Recovery plan exists | Partial | recovery_validation.sh | High | Technical script exists, but risk register notes missing comprehensive BCDR plan creates high risk |
| RECOVER | RC.CO-01 | Recovery communications | Not Implemented | ir_playbook.md | Medium | IR playbook completely lacks recovery communication plans for external and internal stakeholders |

## Summary

**Implementation counts:**
- Implemented: 7
- Partial: 8
- Not Implemented: 6

**Top 3 pre-audit priorities:**
1. GV.PO-01 (Critical): Immediate drafting of core security policies (AUP, Data Classification) required.
2. PR.AT-01 (Critical): Implement and document an organization-wide security awareness training program based on forensic findings.
3. GV.SC-04 (High): Formalize vendor inventory and execute BAA with CloudVault immediately.

**Connection to upcoming governance work:**
The Critical and High gaps above are not incidental. They represent the exact control areas this project and the projects that follow are designed to close. Technical controls must be supported by formal policies, vendor risk assessments, and structured training programs to satisfy an auditor.
