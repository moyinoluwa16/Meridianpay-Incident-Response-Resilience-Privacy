MeridianPay Financial Services: Incident Response, Resilience and Privacy Programme
This group project develops an integrated Governance, Risk, and Compliance (GRC) programme for MeridianPay Financial Services, a Nigerian financial technology company facing cybersecurity, operational resilience, and data privacy challenges. The report proposes an Incident Response Plan, three incident response playbooks, a Business Impact Analysis, a Business Continuity and Disaster Recovery framework, a Crisis Communication Plan, and a Data Protection Impact Assessment (DPIA).
Table of Contents
- Project Overview
- Network Topology
- Tools and Technologies
- Configuration Steps
- Results and Findings
- Author
Project Overview
The purpose of this project is to develop an integrated Incident Response, Business Resilience, and Privacy Programme for MeridianPay Financial Services. The assessment responds to a recent phishing incident involving an employee whose credentials were exposed, resulting in suspicious account activity, possible unauthorized access to customer information, and disruption to payment services.

MeridianPay's operating environment presents significant security and continuity risks:
- Processes approximately 150,000 transactions daily, valued at about ₦2.5 billion.
- Generates approximately ₦18 million in daily revenue.
- Serves approximately 600,000 customers and 9,000 merchants.
- Operates a 24/7 payment platform regulated by the Central Bank of Nigeria (CBN).
- Processes personal data under the Nigeria Data Protection Act 2023 (NDPA).
- Has a four-person security team providing business-hours coverage, despite operating continuously.
- Lacks formal Incident Response, Business Continuity, and Disaster Recovery plans.
- Has inadequate evidence-handling procedures and privacy documentation.
The project addresses five key deliverables:
1. Incident Response Plan (IRP): Develop a formal incident response framework with defined responsibilities, severity classifications, escalation procedures, evidence-handling requirements, and three playbooks covering phishing, ransomware, and personal data breaches.
2. Business Impact Analysis (BIA): Identify critical business activities, assess the impact of service disruptions, establish recovery priorities, and recommend recovery targets.
3. Business Continuity Plan (BCP): Define strategies for maintaining essential banking and payment services during disruptive events.
4. Crisis Communication Plan: Establish communication procedures and templates for customers, merchants, employees, regulators, partner banks, media, and management.
5. Data Protection Impact Assessment (DPIA): Assess privacy risks associated with customer onboarding and Know Your Customer (KYC) verification and recommend appropriate mitigation measures.
The report aligns its proposed framework with relevant industry standards and regulatory requirements, including ISO/IEC 27001, ISO/IEC 27035, ISO 22301, NIST SP 800-61, the NDPA 2023, and applicable CBN requirements.
Network Topology
The report describes MeridianPay's technology and operational environment but does not provide a detailed network topology diagram, specific network device models, IP addresses, subnet configurations, or firewall configurations.

The following infrastructure components and system dependencies are identified:
- Cloud Hosting Platform: Hosts the company's payment platform and supporting services. The report assumes a single cloud provider, while multi-region architecture remains unconfirmed.
- Core Payment Platform: Supports 24/7 wallet transactions and merchant payment processing.
- Merchant Gateway: Processes merchant payments and supports settlement-related activities.
- Customer Onboarding and KYC Systems: Handle customer registration, identity verification, identity documents, facial images, and onboarding risk scores.
- Cloud-Hosted KYC Database and Document Store: Store customer identity and verification information.
- Identity and Access Management (IAM): Supports staff authentication and access to organizational systems.
- Security Monitoring Infrastructure: Includes SIEM, EDR, and fraud-monitoring capabilities referenced in the incident response framework.
- Customer Support Systems: Allow support agents to access customer profiles and respond to enquiries.
- Settlement Infrastructure: Supports transactions and settlement activities with three partner banks.
- Third-Party Services: Include cloud hosting, KYC and identity verification vendors, partner banks, telecommunications, and internet connectivity providers.
- Backup and Recovery Infrastructure: Includes proposed immutable, offline, cross-region backups, replication, and secondary availability zones.
Proposed resilience improvements:
- Multi-availability-zone deployment and warm standby in a second region for Tier 1 services.
- Encrypted, immutable, offline, and cross-region backups.
- Synchronous or near-synchronous replication to a secondary availability zone.
- Asynchronous replication to a second region.
- Dual internet service providers and mobile data fallback.
- Break-glass emergency administrative accounts independent of the primary identity provider.
- Secure out-of-band communication channels for incident response.
Tools and Technologies
The project references the following security technologies, frameworks, systems, and operational resources:
- ISO/IEC 27001:2022: Information Security Management System framework.
- ISO/IEC 27035: Information security incident management.
- ISO 22301: Business Continuity Management System framework.
- ISO/IEC 29134: Privacy Impact Assessment guidance.
- NIST SP 800-61 Rev. 2: Computer security incident handling guidance.
- NIST Cybersecurity Framework: Cybersecurity risk management reference.
- Nigeria Data Protection Act 2023 (NDPA): Personal data protection and breach notification requirements.
- Central Bank of Nigeria (CBN) Requirements: Regulatory expectations for payment service providers and incident reporting.
- PCI DSS: Payment card data security requirements, where applicable.
- Security Information and Event Management (SIEM): Security event monitoring and alerting.
- Endpoint Detection and Response (EDR): Endpoint threat detection and investigation.
- User and Entity Behaviour Analytics (UEBA): Detection of unusual account and data-access behaviour.
- Managed Detection and Response (MDR): Proposed continuous security monitoring and response service.
- Multi-Factor Authentication (MFA): Stronger authentication for staff and privileged accounts.
- Conditional Access: Access restrictions based on defined security conditions.
- Data Loss Prevention (DLP): Protection against unauthorized data disclosure or exfiltration.
- Cryptographic Hashing (SHA-256): Verification of forensic evidence integrity.
- Immutable and Offline Backups: Protection of recovery data against unauthorized modification and ransomware.
- Cloud Replication and Failover: Proposed infrastructure resilience and disaster recovery capabilities.
- Infrastructure as Code: Version-controlled infrastructure templates for rebuilding environments.
- Emergency Contact Sheet and Incident Log: Operational documentation for incident coordination, evidence tracking, and decision recording.
Note: The report identifies these technologies and capabilities as existing references or proposed controls. It does not identify specific commercial software vendors, hardware models, or deployed product configurations.
Configuration Steps
1. Define the Programme Scope and Assessment Method
- Identify the systems and business activities covered by the programme, including wallets, merchant gateway, onboarding and KYC, settlement, customer support, fraud monitoring, cloud infrastructure, and staff systems.
- Establish assumptions requiring management validation, including cloud architecture, staff access restrictions, MFA coverage, and backup recovery capability.
- Align the assessment with ISO/IEC 27001, ISO/IEC 27035, ISO 22301, NIST SP 800-61, NDPA 2023, and applicable CBN requirements.
2. Develop the Incident Response Plan
- Establish document ownership, CEO approval, annual review, and distribution requirements.
- Define incident response objectives covering detection, containment, customer protection, evidence preservation, regulatory compliance, and accountability.
- Establish the Incident Response Team and assign responsibilities to the Incident Commander, Technical Lead, Forensics and Evidence Lead, Privacy Lead/DPO, Compliance Lead, Communications Lead, Operations Lead, Customer Support Lead, Executive Sponsor, and Scribe.
- Develop a RACI matrix to clarify responsibility and accountability for incident response activities.
- Establish an on-call rota with a named Incident Commander and Technical Lead available every day, reachable within 15 minutes.
3. Establish Incident Severity Classification and Escalation Procedures
- Define four incident severity levels:
  - SEV-1 Critical: Major impact on payments, customer funds, or large-scale personal data.
  - SEV-2 High: Significant impact or credible risk of a critical incident.
  - SEV-3 Medium: Limited and contained incident.
  - SEV-4 Low: Minor security event or policy violation.
- Define internal response targets of 15 minutes for SEV-1, 30 minutes for SEV-2, four hours for SEV-3, and the next business day for SEV-4.
- Establish escalation triggers for phishing, compromised credentials, unauthorized customer data access, ransomware, suspected fraud, settlement disruption, and personal data breaches.
- Classify the previous phishing incident at a minimum of SEV-2 until the extent of customer data access is confirmed.
4. Implement the Incident Response Lifecycle
- Preparation: Maintain security tools, logging, backups, contact lists, forensic support, staff training, and exercises.
- Detection and Reporting: Monitor security alerts and provide channels for reporting suspicious activity.
- Analysis and Classification: Validate incidents, identify affected systems and accounts, assess data exposure, and assign severity.
- Containment: Isolate affected hosts, disable compromised accounts, revoke sessions and tokens, and block malicious indicators.
- Eradication: Remove malware and persistence mechanisms, reset credentials, and patch exploited weaknesses.
- Recovery: Restore systems from verified backups, monitor services, and validate transaction integrity and account balances.
- Post-Incident Review: Conduct lessons-learned meetings within five working days and document corrective actions.
5. Establish Evidence Handling and Chain of Custody
- Preserve volatile data, running processes, network connections, disk images, and cloud snapshots where safe.
- Use forensic copies rather than original evidence.
- Verify evidence integrity using SHA-256 cryptographic hashes.
- Maintain an Evidence Register documenting evidence ID, description, source, collector, date and time, hash, and storage location.
- Record every evidence transfer to maintain chain of custody.
- Preserve authentication, VPN, cloud audit, application, email gateway, and EDR logs for at least 12 months.
- Restrict access to evidence repositories and engage external forensic support for critical incidents or potential legal proceedings.
6. Develop Three Incident Response Playbooks
- Playbook A – Phishing and Credential Compromise:
  - Receive and document the phishing report.
  - Preserve the original email, headers, URLs, and screenshots.
  - Disable affected accounts, revoke sessions and tokens, reset credentials, and re-register MFA.
  - Review sign-in logs, mailbox rules, VPN activity, cloud activity, and customer data access.
  - Search for and remove malicious emails and block confirmed indicators.
  - Investigate lateral movement and other affected users.
  - Escalate to the personal data breach playbook if unauthorized customer data access or exfiltration is identified.
  - Restore account access using MFA and least privilege, with heightened monitoring for 30 days.
- Playbook B – Ransomware:
  - Confirm ransomware activity using endpoint and system evidence.
  - Declare SEV-1 and activate the Incident Response Team.
  - Establish secure out-of-band communications.
  - Isolate affected hosts and network segments and protect backup systems.
  - Assess payment processing risks and invoke the BCP where necessary.
  - Preserve memory captures, disk images, ransom notes, wallet addresses, and logs.
  - Investigate the entry point, malware spread, and possible data exfiltration.
  - Rebuild affected systems from known-good images and restore from verified offline or immutable backups.
  - Reconcile transactions and balances before restoring normal operations.
- Playbook C – Personal Data Breach:
  - Contain unauthorized access or disclosure.
  - Open a breach register entry and begin tracking the applicable 72-hour notification period.
  - Identify affected data categories, individuals, systems, and likely consequences.
  - Assess the risk of identity theft, fraud, financial loss, and distress.
  - Determine whether NDPC and data subject notifications are required.
  - Notify affected individuals in plain language where required.
  - Coordinate CBN, partner bank, and other relevant notifications.
  - Consider protective measures such as password and PIN resets and enhanced fraud monitoring.
  - Update the DPIA and Record of Processing Activities following the incident.
7. Conduct the Business Impact Analysis
- Identify critical activities, dependencies, and the consequences of service disruption.
- Assess financial, regulatory and legal, customer and merchant, and reputational impacts at one, four, eight, and 24 hours of downtime.
- Establish Maximum Tolerable Period of Disruption (MTPD), Recovery Time Objectives (RTO), Recovery Point Objectives (RPO), and Minimum Business Continuity Objectives (MBCO).
- Prioritize payment processing, merchant gateway, settlement, fraud monitoring, and identity and access management as critical recovery activities.
- Assess dependencies involving cloud hosting, partner banks, backups, identity providers, security staffing, KYC vendors, and telecommunications.
8. Establish Recovery Targets

   The report proposes the following recovery targets for management approval:
Priority	Critical Activity	MTPD	RTO	RPO
Tier 1	Payment processing and merchant gateway	4 hours	1 hour	5 minutes
Tier 1	Settlement with partner banks	Before next 10:00 cut-off	2 hours and before cut-off	0
Tier 1	Fraud monitoring	4 hours	1 hour	5 minutes
Tier 1	Identity and access management and security monitoring	4 hours	2 hours	15 minutes
Tier 2	Customer support	24 hours	4 hours	1 hour
Tier 2	Corporate email and collaboration	24 hours	4 hours	1 hour
Tier 3	Customer onboarding and KYC	72 hours	8 hours	1 hour
Tier 3	Finance, reconciliation, and reporting	72 hours	24 hours	4 hours

- Validate targets against cloud architecture, backup capabilities, partner bank agreements, and regulatory requirements.
- Confirm that payment processing can meet the proposed five-minute RPO through actual testing.
- Establish a dedicated manual or file-based settlement fallback procedure with partner banks.
9. Develop the Business Continuity Plan
- Define BCP activation criteria, including Tier 1 service disruption beyond 15 minutes, SEV-1 incidents, or SEV-2 incidents threatening recovery targets.
- Assign activation authority to the COO or CEO if the COO is unavailable, based on the advice of the Incident Commander and Operations Lead.
- Establish a Continuity Team comprising Engineering, Operations, Support, Finance, Compliance, Security, HR, and Communications.
- Develop continuity strategies for payment processing, settlement, fraud monitoring, customer support, KYC, security operations, staff availability, premises, connectivity, and suppliers.
- Establish technical disaster recovery requirements covering encrypted backups, quarterly restore tests, replication, infrastructure as code, failover runbooks, break-glass access, and 24/7 monitoring.
- Define the recovery sequence, including service assessment, containment, payment restoration, settlement fallback, customer support restoration, transaction reconciliation, and post-incident review.
10. Develop the Crisis Communication Plan
- Establish communication principles based on speed, accuracy, honesty, consistency, and approved messaging.
- Assign communication responsibilities to the Communications Lead, Executive Sponsor, Legal and Compliance, Privacy Lead, and Customer Support Lead.
- Identify communication channels, including an independently hosted status page, in-app notices, SMS, email, merchant portal, account managers, social media, press statements, and internal messaging.
- Establish an external crisis communication channel for use if corporate email is compromised.
- Define audience-specific communication timelines and update frequencies for employees, customers, merchants, regulators, partner banks, board members, media, law enforcement, insurers, and third-party vendors.
- Establish a message approval workflow: Communications draft, technical and privacy fact-check, legal and compliance review, executive approval, publication, and decision-log recording.
- Develop seven communication templates covering public holding statements, customer service disruptions, personal data breaches, merchant notices, internal staff updates, regulator notifications, and management or board updates.
- Establish customer support procedures requiring approved scripts, identity verification, protection of PINs and OTPs, incident-contact logging, and immediate escalation of suspected account takeovers.
11. Conduct the Data Protection Impact Assessment
- Assess customer onboarding and KYC verification because of the volume and sensitivity of personal information processed.
- Identify data subjects, data categories, sources, recipients, systems, retention periods, and potential cross-border transfers.
- Assess lawful bases, necessity, proportionality, data minimization, transparency, data subject rights, accuracy, and third-party processor arrangements.
- Consult the DPO, Compliance, Security, Engineering, Customer Support, and KYC vendors.
- Identify and score ten privacy risks using likelihood multiplied by severity.
- Prioritize high-risk areas, including compromised staff credentials, excessive internal access, large-scale data exfiltration, and delayed breach detection.
- Define mitigation measures covering MFA, conditional access, role-based access control, masking sensitive fields, encryption, immutable backups, vendor due diligence, retention schedules, privacy notices, cross-border transfer safeguards, and access monitoring.
- Submit the DPIA for DPO and executive review and approval.
12. Establish the Implementation Roadmap
- Immediate (0–14 days): Approve the Incident Response Plan, appoint key incident response roles, investigate the phishing incident, assess NDPC notification obligations, enforce MFA, reset exposed credentials, establish an on-call rota, and engage forensic support.
- 30 days: Conduct the first tabletop exercise, restrict customer support access to sensitive data, improve privacy notices, approve BIA recovery targets, and begin phishing awareness training.
- 60 days: Implement immutable and cross-region backups, conduct the first restore test, deploy MDR or 24/7 monitoring, review vendor agreements, conduct phishing simulations, and enforce DMARC.
- 90 days: Test Tier 1 failover, conduct settlement fallback drills, implement retention schedules, close DPIA actions, and submit the first executive metrics report.
- 6–12 months: Establish a warm standby region, prepare for ISO 27001 certification readiness and PCI DSS review, conduct an internal audit, and maintain the annual programme review cycle.
13. Establish Programme Performance Indicators
- Track mean time to detect (MTTD), mean time to contain (MTTC), and mean time to recover (MTTR).
- Target MTTD below one hour for SEV-1 and SEV-2 incidents.
- Target MTTC below four hours for SEV-1 and SEV-2 incidents.
- Achieve 100% compliance with applicable regulatory notification deadlines.
- Reduce phishing simulation click rates below 5% within six months.
- Achieve 100% MFA coverage across staff accounts.
- Achieve 100% successful Tier 1 restore tests each quarter.
- Complete 100% of high-risk DPIA mitigation actions on schedule.
Results and Findings
The group project produced an integrated framework addressing MeridianPay's cybersecurity incident response, operational resilience, crisis communication, and privacy management requirements.

Key findings and proposed improvements include:
- Incident Response Governance: MeridianPay requires a formally approved Incident Response Plan, clearly assigned incident response roles, defined escalation procedures, and an on-call response structure.
- 24/7 Security Monitoring Gap: The security team operates during business hours while the payment platform runs continuously. An on-call rota and medium-term MDR implementation are recommended.
- Phishing and Credential Risks: The recent incident demonstrates the need for stronger authentication, credential protection, session management, access reviews, and security awareness.
- Evidence Management: Formal evidence registers, forensic copies, cryptographic hashes, chain-of-custody procedures, and secure evidence storage are required to support investigations and regulatory enquiries.
- Business Continuity Risks: Payment processing, merchant gateway services, settlement, fraud monitoring, and identity management require prioritized recovery arrangements.
- Settlement Deadline Exposure: The daily 10:00 a.m. settlement cut-off creates a critical operational dependency. A dedicated manual fallback procedure and partner bank coordination are recommended.
- Unproven Disaster Recovery Capability: Existing backups have not been restore-tested. Immutable backups, cross-region replication, quarterly restore testing, and Tier 1 failover testing are proposed.
- Customer Data Privacy Risks: Customer support agents' reported access to full customer profiles and KYC information without adequate role-based restrictions creates unnecessary exposure.
- DPIA Risk Assessment: Ten privacy risks were identified, with high-priority concerns involving compromised credentials, excessive internal access, large-scale data exfiltration, and delayed breach detection.
- Crisis Communication: Audience-specific communication procedures, approved message templates, defined approval authority, and scheduled updates are recommended to maintain customer and stakeholder confidence.
Major deliverables developed:
- Formal Incident Response Plan with governance, RACI, severity classification, escalation triggers, lifecycle procedures, evidence handling, and notification requirements.
- Three incident response playbooks covering phishing and credential compromise, ransomware, and personal data breaches.
- Business Impact Analysis identifying critical activities, dependencies, impact ratings, and proposed recovery targets.
- Business Continuity Plan with service-specific continuity strategies and technical disaster recovery requirements.
- Crisis Communication Plan with seven communication templates and procedures for internal and external stakeholders.
- Data Protection Impact Assessment for customer onboarding and KYC verification, including ten identified privacy risks and mitigation measures.
- Implementation roadmap covering immediate, 30-day, 60-day, 90-day, and 6–12-month activities.
- Key performance indicators for monitoring programme effectiveness and management accountability.
Overall conclusion:

The project demonstrates the importance of integrating incident response, business continuity, disaster recovery, and privacy management into a coordinated GRC programme. The proposed framework provides MeridianPay with a structured approach to protecting customer funds and information, maintaining essential payment services, meeting regulatory obligations, and improving organizational resilience.

The recommendations remain subject to management approval and validation of assumptions, recovery capabilities, contractual dependencies, and current regulatory requirements. The report is classified as Confidential and was prepared as Version 1.0, Draft for Management Review.
Author
Project: MeridianPay Financial Services – Incident Response, Resilience and Privacy Programme

Project Type: Group Project – GRC Advisory Team

Team: Pod Orion

Prepared for: Folake Adeyemi, Chief Executive Officer, MeridianPay Financial Services

Group Members:
- Adenike 
- Blessing
- Moyinoluwa 
My Contribution: Contributed to the collaborative development of this group project as a member of Pod Orion, the GRC Advisory Team.

Programme: 10alytics GRC June 2026 Cohort

Instructor: Victoria Olyori

Report Date: 26 October 2026

Version: 1.0 – Draft for Management Review

Classification: Confidential

Location: Ottawa, Ontario, Canada
