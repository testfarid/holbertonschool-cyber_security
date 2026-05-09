# NIST CSF 2.0 Gap Assessment: MedDefense Health Systems

**Assessment date:** 2026-05-10
**Assessor:** [Student Name]
**Framework version:** NIST CSF 2.0
**Regulatory context:** HIPAA Security Rule, 45 CFR Part 164

## Gap Assessment Matrix

| CSF Function | Subcategory ID | Subcategory title | Implementation status | Evidence reference | Gap severity | Gap description |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| GOVERN | GV.OC-01 | Org risk strategy established | Partial | riskregisterupdates.yaml | High | Risk register exists but lacks board-approved risk appetite statement, preventing formal strategic alignment |
| GOVERN | GV.PO-01 | Cybersecurity policy established | Not Implemented | No existing artifact | Critical | Complete absence of written AUP or data policy renders controls legally unenforceable during audit |
| GOVERN | GV.SC-04 | Suppliers inventoried by criticality | Not Implemented | Vendor management file missing | High | No formal vendor inventory; unassessed ePHI vendors like CloudVault pose extreme third-party risk |
| GOVERN | GV.SC-07 | Supplier risks in risk register | Not Implemented | riskregisterupdates.yaml | High | Vendor risk is completely omitted from the current risk register, blinding org to supply chain threats |
| IDENTIFY | ID.AM-01 | Asset inventory maintained | Partial | endpoint_hardening_baseline.md | Low | Workstation inventory exists; missing medical devices is a low risk currently due to isolated VLANs |
| IDENTIFY | ID.RA-01 | Vulnerabilities identified and recorded | Implemented | riskregisterupdates.yaml | None | Vulnerability identification clearly evident and documented through recent incident findings |
| IDENTIFY | ID.RA-06 | Risk responses tracked | Partial | implementation_package.md | Medium | Treatment plans exist post-incident, but lack an ongoing tracking cadence for long-term resolution |
| PROTECT | PR.AA-01 | Identity and credential management | Partial | playbookcredentialexposure.yaml | High | IR credential procedures exist, but lack of a proactive IAM program allows severe access risks |
| PROTECT | PR.AA-05 | Access permissions reviewed | Not Implemented | IAM audit logs missing | High | No evidence of periodic access reviews, allowing privilege creep and unauthorized ePHI access |
| PROTECT | PR.AT-01 | Awareness training provided | Not Implemented | HR training portal empty | Critical | No documented security awareness training program exists, leading to high risk of phishing success |
| PROTECT | PR.DS-01 | Data-at-rest protected | Partial | endpoint_hardening_baseline.md | Medium | Endpoints have BitLocker, but cloud database encryption status remains unverified and undocumented |
| PROTECT | PR.PS-01 | Configuration baselines managed | Implemented | endpoint_hardening_baseline.md | None | Hardening baselines are successfully deployed and formally documented |
| PROTECT | PR.PS-04 | Log records generated/managed | Implemented | sigma_detection_rules.yml | None | Sigma rules exist and are active, confirming centralized log collection is functional |
| DETECT | DE.CM-01 | Networks/environments monitored | Partial | sigma_detection_rules.yml | Medium | Sigma rules deployed for monitoring, but the overall scope may be limited to specific subnets |
| DETECT | DE.CM-06 | Malicious code detected | Implemented | sigma_detection_rules.yml | None | Sigma rules explicitly configured for ongoing malware and ransomware detection |
| DETECT | DE.AE-02 | Anomalous activity analyzed | Implemented | forensic_runbook.md | None | Strong forensic capabilities and runbooks exist for analyzing suspected anomalous activity |
| RESPOND | RS.MA-01 | Incident response plan exists | Implemented | ir_playbook.md | None | Formalized IR playbooks are available and have been successfully tested |
| RESPOND | RS.AN-03 | Incidents analyzed/categorized | Implemented | forensic_runbook.md | None | Post-incident forensic runbooks are established and utilized for analysis |
| RESPOND | RS.CO-02 | Internal/external reporting | Partial | ir_playbook.md | Medium | IR playbook handles internal response, but formal external/regulatory reporting policy is unclear |
| RECOVER | RC.RP-01 | Recovery plan exists | Partial | recovery_validation.sh | High | Technical validation script exists, but a comprehensive, organization-wide BCDR plan is missing |
| RECOVER | RC.CO-01 | Recovery communications | Not Implemented | No communication plan found | Medium | Complete lack of documented plans for communicating recovery status to internal and external stakeholders |

## Summary

**Implementation counts:**
- Implemented: 7
- Partial: 8
- Not Implemented: 6

**Top 3 pre-audit priorities:**
1. GV.PO-01 (Critical): Immediate drafting of core security policies (AUP, Data Classification) required.
2. PR.AT-01 (Critical): Implement and document an organization-wide security awareness training program.
3. GV.SC-04 (High): Formalize vendor inventory and execute BAA with CloudVault immediately.

**Connection to upcoming governance work:**
The Critical and High gaps above are not incidental. They represent the exact control areas this project and the projects that follow are designed to close. Technical controls must be supported by formal policies, vendor risk assessments, and structured training programs to satisfy an auditor.
