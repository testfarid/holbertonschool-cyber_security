# NIST CSF 2.0 Gap Assessment: MedDefense Health Systems

**Assessment date:** 2026-05-10
**Assessor:** [Student Name]
**Framework version:** NIST CSF 2.0
**Regulatory context:** HIPAA Security Rule, 45 CFR Part 164

## Gap Assessment Matrix

| CSF Function | Subcategory ID | Subcategory title | Implementation status | Evidence reference | Gap severity | Gap description |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| GOVERN | GV.OC-01 | Org risk strategy established | Partial | riskregisterupdates.yaml | High | Risk register exists and is updated post-incident; no board-approved risk appetite statement |
| GOVERN | GV.PO-01 | Cybersecurity policy established | Not Implemented | None | Critical | No written AUP or data classification policy; verbal policy is not auditable |
| GOVERN | GV.SC-04 | Suppliers inventoried by criticality | Not Implemented | None | High | No formal vendor inventory; Nexus, CloudVault, and other ePHI-adjacent vendors are not tiered or catalogued |
| GOVERN | GV.SC-07 | Supplier risks in risk register | Not Implemented | None | High | Vendor risk not represented in the risk register; supply chain exposure identified in incident not yet formalized |
| IDENTIFY | ID.AM-01 | Asset inventory maintained | Partial | endpoint_hardening_baseline.md | Medium | Workstation inventory exists, but missing cloud assets creates a moderate visibility gap |
| IDENTIFY | ID.RA-01 | Vulnerabilities identified and recorded | Implemented | riskregisterupdates.yaml | None | Vulnerability identification is fully implemented and evident through incident findings |
| IDENTIFY | ID.RA-06 | Risk responses tracked | Partial | implementation_package.md | Medium | Treatment plans exist post-incident, but lack of ongoing tracking creates a moderate operational risk |
| PROTECT | PR.AA-01 | Identity and credential management | Partial | playbookcredentialexposure.yaml | High | IR credential procedures exist, but missing proactive IAM program creates high access risks |
| PROTECT | PR.AA-05 | Access permissions reviewed | Partial | ad_users_export.csv | Medium | Initial access is controlled, but missing periodic review cycles creates moderate privilege creep risks |
| PROTECT | PR.AT-01 | Awareness training provided | Not Implemented | None | Critical | Complete lack of awareness training creates a critical vulnerability to social engineering attacks |
| PROTECT | PR.DS-01 | Data-at-rest protected | Partial | endpoint_hardening_baseline.md | Medium | Endpoints have BitLocker, but unverified cloud database encryption creates moderate data exposure risk |
| PROTECT | PR.PS-01 | Configuration baselines managed | Implemented | endpoint_hardening_baseline.md | None | Hardening baselines are successfully deployed and formally documented |
| PROTECT | PR.PS-04 | Log records generated/managed | Implemented | sigma_detection_rules.yml | None | Sigma rules exist and confirm centralized log collection is fully functional |
| DETECT | DE.CM-01 | Networks/environments monitored | Partial | sigma_detection_rules.yml | Medium | Sigma rules deployed for monitoring, but limited subnet scope creates moderate visibility gaps |
| DETECT | DE.CM-06 | Malicious code detected | Implemented | sigma_detection_rules.yml | None | Sigma rules are explicitly configured for ongoing malware and ransomware detection |
| DETECT | DE.AE-02 | Anomalous activity analyzed | Implemented | forensic_runbook.md | None | Forensic capabilities fully exist for analyzing suspected anomalous activity |
| RESPOND | RS.MA-01 | Incident response plan exists | Implemented | ir_playbook.md | None | Formalized IR playbooks are available, fully implemented, and tested |
| RESPOND | RS.AN-03 | Incidents analyzed/categorized | Implemented | forensic_runbook.md | None | Post-incident forensic runbooks are established and consistently utilized |
| RESPOND | RS.CO-02 | Internal/external reporting | Partial | ir_playbook.md | Low | Internal response is dictated, but unclear external reporting policy creates minor compliance friction |
| RECOVER | RC.RP-01 | Recovery plan exists | Partial | recovery_validation.sh | High | Technical script exists, but missing comprehensive BCDR plan creates high business continuity risk |
| RECOVER | RC.CO-01 | Recovery communications | Partial | slack_ir_channel_logs.txt | Low | Ad-hoc communication exists, but lack of formal stakeholder communication plan is a minor gap |

## Summary

**Implementation counts:**
- Implemented: 7
- Partial: 10
- Not Implemented: 4

**Top 3 pre-audit priorities:**
1. GV.PO-01 (Critical): Immediate drafting of core security policies (AUP, Data Classification) required.
2. PR.AT-01 (Critical): Implement and document an organization-wide security awareness training program.
3. GV.SC-04 (High): Formalize vendor inventory and execute BAA with CloudVault immediately.

**Connection to upcoming governance work:**
The Critical and High gaps above are not incidental. They represent the exact control areas this project and the projects that follow are designed to close. Technical controls must be supported by formal policies, vendor risk assessments, and structured training programs to satisfy an auditor.
