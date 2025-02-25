---
layout: page
title: "Security Incident Response Procedure"
permalink: /procedures/isms-proc-03/
---

**Document ID**: ISMS-PROC-03  
**Version**: 1.0  
**Last Updated**: February 25, 2025  
**Owner**: Chief Technology Officer  
**Approved by**: Board of Directors

## 1. Purpose and Scope

### 1.1 Purpose

This Security Incident Response Procedure provides structured guidance for effectively detecting, responding to, and recovering from security incidents affecting Enablis and its clients. It enables prompt and consistent incident handling while minimizing business impact.

### 1.2 Scope

This procedure applies to:

- All security incidents affecting Enablis systems, data, or services
- All employees, contractors, and temporary staff of Enablis
- Client environments and data managed by Enablis
- Third-party services used by Enablis
- All locations from which Enablis business is conducted

## 2. Incident Response Team

### 2.1 Team Structure

The Incident Response Team (IRT) consists of core and extended members:

**Core Team Members**:

- Security Manager (Incident Response Manager)
- IT Operations Manager
- Senior Security Analyst
- System Administrator

**Extended Team Members** (engaged as needed):

- Chief Technology Officer
- Legal representative
- Human Resources representative
- Client Account Manager
- External security specialists
- Communications representative

### 2.2 Roles and Responsibilities

#### 2.2.1 Security Manager (Incident Response Manager)

- Oversees incident response activities
- Declares incident classifications
- Coordinates the response team
- Makes critical response decisions
- Approves external communications
- Reports to senior management

#### 2.2.2 IT Operations Manager

- Coordinates technical response resources
- Implements containment measures
- Oversees recovery activities
- Ensures service continuity
- Manages operational aspects of the response

#### 2.2.3 Senior Security Analyst

- Performs technical investigation
- Analyzes incident evidence
- Identifies attack vectors and impacts
- Recommends containment and remediation steps
- Documents technical findings

#### 2.2.4 System Administrator

- Implements technical response actions
- Collects system logs and evidence
- Applies emergency fixes and configurations
- Restores affected systems
- Documents technical response actions

#### 2.2.5 Extended Team Member Responsibilities

- **CTO**: Strategic oversight and executive decisions
- **Legal**: Legal advice and regulatory notification requirements
- **HR**: Personnel-related aspects of incidents
- **Account Manager**: Client communication and coordination
- **External Specialists**: Specialized technical expertise
- **Communications**: Internal and external communications support

## 3. Incident Classification

### 3.1 Incident Categories

Security incidents are categorized by type:

| Category               | Description                                  | Examples                                                                                                                  |
| ---------------------- | -------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **Data Breach**        | Unauthorized access to or disclosure of data | - Unauthorized data exfiltration<br>- Accidental data exposure<br>- Loss of data storage containing sensitive information |
| **Malware**            | Systems affected by malicious software       | - Virus or worm infection<br>- Ransomware attack<br>- Trojan or backdoor installation                                     |
| **Account Compromise** | Unauthorized access to accounts              | - Credential theft<br>- Account takeover<br>- Privilege escalation                                                        |
| **Denial of Service**  | Disruption of service availability           | - DDoS attack<br>- Application resource exhaustion<br>- Network flooding                                                  |
| **System Intrusion**   | Unauthorized access to systems               | - Server compromise<br>- Database intrusion<br>- Network penetration                                                      |
| **Social Engineering** | Manipulation of people to gain access        | - Phishing attempts<br>- Pretexting attacks<br>- Business email compromise                                                |
| **Physical Security**  | Physical security breaches                   | - Unauthorized facility access<br>- Theft of equipment<br>- Physical tampering                                            |

### 3.2 Severity Levels

Incidents are classified by severity to determine response urgency:

| Severity     | Description                                               | Response Time                     | Examples                                                                                                                     |
| ------------ | --------------------------------------------------------- | --------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| **Critical** | Severe impact on critical systems with wide-scale effects | Immediate response (24/7)         | - Widespread ransomware attack<br>- Major data breach of client data<br>- Complete outage of critical services               |
| **High**     | Significant impact with limited scope                     | Response within 2 hours           | - Localized malware infection<br>- Compromise of administrator account<br>- Breach of sensitive internal data                |
| **Medium**   | Limited impact on non-critical systems                    | Response within 8 business hours  | - Isolated system compromise<br>- Unauthorized access to non-sensitive data<br>- Suspicious activity requiring investigation |
| **Low**      | Minimal impact with no immediate effect                   | Response within 24 business hours | - Unsuccessful intrusion attempts<br>- Minor policy violations<br>- Low-risk vulnerabilities                                 |

## 4. Incident Response Process

### 4.1 Detection and Reporting

#### 4.1.1 Detection Sources

Security incidents may be detected through:

- Security monitoring systems and alerts
- Automated detection tools
- System and application logs
- Staff observations
- Client reports
- Third-party notifications
- Threat intelligence feeds

#### 4.1.2 Reporting Procedure

Any person who discovers a potential security incident must:

1. **For Critical or High severity potential incidents**:

   - Immediately contact the Security Manager by phone
   - If unavailable, contact the IT Operations Manager
   - Follow up with an email to security@enablis.co

2. **For Medium or Low severity potential incidents**:

   - Email security@enablis.co with details
   - Include "Security Incident" in the subject line
   - Provide as much information as possible

3. **Information to include**:
   - Description of the incident
   - Systems or data potentially affected
   - Date and time of discovery
   - Any actions already taken
   - Contact information of the reporter

#### 4.1.3 Initial Documentation

Upon receiving a report, the Security Manager will:

- Create an incident record in the incident management system
- Assign an incident ID
- Record initial details and reporter information
- Perform preliminary classification
- Initiate response activities based on severity

### 4.2 Assessment and Triage

#### 4.2.1 Initial Assessment

The Incident Response Manager will:

1. Verify if the reported event is a security incident
2. Gather preliminary information
3. Determine the incident category and severity
4. Identify systems and data potentially affected
5. Estimate business impact
6. Activate appropriate response team members

#### 4.2.2 Triage Actions

Based on severity, take immediate actions:

**Critical and High Severity**:

- Activate the core Incident Response Team
- Notify the CTO
- Initiate emergency response procedures
- Begin immediate containment actions
- Establish an incident command center (physical or virtual)

**Medium Severity**:

- Notify relevant technical team members
- Begin investigation within defined timeframe
- Plan containment approach
- Assess need for additional resources

**Low Severity**:

- Assign to appropriate technical staff
- Schedule investigation
- Document in incident management system
- Monitor for escalation

#### 4.2.3 Escalation

Escalate incidents when:

- Impact is greater than initially assessed
- Additional resources are required
- Executive decisions are needed
- Client impact is identified
- Regulatory or legal implications arise

Escalation path: Security Manager → IT Operations Manager → CTO → CEO

### 4.3 Containment

#### 4.3.1 Immediate Containment

Take immediate actions to limit damage:

- Isolate affected systems
- Block malicious network traffic
- Disable compromised accounts
- Place temporary security controls
- Preserve evidence

#### 4.3.2 Containment Strategy

Develop a containment strategy considering:

- Potential damage if containment is delayed
- Business impact of containment actions
- Resource requirements
- Evidence preservation needs
- Effectiveness of containment options

#### 4.3.3 Evidence Collection

Collect and preserve evidence:

- System logs
- Network traffic captures
- Memory dumps where appropriate
- Disk images when necessary
- Screenshots and documentation
- Chain of custody records for critical incidents

### 4.4 Investigation

#### 4.4.1 Investigation Activities

Conduct a thorough investigation:

- Determine the attack vector and entry point
- Identify compromised systems and accounts
- Determine what actions were taken by the attacker
- Assess data access or exfiltration
- Establish a timeline of events
- Identify exploited vulnerabilities
- Document findings throughout the process

#### 4.4.2 Client Impact Assessment

For incidents affecting client environments:

- Identify affected clients
- Determine specific client data or systems impacted
- Assess breach notification requirements
- Document client-specific findings
- Prepare client communication

#### 4.4.3 Forensic Investigation

For significant incidents, perform forensic activities:

- Engage specialists if required
- Follow forensic best practices
- Maintain chain of custody
- Document all forensic activities
- Preserve evidence for potential legal proceedings

### 4.5 Eradication

#### 4.5.1 Eradication Planning

Develop a plan to remove the threat:

- Identify all malicious components
- Plan removal of malware and artifacts
- Address vulnerabilities that were exploited
- Reset compromised credentials
- Develop restoration approach
- Document eradication steps

#### 4.5.2 Eradication Activities

Execute the eradication plan:

- Remove malware and unauthorized modifications
- Patch or mitigate exploited vulnerabilities
- Delete or disable compromised accounts
- Remove unauthorized access methods
- Conduct security scans to verify eradication
- Document all actions taken

#### 4.5.3 Validation

Verify successful eradication:

- Conduct vulnerability scans
- Review system integrity
- Perform penetration testing if appropriate
- Monitor for signs of persistent access
- Validate security controls

### 4.6 Recovery

#### 4.6.1 Recovery Planning

Plan the return to normal operations:

- Prioritize systems for restoration
- Determine recovery sequence
- Establish verification testing
- Define monitoring requirements
- Develop back-out procedures if issues occur

#### 4.6.2 Recovery Implementation

Restore systems to normal operation:

- Restore from clean backups where necessary
- Rebuild systems if required
- Reset and restore credentials
- Implement additional security controls
- Return systems to production
- Document all recovery actions

#### 4.6.3 Post-Recovery Monitoring

After recovery, implement enhanced monitoring:

- Monitor for signs of recurrence
- Implement additional logging if needed
- Conduct regular security checks
- Verify system performance
- Document monitoring results

### 4.7 Post-Incident Activities

#### 4.7.1 Post-Incident Review

Conduct a post-incident review meeting:

- Include all response team members
- Review the incident timeline
- Evaluate response effectiveness
- Identify improvement opportunities
- Document lessons learned
- Develop action items

#### 4.7.2 Documentation Finalization

Complete incident documentation:

- Finalize the incident report
- Include technical details and timeline
- Document business impact
- Record response actions and decisions
- Identify root causes
- Include recommendations

#### 4.7.3 Improvements Implementation

Implement security improvements:

- Address identified vulnerabilities
- Enhance detection capabilities
- Update response procedures if needed
- Provide additional training if required
- Improve preventive controls
- Track implementation of improvements

## 5. Communication Plan

### 5.1 Internal Communication

#### 5.1.1 Management Notification

Notify management based on severity:

- **Critical**: Immediate notification to CTO and CEO
- **High**: Notification to CTO within 2 hours
- **Medium**: Notification to relevant department heads
- **Low**: Include in regular security reporting

#### 5.1.2 Staff Communication

Communicate with staff as appropriate:

- Provide need-to-know information
- Communicate required actions
- Share security awareness lessons
- Maintain confidentiality of sensitive details
- Use secure communication channels

### 5.2 External Communication

#### 5.2.1 Client Communication

For incidents affecting clients:

1. Prepare client communication in coordination with account managers
2. Obtain approval from the Incident Response Manager
3. Ensure accuracy and appropriate level of detail
4. Provide clear information about impact and actions
5. Include point of contact for questions
6. Maintain ongoing communication as needed

#### 5.2.2 Regulatory Notification

If regulatory notification is required:

1. Consult with legal representative
2. Identify specific regulatory requirements
3. Prepare necessary documentation
4. Submit notifications within required timeframes
5. Document all communication with regulators

#### 5.2.3 Public Communications

For public-facing incidents:

- All public communications must be approved by CTO
- Coordinate with communications representative
- Provide factual, concise information
- Direct media inquiries to designated spokesperson
- Monitor media coverage and social media

## 6. Client Environment Incidents

### 6.1 Client-Specific Response

#### 6.1.1 Client Environment Containment

When responding to incidents in client environments:

- Follow client-specific incident procedures if defined
- Implement containment while minimizing service disruption
- Coordinate actions with client technical teams
- Document client-specific actions
- Adhere to contractual SLAs

#### 6.1.2 Client Notification

Notify clients according to:

- Contractual requirements
- Regulatory obligations
- Agreed communication procedures
- Severity and impact

#### 6.1.3 Client Coordination

Coordinate response with clients:

- Establish clear communication channels
- Define roles and responsibilities
- Share relevant information
- Coordinate remediation activities
- Provide regular status updates

### 6.2 Managed Services Incidents

#### 6.2.1 Managed Service Response

For managed services:

- Follow service-specific incident procedures
- Prioritize based on service impact and SLAs
- Implement containment while maintaining service levels
- Use established escalation procedures
- Document service impact and restoration

#### 6.2.2 Multi-Client Impacts

When multiple clients are affected:

- Prioritize based on severity and impact
- Coordinate communications across account teams
- Implement consistent remediation approaches
- Track client-specific status
- Document lessons learned for service improvement

## 7. Special Incident Types

### 7.1 Data Breach Response

#### 7.1.1 Data Breach Assessment

When a data breach is suspected:

1. Identify potentially compromised data
2. Determine data types and sensitivity
3. Assess regulatory implications
4. Estimate scope and number of affected individuals
5. Document assessment findings

#### 7.1.2 Data Breach Notification Requirements

Determine notification requirements:

- Identify applicable regulations (e.g., GDPR, regional laws)
- Determine notification timelines
- Prepare required notification content
- Document notification decisions and actions

#### 7.1.3 Data Breach Containment

Contain data breaches by:

- Stopping ongoing data exfiltration
- Revoking unauthorized access
- Securing compromised systems
- Implementing additional monitoring
- Documenting containment actions

### 7.2 Ransomware Response

#### 7.2.1 Ransomware Containment

For ransomware incidents:

1. Immediately isolate affected systems
2. Disable network connections
3. Power off unaffected systems if appropriate
4. Block relevant network traffic
5. Preserve ransomware samples for analysis

#### 7.2.2 Ransomware Assessment

Assess the ransomware situation:

- Identify ransomware variant
- Determine encryption mechanism
- Assess availability of decryption tools
- Evaluate backup availability and integrity
- Document extent of encryption

#### 7.2.3 Ransomware Recovery

Implement recovery strategy:

- Restore from clean backups
- Rebuild systems where necessary
- Verify system integrity
- Implement additional security controls
- Document recovery approach and effectiveness

### 7.3 Account Compromise

#### 7.3.1 Account Containment

When account compromise is detected:

1. Immediately reset compromised credentials
2. Implement additional authentication factors if available
3. Review and revoke active sessions
4. Monitor for suspicious activity
5. Document containment actions

#### 7.3.2 Impact Assessment

Assess the impact of compromised accounts:

- Review account activity logs
- Identify accessed systems and data
- Determine if privilege escalation occurred
- Assess if additional accounts were compromised
- Document assessment findings

#### 7.3.3 Account Recovery

Implement account recovery:

- Create new credentials
- Review and adjust access rights
- Implement additional monitoring
- Verify successful remediation
- Document recovery actions

## 8. Incident Response Testing

### 8.1 Testing Approaches

#### 8.1.1 Tabletop Exercises

Conduct scenario-based discussions:

- Develop realistic incident scenarios
- Involve relevant team members
- Walk through response procedures
- Identify gaps and improvement areas
- Document exercise results

#### 8.1.2 Functional Exercises

Test specific response capabilities:

- Simulate specific incident components
- Test technical response capabilities
- Validate communication procedures
- Exercise decision-making processes
- Document test results

#### 8.1.3 Full-Scale Exercises

Conduct comprehensive response simulations:

- Simulate complete incident scenarios
- Involve all response team members
- Execute actual response procedures
- Test all phases of incident response
- Document exercise outcomes

### 8.2 Testing Schedule

Conduct testing according to the following schedule:

- Tabletop exercises: Quarterly
- Functional exercises: Semi-annually
- Full-scale exercises: Annually
- Post-incident tests: After significant incidents or changes

### 8.3 Testing Documentation

Document all testing activities:

- Test objectives and scope
- Participants and roles
- Scenario details
- Test results and observations
- Identified improvements
- Action plans

## 9. Tools and Resources

### 9.1 Incident Response Tools

#### 9.1.1 Detection and Analysis Tools

- Security Information and Event Management (SIEM) system
- Endpoint Detection and Response (EDR) tools
- Network monitoring and traffic analysis tools
- Log analysis tools
- Malware analysis environment

#### 9.1.2 Containment and Recovery Tools

- Network isolation tools
- System backup and restoration tools
- Forensic analysis tools
- Security scanning tools
- Secure communication platforms

### 9.2 Incident Response Resources

#### 9.2.1 Documentation Resources

- Incident Response Form (ISMS-FORM-03)
- Incident Handler's Journal template
- Evidence Collection Checklist
- Client Notification Templates
- Post-Incident Review Template

#### 9.2.2 External Resources

- Threat intelligence services
- External forensic specialists contact information
- Legal counsel contact information
- Regulatory authority contacts
- Law enforcement contacts

## 10. Roles and Responsibilities

### 10.1 General Staff

- Promptly report suspected security incidents
- Take immediate containment actions within their authority
- Preserve evidence when possible
- Cooperate with incident response activities
- Maintain confidentiality of incident information

### 10.2 Technical Staff

- Assist with technical investigation and containment
- Implement required security measures
- Support system recovery activities
- Document technical actions taken
- Participate in post-incident reviews

### 10.3 Management

- Provide necessary resources for incident response
- Make business decisions during significant incidents
- Approve external communications
- Support post-incident improvement activities
- Ensure lessons learned are implemented

## 11. Procedure Review

This procedure will be reviewed annually, after significant incidents, or when substantial changes occur to ensure it remains effective and aligned with business requirements.

## 12. Related Documents

- ISMS-POL-01: Information Security Management Policy
- ISMS-POL-04: Incident Management Policy
- ISMS-FORM-03: Security Incident Report Form
- ISMS-PROC-04: Asset Management Procedure
- ISMS-PROC-05: Backup & Recovery Procedure

---

_By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Security Incident Response Procedure._
