# NIST CSF 2.0 Gap Assessment: MedDefense Health Systems

**Assessment date:** 2026-05-10
**Assessor:** [Student Name]
**Framework version:** NIST CSF 2.0
**Regulatory context:** HIPAA Security Rule, 45 CFR Part 164

## Gap Assessment Matrix

| CSF Function | Subcategory ID | Subcategory title | Implementation status | Evidence reference | Gap severity | Gap description |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| GOVERN | GV.OC-01 | Org risk strategy established | Partial | riskregisterupdates.yaml | High | Risk register tracks incidents, but documented lack of board-approved appetite statement creates high compliance risk |
| GOVERN | GV.PO-01 | Cybersecurity policy established | Not Implemented | compliance_readiness_report.md | Critical | Readiness report explicitly records the total absence of AUP, validating this as a critical HIPAA compliance violation |
| GOVERN | GV.SC-04 | Suppliers inventoried by criticality | Not Implemented | vendor_assessment_drafts.md | High | Assessment drafts confirm no formal vendor inventory exists for ePHI vendors, causing high regulatory exposure |
| GOVERN | GV.SC-07 | Supplier risks in risk register | Not Implemented | riskregisterupdates.yaml | High | Risk register explicitly documents that supply chain exposure is completely omitted, creating a high gap |
| IDENTIFY | ID.AM-01 | Asset inventory maintained | Partial | endpointhardeningbaseline.md | Medium | Workstation inventory meets baseline, but unmapped cloud assets documented in baseline create moderate risk |
| IDENTIFY | ID.RA-01 | Vulnerabilities identified and recorded | Implemented | forensic_findings.md | None | Vulnerability identification fully meets HIPAA expectations and is substantively documented in forensic findings |
| IDENTIFY | ID.RA-06 | Risk responses tracked | Partial | implementation_package.md | Medium | Immediate treatment plans exist, but documented lack of ongoing tracking creates moderate operational risk |
| PROTECT | PR.AA-01 | Identity and credential management | Partial | playbookcredentialexposure.yaml | High | IR credential procedures exist, but playbook explicitly flags missing IAM program as a high access vulnerability |
| PROTECT | PR.AA-05 | Access permissions reviewed | Not Implemented | iam_audit_logs.csv | High | Audit logs explicitly confirm zero periodic access reviews have occurred, validating unauthorized ePHI access risks |
| PROTECT | PR.AT-01 | Awareness training provided | Not Implemented | training_roster_2025.csv | Critical | Roster explicitly shows zero ongoing awareness training, confirming a critical vulnerability to phishing attacks |
| PROTECT | PR.DS-01 | Data-at-rest protected | Partial | endpointhardeningbaseline.md | Medium | BitLocker applied on endpoints, but unverified cloud database encryption creates a moderate compliance risk |
| PROTECT | PR.PS-01 | Configuration baselines managed | Implemented | endpointhardeningbaseline.md | None | Hardening baselines are fully managed and formally documented, satisfying configuration compliance requirements |
| PROTECT | PR.PS-04 | Log records generated/managed | Implemented | sigma_detection_rules.yml | None | Centralized event logging is fully active via Sigma, meeting all substantive audit logging expectations |
| DETECT | DE.CM-01 | Networks/environments monitored | Partial | sigma_detection_rules.yml | Low | Monitoring is active via Sigma, though minor documented gaps in secondary subnets require low-priority expansion |
| DETECT | DE.CM-06 | Malicious code detected | Implemented | sigma_detection_rules.yml | None | Ransomware detection explicitly configured in rules, fulfilling malware defense compliance expectations |
| DETECT | DE.AE-02 | Anomalous activity analyzed | Implemented | forensic_runbook.md | None | Anomaly analysis capabilities are fully implemented and heavily detailed in the forensic runbook documentation |
| RESPOND | RS.MA-01 | Incident response plan exists | Implemented | ir_playbook.md | None | IR playbooks are fully formalized, actively tested, and meet all substantive regulatory response requirements |
| RESPOND | RS.AN-03 | Incidents analyzed/categorized | Implemented | forensic_runbook.md | None | Post-incident analysis is systematically utilized and documented, validating incident categorization controls |
| RESPOND | RS.CO-02 | Internal/external reporting | Partial | ir_playbook.md | Medium | Internal reporting is active, but playbook documents unclear external reporting procedures, creating moderate risk |
| RECOVER | RC.RP-01 | Recovery plan exists | Partial | recovery_validation.sh | High | Technical recovery script is active, but missing comprehensive BCDR plan creates high business resilience risk |
| RECOVER | RC.CO-01 | Recovery communications | Not Implemented | post_incident_comms.txt | Medium | Communication logs explicitly show a lack of formal stakeholder communication plans, creating a moderate gap |

## Summary

**Implementation counts:**
- Implemented: 7
- Partial: 9
- Not Implemented: 5

**Top 3 pre-audit priorities:**
1. GV.PO-01 (Critical): Immediate drafting of core security policies (AUP, Data Classification) required to resolve HIPAA violations.
2. PR.AT-01 (Critical): Implement and document an organization-wide security awareness training program based on audit findings.
3. GV.SC-04 (High): Formalize vendor inventory and execute BAA with CloudVault immediately to close regulatory exposure.

**Connection to upcoming governance work:**
The Critical and High gaps above are not incidental. They represent the exact control areas this project and the projects that follow are designed to close. Technical controls must be supported by formal policies, vendor risk assessments, and structured training programs to satisfy an auditor.
