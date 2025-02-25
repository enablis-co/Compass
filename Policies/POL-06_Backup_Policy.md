# Enablis Backup Policy

**Document ID**: POL-06  
**Version**: 1.0  
**Last Updated**: February 24, 2025  
**Owner**: IT Operations Manager  
**Approved by**: Chief Technology Officer  

## 1. Purpose and Scope

### 1.1 Purpose
This Backup Policy establishes the requirements for backup and recovery of Enablis information systems and data. It ensures that critical information assets can be restored in the event of data loss, corruption, or system failure, while maintaining appropriate security controls.

### 1.2 Scope
This policy applies to:
- All information systems owned or managed by Enablis
- All data stored on Enablis systems and infrastructure
- Cloud services and applications used by Enablis
- Data and systems managed on behalf of clients
- All employees, contractors, and temporary staff responsible for managing backups

## 2. Backup Requirements

### 2.1 Data Classification and Backup Frequency
Backup frequency must align with the classification and criticality of data:

| Data Classification | Backup Frequency | Retention Period |
|---------------------|------------------|------------------|
| Critical            | Daily            | 12 months        |
| Confidential        | Daily            | 6 months         |
| Internal            | Weekly           | 3 months         |
| Public              | Monthly          | 1 month          |

### 2.2 System Backup Requirements
Systems must be backed up based on their criticality:

| System Type                    | Backup Frequency                 | Retention Period |
|--------------------------------|----------------------------------|------------------|
| Production systems             | Daily full, hourly incremental   | 12 months        |
| Development systems            | Weekly full                      | 3 months         |
| Test/QA systems                | As needed before major changes   | 1 month          |
| Client production environments | As per client agreement          | As per client agreement |

### 2.3 Backup Storage Location
- At least one copy of critical and confidential data backups must be stored in a geographically separate location
- Cloud backup solutions must use different regions or availability zones
- Physical backup media must be stored in secure, environmentally controlled facilities

## 3. Technical Implementation

### 3.1 Backup Methods

#### 3.1.1 Full Backups
- Complete backup of all selected data
- Required for initial backup and periodically thereafter
- Baseline for incremental and differential backups

#### 3.1.2 Incremental Backups
- Backup of data changed since the last backup (full or incremental)
- Reduces backup time and storage requirements
- May increase recovery time and complexity

#### 3.1.3 Differential Backups
- Backup of data changed since the last full backup
- Balances backup and recovery time
- May increase storage requirements compared to incremental backups

### 3.2 Backup Encryption
- All backup data must be encrypted at rest and during transmission
- Encryption keys must be managed according to the Cryptographic Controls Procedure (DOC-17)
- Encryption strength must align with current industry standards

### 3.3 Backup Authentication and Access Control
- Access to backup systems and data must be restricted to authorized personnel
- Multi-factor authentication must be used for backup system administration
- Backup system access must be logged and monitored

### 3.4 Automated Backup Solutions
- Backup processes should be automated where possible
- Automated monitoring and alerting must be implemented
- Exception handling procedures must be documented

## 4. Cloud Services and Applications

### 4.1 SaaS Backup Requirements
- Critical data stored in SaaS applications must be backed up
- Backup capabilities must be evaluated when selecting SaaS providers
- Third-party backup solutions should be considered when native backup capabilities are insufficient

### 4.2 Cloud Infrastructure Backup
- Virtual machines and containers must be backed up using snapshots or equivalent methods
- Cloud storage buckets containing critical or confidential data must be versioned
- Infrastructure as Code (IaC) configurations must be backed up and version-controlled

### 4.3 Multi-Cloud Considerations
- Backup strategies must account for multi-cloud environments
- Cross-cloud recovery capabilities should be tested periodically
- Dependencies between cloud services must be documented

## 5. Recovery Requirements

### 5.1 Recovery Time Objectives (RTO)
Recovery Time Objectives must be established for all systems based on business impact:

| System Criticality | Maximum RTO      |
|--------------------|------------------|
| Critical           | 4 hours          |
| High               | 8 hours          |
| Medium             | 24 hours         |
| Low                | 72 hours         |

### 5.2 Recovery Point Objectives (RPO)
Recovery Point Objectives must be established for all data based on business impact:

| Data Criticality   | Maximum RPO      |
|--------------------|------------------|
| Critical           | 1 hour           |
| High               | 4 hours          |
| Medium             | 24 hours         |
| Low                | 1 week           |

### 5.3 Recovery Procedures
- Documented recovery procedures must be maintained for all critical systems
- Recovery procedures must be tested regularly
- Recovery capabilities must be verified after significant system changes

## 6. Backup Testing and Verification

### 6.1 Regular Testing
- Backup recovery must be tested quarterly for critical systems
- Backup recovery must be tested bi-annually for all other systems
- Test results must be documented and reviewed

### 6.2 Verification Methods
- Backup integrity must be verified through automated checks
- Sample data must be restored periodically to verify recoverability
- Complete system recovery tests must be performed in an isolated environment

### 6.3 Testing Documentation
- Test scenarios must be documented
- Test results must be recorded and maintained
- Issues identified during testing must be tracked to resolution

## 7. Client Data Backup Considerations

### 7.1 Client Data Backup Requirements
- Client data backup requirements must be documented in service agreements
- Client-specific backup policies must be implemented when required
- Client approvals must be obtained for backup methods affecting their data

### 7.2 Client Environment Backups
- Development environments for client projects must be backed up according to project requirements
- Client production environments managed by Enablis must have documented backup and recovery plans
- Backup and recovery capabilities must be included in client handover documentation

## 8. Roles and Responsibilities

### 8.1 IT Operations Team
- Implementation and management of backup systems
- Monitoring backup success and failure
- Troubleshooting backup issues
- Executing recovery procedures when required

### 8.2 System Owners
- Defining backup requirements for their systems
- Approving recovery procedures
- Participating in recovery testing
- Validating recovered data and functionality

### 8.3 Security Team
- Reviewing backup security controls
- Ensuring backup compliance with security policies
- Participating in recovery exercises involving critical systems

## 9. Documentation Requirements

### 9.1 Backup System Documentation
- Backup architecture and configuration must be documented
- Backup schedules and retention periods must be documented
- Backup system access controls must be documented

### 9.2 Recovery Documentation
- Step-by-step recovery procedures must be maintained
- Recovery prioritization must be documented
- Contact information for key personnel must be kept current

### 9.3 Inventory of Backup Data
- An inventory of backed-up systems and data must be maintained
- Backup locations and methods must be documented
- Retention periods must be tracked

## 10. Compliance and Audit

### 10.1 Compliance Requirements
- Backup processes must comply with relevant regulations and standards
- Client-specific compliance requirements must be documented and implemented
- Backup logs and documentation must be maintained for audit purposes

### 10.2 Audit Procedures
- Backup processes must be included in regular security audits
- Audit findings must be addressed promptly
- Backup metrics must be reported to management quarterly

## 11. Exceptions

Exceptions to this policy may be granted only after a documented risk assessment and formal approval by the IT Operations Manager or CTO. All exceptions must be:
- Documented with a clear business justification
- Time-limited with a defined expiration date
- Reviewed periodically for continued necessity

## 12. Policy Compliance

### 12.1 Verification
Compliance with this policy will be verified through:
- Regular backup system audits
- Recovery testing results
- Backup success rate metrics
- Independent security assessments

### 12.2 Consequences of Non-Compliance
Failures to comply with this policy may result in:
- Additional controls or oversight
- Remediation requirements
- Disciplinary action in accordance with HR policies

## 13. Policy Review

This policy will be reviewed annually or when significant changes occur to ensure it remains aligned with business requirements, evolving technology, and regulatory obligations.

## 14. Related Documents

- POL-01: Information Security Policy
- DOC-09: Business Continuity Plan
- POL-08: Incident Management Policy
- DOC-17: Cryptographic Controls Procedure
- DOC-18: Backup and Recovery Procedures

---

*By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Backup Policy.*