---
layout: document
title: "Incident Management Policy"
permalink: /policies/isms-pol-04/
---

**Document ID**: ISMS-POL-04  
**Version**: 1.0  
**Last Updated**: February 25, 2025  
**Owner**: Chief Technology Officer  
**Approved by**: Board of Directors

## 1. Purpose and Scope

### 1.1 Purpose

This Incident Management Policy establishes the framework for effectively identifying, responding to, and recovering from security incidents affecting Enablis and its clients. It ensures a structured approach to incident management while maintaining business continuity and minimizing adverse impacts.

### 1.2 Scope

This policy applies to:

- All security incidents affecting Enablis systems, data, or services
- All employees, contractors, and temporary staff of Enablis
- Client environments managed by Enablis
- Third-party services and cloud environments used by Enablis
- All locations from which Enablis business is conducted, including remote environments

## 2. Incident Management Principles

Enablis applies these core principles to our incident management approach:

### 2.1 Rapid Response

We prioritize swift, decisive action to contain and resolve incidents, focusing on minimizing impact to our business and clients.

### 2.2 Transparent Communication

We communicate clearly and appropriately with affected stakeholders, providing accurate information without unnecessary delay.

### 2.3 Continuous Learning

We view incidents as opportunities to improve our security posture, conducting thorough analysis and implementing lessons learned.

### 2.4 Structured Approach

We follow a consistent, documented process for incident management while maintaining flexibility to address unique situations.

### 2.5 Trust and Empowerment

We trust our staff to make appropriate decisions during incident response, empowering them to take necessary actions within their areas of responsibility.

## 3. Incident Definition and Classification

### 3.1 Security Incident Definition

A security incident is defined as an event that actually or potentially compromises:

- The confidentiality, integrity, or availability of information systems or data
- The security policies, procedures, or controls of Enablis
- The security of client systems or data managed by Enablis

### 3.2 Incident Classification

Incidents are classified based on their impact and urgency:

| Classification | Description                                                                  | Response Time                                                            | Examples                                                                                                          |
| -------------- | ---------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------- |
| **Critical**   | Severe impact on critical systems or client services with wide-scale effects | Immediate response (24/7)                                                | - Ransomware attack<br>- Data breach involving client data<br>- Critical system outage affecting multiple clients |
| **High**       | Significant impact on important systems or services with limited scope       | Response within 2 hours (business hours) or 4 hours (non-business hours) | - Targeted malware infection<br>- Unauthorized system access<br>- Loss of sensitive internal data                 |
| **Medium**     | Limited impact on non-critical systems or services                           | Response within 8 business hours                                         | - Suspicious activities requiring investigation<br>- Minor policy violations<br>- Isolated service disruption     |
| **Low**        | Minimal impact with no immediate effect on business operations               | Response within 24 business hours                                        | - Unsuccessful intrusion attempts<br>- Minor security policy violations<br>- Single-user issues                   |

### 3.3 Incident Examples

Examples of security incidents include but are not limited to:

- Unauthorized access to systems or data
- Malware infections
- Data breaches or unauthorized disclosure
- Denial of service attacks
- Theft or loss of equipment containing sensitive data
- Unauthorized system changes
- Social engineering attempts

## 4. Roles and Responsibilities

### 4.1 All Staff

- Identify and report potential security incidents
- Take immediate containment actions within their authority
- Cooperate with incident response activities
- Maintain confidentiality of incident information

### 4.2 Security Manager

- Overall responsibility for incident management
- Classification of incidents and coordination of response
- Communication with management and stakeholders
- Decision-making authority during incident response
- Post-incident review facilitation

### 4.3 Incident Response Team

- Investigation and analysis of incidents
- Implementation of containment and eradication measures
- System recovery and verification
- Documentation of response activities
- Support for post-incident analysis

### 4.4 Chief Technology Officer

- Strategic oversight of significant incidents
- Approval of major response decisions
- Communication with executive management
- Resource allocation for incident response
- Final authority on critical incident decisions

### 4.5 Client Account Managers

- Communication with affected clients
- Coordination of client-specific response requirements
- Management of client expectations
- Documentation of client impact and actions

## 5. Incident Response Process

### 5.1 Identification and Reporting

#### 5.1.1 Detection Sources

Incidents may be detected through:

- Security monitoring systems and alerts
- Staff observations
- Client reports
- Third-party notifications
- Vulnerability assessments
- Automated security tools

#### 5.1.2 Reporting Procedures

- All potential incidents must be reported promptly to the Security Manager
- Reports should include as much detail as available
- After-hours reporting methods are available for urgent incidents
- Reports can be submitted via:
  - Email to security@enablis.co
  - Phone to the security hotline
  - In-person to any member of the security team
  - Messaging on the #security-alerts channel

### 5.2 Assessment and Classification

#### 5.2.1 Initial Assessment

- Verify whether a security incident has occurred
- Gather preliminary information on scope and impact
- Determine the incident classification
- Activate the appropriate response level

#### 5.2.2 Incident Documentation

- Create an incident record
- Document initial findings and assessment
- Establish a timeline of events
- Record all response actions

### 5.3 Containment

#### 5.3.1 Immediate Containment

- Implement measures to limit the immediate impact
- Isolate affected systems when necessary
- Block malicious activity
- Preserve evidence for investigation

#### 5.3.2 Containment Strategies

Different containment strategies may be appropriate depending on the incident:

- Network isolation
- Account lockdown
- Temporary service suspension
- Implementation of additional security controls

### 5.4 Investigation and Analysis

#### 5.4.1 Investigation Process

- Determine the scope of the incident
- Identify affected systems and data
- Establish the timeline of events
- Determine the root cause when possible
- Identify vulnerabilities that were exploited

#### 5.4.2 Evidence Collection

- Collect evidence according to forensic best practices when required
- Maintain chain of custody for potential legal proceedings
- Document system state and activities
- Preserve logs and activity records

### 5.5 Eradication and Recovery

#### 5.5.1 Eradication

- Remove malicious content
- Address vulnerabilities that were exploited
- Reset compromised credentials
- Validate system integrity

#### 5.5.2 Recovery

- Restore systems to operational state
- Verify system and data integrity
- Implement additional security controls as needed
- Perform security testing before returning to production

### 5.6 Post-Incident Activities

#### 5.6.1 Post-Incident Review

- Conduct a post-incident review meeting
- Analyze the effectiveness of the response
- Identify security improvements
- Document lessons learned

#### 5.6.2 Improvement Implementation

- Update security controls based on lessons learned
- Revise policies and procedures as needed
- Implement preventive measures
- Enhance monitoring capabilities

## 6. Communication and Escalation

### 6.1 Internal Communication

#### 6.1.1 Management Notification

- Critical incidents: Immediate notification to CTO and CEO
- High incidents: Notification to CTO within 2 hours
- Medium incidents: Notification to department heads as appropriate
- Low incidents: Included in regular security reporting

#### 6.1.2 Staff Communication

- Need-to-know information sharing
- Clear communication of required actions
- Regular status updates for significant incidents
- Final notification when incidents are resolved

### 6.2 Client Communication

#### 6.2.1 Client Notification Criteria

Clients will be notified when:

- Their data or systems are affected
- Service delivery is or will be impacted
- Contractual obligations require notification
- Regulatory requirements mandate disclosure

#### 6.2.2 Notification Process

- Account managers lead client communications
- Communication must be approved by the Security Manager
- Communications should be clear, accurate, and timely
- Updates should be provided as significant developments occur

### 6.3 External Communication

#### 6.3.1 Media Communication

- All media communications must be coordinated through the CEO
- Staff should not speak to media about incidents
- Press statements must be reviewed by leadership
- Consistent messaging must be maintained

#### 6.3.2 Regulatory Notification

- Relevant regulatory authorities will be notified as required by law
- Data protection authorities will be notified of applicable data breaches
- Notification timeframes will comply with regulatory requirements
- Legal counsel will be consulted for significant notifications

### 6.4 Escalation Procedures

#### 6.4.1 Escalation Criteria

Incidents will be escalated based on:

- Severity and business impact
- Scope and complexity
- Need for additional resources
- Strategic decision requirements

#### 6.4.2 Escalation Path

- Security Manager → CTO → CEO → Board of Directors
- Escalation should occur without unnecessary delay
- Escalation should include a summary of the incident, actions taken, and recommendations

## 7. Specialized Incident Types

### 7.1 Data Breach Incidents

#### 7.1.1 Data Breach Definition

A data breach is unauthorized access to, or disclosure of, protected data such as:

- Personal data subject to privacy regulations
- Client confidential information
- Enablis proprietary information

#### 7.1.2 Data Breach Response

Additional steps for data breaches include:

- Identification of affected data and data subjects
- Assessment of regulatory notification requirements
- Development of affected party notification plans
- Implementation of additional monitoring for affected data

### 7.2 Ransomware and Destructive Attacks

#### 7.2.1 Containment Priorities

- Immediate network isolation of affected systems
- Shutdown of vulnerable systems if necessary
- Blocking of malware communication channels
- Protection of backup systems

#### 7.2.2 Recovery Strategy

- Restoration from clean backups
- Validation of system integrity before reconnection
- Vulnerability remediation before recovery
- Phased recovery based on business priorities

### 7.3 Client Environment Incidents

#### 7.3.1 Client-Managed Environments

For incidents in client environments managed by the client:

- Notify the client according to contractual obligations
- Provide technical assistance as requested
- Coordinate response activities with client security teams
- Document all actions taken

#### 7.3.2 Enablis-Managed Client Environments

For incidents in client environments managed by Enablis:

- Implement the full incident response process
- Follow client-specific incident procedures if defined
- Prioritize response based on service level agreements
- Provide detailed incident reports to clients

### 7.4 Third-Party and Supply Chain Incidents

#### 7.4.1 Vendor Notification

- Promptly notify vendors of incidents involving their services
- Coordinate response activities with vendor security teams
- Document vendor response and actions
- Assess vendor incident impact on Enablis systems

#### 7.4.2 Vendor-Originated Incidents

- Implement containment measures to isolate from vendor systems if necessary
- Evaluate alternative solutions if vendor services are compromised
- Review vendor security practices after resolution
- Update risk assessments based on incident findings

## 8. Documentation and Reporting

### 8.1 Incident Documentation

#### 8.1.1 Required Documentation

All incidents must be documented including:

- Incident timeline and description
- Systems and data affected
- Actions taken during response
- Recovery activities
- Root cause when identified
- Recommendations for prevention

#### 8.1.2 Documentation Storage

- Incident documentation must be securely stored
- Access must be restricted to authorized personnel
- Documentation must be retained according to retention requirements
- Documentation must be available for audit purposes

### 8.2 Incident Reporting

#### 8.2.1 Internal Reporting

- Summary reports for management
- Detailed technical reports for security and IT teams
- Trend analysis for security improvement
- Metrics for security performance evaluation

#### 8.2.2 External Reporting

- Client reports as required by contracts
- Regulatory reports as required by law
- Law enforcement reports for criminal activities
- Insurance notifications as required by policies

## 9. Testing and Improvement

### 9.1 Incident Response Testing

#### 9.1.1 Test Methods

- Tabletop exercises at least quarterly
- Functional drills at least annually
- Full simulations for critical scenarios annually
- Technical tests integrated with security testing

#### 9.1.2 Test Scope

Tests should cover various scenarios including:

- Data breaches
- Ransomware attacks
- System compromises
- Denial of service
- Client environment incidents

### 9.2 Continuous Improvement

#### 9.2.1 Review Process

- Post-incident reviews for all significant incidents
- Periodic review of incident trends
- Annual review of the incident response process
- Regular benchmarking against industry standards

#### 9.2.2 Improvement Implementation

- Security control enhancements
- Process refinements
- Documentation updates
- Training improvements

## 10. Training and Awareness

### 10.1 Incident Response Team Training

#### 10.1.1 Technical Training

- Incident investigation techniques
- Forensic tools and methods
- Containment strategies
- Recovery procedures

#### 10.1.2 Process Training

- Incident classification
- Communication protocols
- Documentation requirements
- Decision-making authority

### 10.2 General Staff Awareness

#### 10.2.1 Awareness Topics

- Incident identification
- Reporting procedures
- Initial response actions
- Communication boundaries

#### 10.2.2 Awareness Methods

- Security awareness program
- Incident response overviews
- Case studies from past incidents
- Regular security updates

## 11. Client-Specific Considerations

### 11.1 Client Requirements

#### 11.1.1 Contractual Obligations

- Review client contracts for incident response requirements
- Document client-specific procedures where needed
- Ensure alignment between Enablis and client processes
- Validate compliance with client requirements

#### 11.1.2 Industry-Specific Requirements

- Identify industry-specific incident response requirements
- Implement additional controls for regulated industries
- Maintain awareness of regulatory changes
- Document compliance with industry standards

### 11.2 Client Collaboration

#### 11.2.1 Joint Response

- Establish collaboration procedures with clients
- Define roles and responsibilities
- Identify communication channels
- Document escalation paths

#### 11.2.2 Client Integration

- Integrate with client incident response processes where appropriate
- Participate in client incident response testing
- Share relevant threat intelligence
- Coordinate security monitoring

## 12. Exceptions

Exceptions to this policy may be granted only after a documented risk assessment and formal approval by the Security Manager or CTO. All exceptions must be:

- Documented using the Security Exception Request Form (ISMS-FORM-05)
- Time-limited with a defined expiration date
- Reviewed periodically for continued necessity
- Accompanied by compensating controls where appropriate

## 13. Policy Review

This policy will be reviewed annually or when significant changes occur to ensure it remains aligned with business requirements, threat landscape changes, and industry best practices.

## 14. Related Documents

- ISMS-POL-01: Information Security Management Policy
- ISMS-POL-02: Data Protection & Classification Policy
- ISMS-POL-03: Access Control & Identity Management Policy
- ISMS-PROC-03: Security Incident Response Procedure
- ISMS-FORM-03: Security Incident Report Form
- ISMS-FORM-05: Security Exception Request Form

---

_By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Incident Management Policy._
