# NIST CSF 2.0 Gap Assessment: MedDefense Health Systems

**Assessment date:** 2026-05-10
**Assessor:** [Student Name]
**Framework version:** NIST CSF 2.0
**Regulatory context:** HIPAA Security Rule, 45 CFR Part 164

## Gap Assessment Matrix

| CSF Function | Subcategory ID | Subcategory title | Implementation status | Evidence reference | Gap severity | Gap description |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| GOVERN | GV.OC-01 | Org risk strategy established | Partial | riskregisterupdates.yaml (Post-incident entries) | High | Risk register exists but explicitly documents the lack of a board-approved risk appetite statement |
| GOVERN | GV.PO-01 | Cybersecurity policy established | Not Implemented | None (No AUP document exists) | Critical | No written AUP or data classification policy exists; verbal policy is explicitly not auditable under HIPAA |
| GOVERN | GV.SC-04 | Suppliers inventoried by criticality | Not Implemented | None (No vendor catalog) | High | No formal vendor inventory exists; Nexus, CloudVault, and other ePHI vendors are not catalogued |
| GOVERN | GV.SC-07 | Supplier risks in risk register | Not Implemented | None (No supply chain risks tracked) | High | Vendor risk is not represented in the risk register; supply chain exposure is completely omitted |
| IDENTIFY | ID.AM-01 | Asset inventory maintained | Partial | endpointhardeningbaseline.md (Workstation scope) | Medium | Workstation inventory exists from hardening phase, but missing cloud assets creates a moderate visibility gap |
| IDENTIFY | ID.RA-01 | Vulnerabilities identified and recorded | Implemented | forensic_findings.md (Crimson Tide incident) | None | Vulnerability identification is fully implemented and evident through Crimson Tide incident findings |
| IDENTIFY | ID.RA-06 | Risk responses tracked | Partial | implementation_package.md (Treatment plans) | Medium | Treatment plans exist post-incident, but lack of ongoing tracking creates moderate operational risk |
| PROTECT | PR.AA-01 | Identity and credential management | Partial | playbookcredentialexposure.yaml (IR context only) | High | Credential procedures exist in IR context only; missing proactive IAM program creates high access risks |
| PROTECT | PR.AA-05 | Access permissions reviewed | Not Implemented | None (No IAM audit logs) | High | No evidence of periodic access reviews exists, leading to unauthorized ePHI access risks |
| PROTECT | PR.AT-01 | Awareness training provided | Not Implemented | forensic_findings.md (Crimson Tide incident) | Critical | Forensic findings explicitly state users fell for phishing because no awareness training program is provided |
| PROTECT | PR.DS-01 | Data-at-rest protected | Partial | endpointhardeningbaseline.md (BitLocker logs) | Medium | BitLocker verified on endpoints, but unverified cloud database encryption creates moderate risk |
| PROTECT | PR.PS-01 | Configuration baselines managed | Implemented | endpointhardeningbaseline.md | None | Hardening baselines are successfully deployed, configured, and formally documented |
| PROTECT | PR.PS-04 | Log records generated/managed | Implemented | sigma_detection_rules.yml (Event logging) | None | Sigma rules exist and confirm centralized log collection is fully active and functional |
| DETECT | DE.CM-01 | Networks/environments monitored | Partial | sigma_detection_rules.yml (Subnet scope) | Medium | Sigma rules deployed for monitoring, but limited subnet scope creates moderate visibility gaps |
| DETECT | DE.CM-06 | Malicious code detected | Implemented | sigma_detection_rules.yml (Ransomware rules) | None | Sigma rules are explicitly configured and active for ongoing malware and ransomware detection |
| DETECT | DE.AE-02 | Anomalous activity analyzed | Implemented | forensic_runbook.md (Anomaly analysis) | None | Forensic capabilities fully exist and are documented for analyzing suspected anomalous activity accurately |
| RESPOND | RS.MA-01 | Incident response plan exists | Implemented | ir_playbook.md | None | Formalized IR playbooks are available, fully implemented, structurally sound, and tested |
| RESPOND | RS.AN-03 | Incidents analyzed/categorized | Implemented | forensic_runbook.md | None | Post-incident forensic runbooks are established, documented, and consistently utilized |
| RESPOND | RS.CO-02 | Internal/external reporting | Partial | ir_playbook.md (Internal reporting section) | Low | Internal response is dictated, but unclear external reporting policy creates minor compliance friction |
| RECOVER | RC.RP-01 | Recovery plan exists | Partial | recovery_validation.sh (Technical script) | High | Technical script exists, but missing comprehensive BCDR plan creates high business continuity risk |
| RECOVER | RC.CO-01 | Recovery communications | Not Implemented | None (No recovery comms plan) | Medium | No documented plan exists for communicating recovery status to internal and external stakeholders |

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
