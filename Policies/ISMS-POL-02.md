# Enablis Data Protection & Classification Policy

**Document ID**: ISMS-POL-02  
**Version**: 1.0  
**Last Updated**: February 25, 2025  
**Owner**: Chief Technology Officer  
**Approved by**: Board of Directors

## 1. Purpose and Scope

### 1.1 Purpose

This Data Protection & Classification Policy establishes the framework for protecting and managing data at Enablis. It provides clear guidelines for classifying information, implementing appropriate security controls, and ensuring compliance with data protection regulations while maintaining operational efficiency.

### 1.2 Scope

This policy applies to:

- All data created, processed, stored, or transmitted by Enablis
- Client data managed or accessed by Enablis
- All employees, contractors, and temporary staff of Enablis
- All systems, applications, and environments used for data processing
- All locations from which Enablis business is conducted, including remote environments

## 2. Data Protection Principles

Enablis follows these core principles for data protection:

### 2.1 Accountability

We take responsibility for how we handle data and implement appropriate measures to demonstrate compliance with data protection principles.

### 2.2 Minimization

We collect, process, and retain only the data necessary for legitimate business purposes.

### 2.3 Transparency

We provide clear information about how we use data and respect the rights of individuals whose data we process.

### 2.4 Security

We implement appropriate technical and organizational measures to protect data from unauthorized access, disclosure, or loss.

### 2.5 Purpose Limitation

We process data only for specified, explicit, and legitimate purposes and not in ways incompatible with those purposes.

## 3. Data Classification Framework

### 3.1 Classification Levels

Enablis uses a three-level classification system:

| Classification   | Description                                                    | Examples                                                                                                                                   |
| ---------------- | -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **Public**       | Information that can be freely shared                          | - Marketing materials<br>- Public website content<br>- Published case studies<br>- Open-source contributions                               |
| **Internal**     | Information for use within Enablis or with authorized partners | - Internal processes<br>- General project methodologies<br>- Team structures<br>- Non-sensitive business information                       |
| **Confidential** | Sensitive information requiring protection                     | - Client data and projects<br>- Financial information<br>- Employee personal data<br>- Strategic business plans<br>- Intellectual property |

### 3.2 Classification Criteria

When determining the appropriate classification level, consider:

- Potential impact if the information is disclosed, modified, or lost
- Legal, regulatory, or contractual obligations
- Business value and sensitivity
- Client expectations and requirements

### 3.3 Classification Ownership

- The original creator or owner of information is responsible for initial classification
- Classification may be changed by the information owner or authorized delegates
- The Security Manager will provide guidance on classification decisions when needed

## 4. Handling Requirements by Classification

### 4.1 Public Information

#### 4.1.1 Access Controls

- No specific access restrictions
- May be shared freely internally and externally

#### 4.1.2 Storage

- Can be stored on any approved system
- No encryption requirements

#### 4.1.3 Transmission

- Can be transmitted via any channel
- No encryption requirements

#### 4.1.4 Disposal

- No special disposal requirements

### 4.2 Internal Information

#### 4.2.1 Access Controls

- Available to all Enablis staff by default
- May be shared with authorized third parties with appropriate agreements

#### 4.2.2 Storage

- Must be stored on Enablis-approved systems
- Encryption recommended for mobile devices

#### 4.2.3 Transmission

- Encryption recommended when transmitted externally
- Appropriate authentication for system access

#### 4.2.4 Disposal

- Electronic data should be deleted when no longer needed
- Physical documents should be placed in secure disposal bins

### 4.3 Confidential Information

#### 4.3.1 Access Controls

- Restricted to individuals with a business need to know
- Access should be revoked when no longer required
- Authentication controls must include multi-factor authentication where feasible

#### 4.3.2 Storage

- Must be stored on approved secure systems with appropriate access controls
- Must be encrypted when stored on mobile devices or removable media
- Cloud storage must include appropriate security controls

#### 4.3.3 Transmission

- Must be encrypted during transmission
- Secure file transfer methods must be used
- Verification of recipient identity before transmission

#### 4.3.4 Disposal

- Electronic data must be securely wiped using approved methods
- Physical documents must be cross-cut shredded or placed in secure disposal bins
- Disposal must be documented where required by regulations or contracts

## 5. Client Data Management

### 5.1 Client Data Classification

- Client data will be treated as Confidential by default
- Classification may be adjusted based on specific client requirements
- Client data classification must be documented in project security plans

### 5.2 Client Data Access

- Access to client data must be restricted to staff working on the respective client project
- Access privileges must be reviewed regularly during project delivery
- Access must be promptly revoked when staff leave projects

### 5.3 Client Data Segregation

- Client data must be logically or physically segregated from other clients' data
- Development environments must not contain production client data unless specifically authorized
- Client data must not be used for testing purposes without explicit client approval

### 5.4 Client Data Retention and Return

- Client data must be retained only as long as necessary for the purposes for which it was collected
- Client data must be returned or securely destroyed upon project completion or as specified in client agreements
- Evidence of data return or destruction must be maintained where required

## 6. Personal Data Protection

### 6.1 Lawful Basis for Processing

Enablis will ensure all personal data processing has a valid lawful basis, such as:

- Consent of the data subject
- Necessity for contract performance
- Compliance with legal obligations
- Legitimate interests where appropriate

### 6.2 Data Subject Rights

Enablis respects and facilitates data subject rights, including:

- Right to be informed about data processing
- Right of access to personal data
- Right to rectification of inaccurate data
- Right to erasure where appropriate
- Right to restrict processing
- Right to data portability
- Right to object to processing

### 6.3 Data Protection Impact Assessments

- Data Protection Impact Assessments (DPIAs) will be conducted for processing activities likely to result in high risk to individuals
- The Security Manager will provide guidance on when DPIAs are required
- DPIA results will inform security controls and processing decisions

## 7. Data Security Controls

### 7.1 Technical Controls

Enablis implements technical controls appropriate to data classification:

#### 7.1.1 Access Controls

- Role-based access control
- Multi-factor authentication for confidential data
- Privileged access management
- Regular access reviews

#### 7.1.2 Encryption

- Transport Layer Security (TLS) for data in transit
- Encryption for confidential data at rest
- Secure key management

#### 7.1.3 Data Loss Prevention

- Monitoring of data transfers
- Controls to prevent unauthorized data exfiltration
- Email security controls

#### 7.1.4 Backup and Recovery

- Regular backups of important data
- Encryption of backup media containing confidential data
- Tested recovery procedures

### 7.2 Procedural Controls

Procedural controls supplement technical measures:

#### 7.2.1 Data Handling Procedures

- Clear guidelines for data sharing
- Processes for secure data transfer
- Procedures for data disposal

#### 7.2.2 Data Breach Response

- Defined process for reporting and handling data breaches
- Notification procedures for affected individuals and regulators
- Post-breach analysis and improvements

#### 7.2.3 Third-Party Data Sharing

- Due diligence of third parties before sharing data
- Data processing agreements where required
- Monitoring of third-party compliance

## 8. Data in Development Environments

### 8.1 Development Data Controls

- Production data must not be used in development environments without approval
- Personal or confidential data must be anonymized or pseudonymized when used for development
- Development environments must implement appropriate security controls based on data sensitivity

### 8.2 Data Masking and Anonymization

- Techniques for data masking or anonymization must be appropriate for the data type
- Anonymization must be irreversible when used for data sets that will be retained
- Effectiveness of anonymization techniques must be verified

### 8.3 Test Data Management

- Test data creation should be automated where possible
- Synthetic data should be used instead of production data where feasible
- Test data must be managed according to its sensitivity

## 9. Data in Cloud Environments

### 9.1 Cloud Data Storage

- Cloud services storing confidential data must be assessed for security
- Data residency requirements must be identified and addressed
- Encryption must be implemented for confidential data

### 9.2 Cloud Access Controls

- Access to cloud services must follow the principle of least privilege
- Cloud administrative access must be tightly controlled
- Cloud security configurations must be regularly reviewed

### 9.3 Cloud Provider Assessment

- Cloud service providers must be assessed for security capabilities
- Contracts must address data protection requirements
- Regular monitoring of cloud provider compliance

## 10. Data Incident Management

### 10.1 Data Breach Identification

Potential data breaches include:

- Unauthorized access to data
- Loss or theft of data
- Accidental disclosure of data
- Alteration of data without permission

### 10.2 Data Breach Response

The response to data breaches will follow the Incident Management Policy (ISMS-POL-04) with additional considerations for:

- Assessment of data breach severity
- Notification requirements under data protection regulations
- Communication with affected data subjects
- Documentation of the breach and response actions

### 10.3 Data Breach Prevention

Preventive measures include:

- Regular security awareness training
- Data security risk assessments
- Implementation of appropriate security controls
- Monitoring and alerting on potential data security issues

## 11. Data Protection in Project Delivery

### 11.1 Security in Project Lifecycle

- Data protection requirements must be identified during project initiation
- Security controls must be implemented during project delivery
- Data handling procedures must be included in project documentation
- Data disposal or return must be addressed during project closure

### 11.2 Project Data Security Plans

For projects involving sensitive data:

- A Project Security Plan must be created
- Data flows must be documented
- Security controls must be specified
- Roles and responsibilities must be defined

### 11.3 Client Data Handling Requirements

- Client-specific data requirements must be documented
- Compliance with client security policies must be verified
- Exceptions to standard data handling must be approved and documented

## 12. Cross-Border Data Transfers

### 12.1 Transfer Assessment

Before transferring data across borders:

- Legal requirements must be identified
- Appropriate transfer mechanisms must be implemented
- Data subject rights must be preserved

### 12.2 Transfer Mechanisms

Mechanisms for lawful cross-border transfers include:

- Adequacy decisions for certain countries
- Standard contractual clauses
- Binding corporate rules
- Explicit consent (in limited circumstances)

### 12.3 Transfer Documentation

Documentation of cross-border transfers must include:

- Countries involved
- Types of data transferred
- Transfer mechanisms used
- Security measures implemented

## 13. Data Retention and Disposal

### 13.1 Retention Periods

- Retention periods must be established for all data types
- Retention must be based on business needs and legal requirements
- Retention periods must be documented and communicated

### 13.2 Secure Disposal

- Data disposal methods must be appropriate to data classification
- Disposal of confidential data must be secure and verified
- Disposal must be documented where required by regulations

### 13.3 Media Handling

- Media containing confidential data must be securely stored
- Reuse of media must include secure erasure of previous content
- Disposal of media must prevent recovery of data

## 14. Training and Awareness

### 14.1 Staff Training

All staff must receive training on:

- Data classification and handling
- Personal data protection requirements
- Security controls for different data types
- Incident reporting procedures

### 14.2 Specialized Training

Staff with specific data responsibilities must receive additional training on:

- Data protection regulatory requirements
- Data security techniques
- Risk assessment methods
- Incident response procedures

## 15. Compliance Monitoring

### 15.1 Compliance Verification

- Regular assessments of data protection practices
- Monitoring of data handling activities
- Auditing of access to sensitive data
- Validation of security control effectiveness

### 15.2 Reporting and Metrics

- Data protection metrics will be defined and monitored
- Regular reporting to senior management
- Identification of improvement opportunities
- Tracking of data protection initiatives

## 16. Exceptions

Exceptions to this policy may be granted only after a documented risk assessment and formal approval by the Security Manager or CTO. All exceptions must be:

- Documented using the Security Exception Request Form (ISMS-FORM-05)
- Time-limited with a defined expiration date
- Reviewed periodically for continued necessity
- Accompanied by compensating controls where appropriate

## 17. Responsibilities

### 17.1 All Staff

- Classify information appropriately
- Handle data according to its classification
- Report data incidents promptly
- Complete required training

### 17.2 Security Manager

- Maintain this policy
- Provide guidance on data classification
- Monitor compliance
- Coordinate data protection activities

### 17.3 Department Managers

- Ensure staff awareness of this policy
- Implement appropriate data controls
- Review data access regularly
- Support data protection initiatives

### 17.4 Project Managers

- Include data protection in project planning
- Ensure client data requirements are met
- Verify appropriate controls during delivery
- Address data handling in project closure

## 18. Policy Review

This policy will be reviewed annually or when significant changes occur to ensure it remains aligned with business requirements, regulatory obligations, and security best practices.

## 19. Related Documents

- ISMS-POL-01: Information Security Management Policy
- ISMS-POL-03: Access Control & Identity Management Policy
- ISMS-POL-04: Incident Management Policy
- ISMS-PROC-02: Secure Client Engagement Procedure
- ISMS-FORM-02: Client Security Requirements Questionnaire
- ISMS-FORM-04: Project Security Plan Template
- ISMS-FORM-05: Security Exception Request Form

---

_By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Data Protection & Classification Policy._
