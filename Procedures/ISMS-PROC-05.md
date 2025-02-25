# Enablis Backup & Recovery Procedure

**Document ID**: ISMS-PROC-05  
**Version**: 1.0  
**Last Updated**: February 25, 2025  
**Owner**: Chief Technology Officer  
**Approved by**: Board of Directors

## 1. Purpose and Scope

### 1.1 Purpose

This Backup & Recovery Procedure establishes the requirements for protecting Enablis information through regular backups and verified recovery capabilities. It ensures business continuity, data integrity, and availability while maintaining appropriate security controls.

### 1.2 Scope

This procedure applies to:

- All information systems owned or managed by Enablis
- Data stored on Enablis systems and infrastructure
- Cloud services used by Enablis
- Client systems and data for which Enablis has contractual backup responsibilities
- All employees, contractors, and temporary staff responsible for managing backups

## 2. Backup Strategy and Planning

### 2.1 Backup Requirements Analysis

#### 2.1.1 Data Criticality Assessment

Determine backup requirements based on:

- Business value of the data
- Operational impact if data is lost
- Regulatory and compliance requirements
- Client requirements and expectations
- Cost of data recreation

#### 2.1.2 Recovery Objectives

Define recovery objectives for each system and data set:

- Recovery Time Objective (RTO): Maximum acceptable time for restoring the system
- Recovery Point Objective (RPO): Maximum acceptable data loss period
- Recovery Level Objective (RLO): Required level of functionality after recovery

#### 2.1.3 System and Data Inventory

Maintain an inventory of systems and data requiring backup:

- Document system dependencies
- Identify data owners
- Determine backup frequency requirements
- Document retention requirements
- Identify special backup considerations

### 2.2 Backup Classification

Classify backup requirements based on data criticality:

| Classification | Recovery Time Objective | Recovery Point Objective | Backup Frequency | Retention Period |
| -------------- | ----------------------- | ------------------------ | ---------------- | ---------------- |
| Critical       | < 4 hours               | < 1 hour                 | Hourly           | 12 months        |
| Important      | < 24 hours              | < 24 hours               | Daily            | 6 months         |
| Standard       | < 72 hours              | < 48 hours               | Weekly           | 3 months         |
| Low            | < 1 week                | < 1 week                 | Monthly          | 1 month          |

### 2.3 Backup Method Selection

#### 2.3.1 Method Determination

Select appropriate backup methods based on:

- Recovery objectives
- System type and architecture
- Data volume and change rate
- Available resources
- Technical constraints

#### 2.3.2 Backup Types

Implement appropriate backup types:

- **Full Backup**: Complete copy of all selected data
- **Incremental Backup**: Backup of data changed since the last backup
- **Differential Backup**: Backup of data changed since the last full backup
- **Snapshot**: Point-in-time capture of data state
- **Continuous Data Protection**: Real-time capture of data changes

#### 2.3.3 Technical Approach

Select technical approaches appropriate to each system:

- Agent-based backup
- Agentless backup
- Application-aware backup
- File-level backup
- Image-level backup
- Database backup (dump, log shipping, replication)

## 3. Backup Implementation

### 3.1 Backup Scheduling

#### 3.1.1 Schedule Development

Develop backup schedules considering:

- Required frequency based on classification
- System usage patterns
- Network bandwidth availability
- Maintenance windows
- Interdependencies between systems

#### 3.1.2 Schedule Documentation

Document backup schedules including:

- Systems and data covered
- Backup type and method
- Start time and estimated duration
- Dependencies and prerequisites
- Responsible personnel

#### 3.1.3 Schedule Review

Regularly review backup schedules to ensure:

- Alignment with current business needs
- Accommodation of new systems
- Optimization of backup windows
- Resolution of scheduling conflicts
- Appropriate resource allocation

### 3.2 Backup Storage

#### 3.2.1 Storage Location

Implement appropriate storage locations:

- On-site storage for rapid recovery
- Off-site storage for disaster recovery
- Cloud storage for geographic distribution
- Air-gapped storage for ransomware protection

#### 3.2.2 Storage Media

Select appropriate storage media based on:

- Recovery time requirements
- Capacity needs
- Retention periods
- Security requirements
- Cost considerations

#### 3.2.3 Storage Management

Implement storage management practices:

- Monitor storage capacity
- Enforce retention policies
- Verify media reliability
- Maintain appropriate environmental conditions
- Secure physical access to backup media

### 3.3 Backup Security

#### 3.3.1 Backup Protection

Secure backup data through:

- Encryption of backup data at rest
- Secure transmission of backup data
- Access controls for backup systems
- Physical security for backup media
- Monitoring of backup access

#### 3.3.2 Backup Authentication

Implement authentication for backup operations:

- Strong authentication for backup administrators
- Separate backup credentials
- Privileged access management
- Role-based access control
- Authentication logging

#### 3.3.3 Encryption Requirements

Encrypt backup data according to classification:

- Critical and Important data: Always encrypted
- Standard data: Encrypted when stored off-site
- All backups containing personal data: Always encrypted
- Encryption key management according to the Cryptographic Controls Policy

## 4. Backup Operations

### 4.1 Backup Execution

#### 4.1.1 Automated Backups

For automated backup processes:

- Configure backup software according to defined schedules
- Verify proper configuration
- Implement pre and post-backup scripts if needed
- Document automation procedures
- Test automated processes

#### 4.1.2 Manual Backups

For manual backup processes:

- Document step-by-step procedures
- Create backup checklists
- Define roles and responsibilities
- Implement verification steps
- Document completion

#### 4.1.3 Special Backup Procedures

Develop special procedures for:

- Application-specific backups
- Database backups
- Virtual machine backups
- Cloud service backups
- System state and configuration backups

### 4.2 Backup Monitoring

#### 4.2.1 Success Verification

Monitor backup completion:

- Automated alerting for backup failures
- Daily review of backup status
- Verification of backup integrity
- Investigation of incomplete backups
- Documentation of backup status

#### 4.2.2 Performance Monitoring

Monitor backup performance:

- Backup duration tracking
- Resource utilization during backups
- Backup size trends
- Network impact
- Storage consumption

#### 4.2.3 Issue Resolution

Establish procedures for addressing backup issues:

- Escalation paths for backup failures
- Troubleshooting guidelines
- Resolution timeframes
- Documentation requirements
- Root cause analysis

### 4.3 Backup Documentation

#### 4.3.1 Backup Catalog

Maintain a backup catalog containing:

- Backup date and time
- Systems and data included
- Backup type and method
- Storage location
- Retention period
- Restoration requirements

#### 4.3.2 Backup Logs

Maintain backup logs including:

- Backup job details
- Success/failure status
- Error messages
- Performance metrics
- Administrative actions

#### 4.3.3 Backup Documentation

Maintain backup documentation including:

- Backup system configuration
- Backup schedules
- Storage locations
- Retention policies
- Recovery procedures

## 5. Recovery Procedures

### 5.1 Recovery Preparation

#### 5.1.1 Recovery Requirements

Document recovery requirements for each system:

- Recovery priority
- Required recovery resources
- Dependencies and prerequisites
- Personnel responsibilities
- Success criteria

#### 5.1.2 Recovery Documentation

Develop recovery documentation:

- Step-by-step recovery procedures
- Required recovery resources
- Verification processes
- Rollback procedures
- Contact information for technical support

#### 5.1.3 Recovery Resources

Ensure availability of recovery resources:

- Backup restoration tools
- System installation media
- Configuration documentation
- Password and access information
- Hardware resources

### 5.2 Recovery Execution

#### 5.2.1 Recovery Initiation

Establish procedures for initiating recovery:

- Incident assessment
- Recovery decision authority
- Recovery team activation
- Communication procedures
- Documentation requirements

#### 5.2.2 Recovery Operations

Document recovery operations:

- System recovery sequence
- Data restoration steps
- Configuration restoration
- Dependency management
- Testing and verification

#### 5.2.3 Recovery Validation

Verify successful recovery:

- System functionality testing
- Data integrity validation
- Performance assessment
- Security validation
- User acceptance testing

### 5.3 Post-Recovery Activities

#### 5.3.1 Recovery Documentation

Document recovery activities:

- Recovery timeline
- Actions taken
- Resources used
- Issues encountered
- Resolution steps

#### 5.3.2 Root Cause Analysis

When recovery is due to failure:

- Identify root cause
- Document contributing factors
- Develop preventive measures
- Update procedures as needed
- Implement improvements

#### 5.3.3 Normal Operations Return

Procedures for returning to normal operations:

- Transition from recovery environment
- User notification
- Monitoring requirements
- Performance validation
- Documentation updates

## 6. Backup Testing and Verification

### 6.1 Backup Verification

#### 6.1.1 Routine Verification

Regularly verify backup integrity:

- Automated integrity checks
- Random sample restoration
- Checksum verification
- Backup metadata validation
- Media verification

#### 6.1.2 Verification Schedule

Implement a verification schedule:

- Daily automated integrity checks
- Weekly sample restoration tests
- Monthly verification of long-term backups
- Quarterly verification of offsite backups
- Annual comprehensive verification

#### 6.1.3 Verification Documentation

Document verification activities:

- Verification date and scope
- Verification method
- Results and findings
- Issues identified
- Corrective actions

### 6.2 Recovery Testing

#### 6.2.1 Recovery Test Types

Implement different types of recovery tests:

- **Paper Test**: Review of recovery documentation
- **Walkthrough Test**: Step-by-step review with stakeholders
- **Simulation Test**: Recovery team practice without actual restoration
- **Parallel Test**: Recovery to alternate environment without disruption
- **Full Interruption Test**: Complete recovery with temporary service disruption

#### 6.2.2 Recovery Test Schedule

Conduct recovery tests according to system criticality:

- Critical systems: Quarterly recovery tests
- Important systems: Semi-annual recovery tests
- Standard systems: Annual recovery tests
- Test different scenarios and recovery methods

#### 6.2.3 Test Documentation

Document recovery tests:

- Test objectives and scope
- Test scenario and method
- Participants and roles
- Test results and observations
- Identified improvements

### 6.3 Continuous Improvement

#### 6.3.1 Performance Review

Regularly review backup and recovery performance:

- Success rate analysis
- Speed and efficiency
- Resource utilization
- Cost effectiveness
- Compliance with requirements

#### 6.3.2 Process Improvement

Identify and implement improvements:

- Update procedures based on test results
- Enhance automation
- Optimize resource usage
- Incorporate new technologies
- Address identified gaps

#### 6.3.3 Documentation Updates

Maintain current documentation:

- Update based on test findings
- Incorporate procedure changes
- Reflect system modifications
- Include lessons learned
- Regular review and validation

## 7. Client System Backup Considerations

### 7.1 Client Backup Requirements

#### 7.1.1 Requirements Documentation

Document client backup requirements:

- Systems and data to be backed up
- Recovery objectives (RTO, RPO)
- Retention requirements
- Compliance considerations
- Reporting requirements

#### 7.1.2 Client Agreement

Ensure backup responsibilities are clearly defined:

- Include backup scope in service agreements
- Document backup and recovery SLAs
- Define roles and responsibilities
- Specify communication procedures
- Establish escalation paths

#### 7.1.3 Client-Specific Procedures

Develop client-specific backup procedures as needed:

- Customized backup schedules
- Specific retention policies
- Special handling requirements
- Unique verification methods
- Client-specific reporting

### 7.2 Client Recovery Support

#### 7.2.1 Recovery Request Handling

Establish procedures for client recovery requests:

- Request submission process
- Required information
- Prioritization criteria
- Response timeframes
- Documentation requirements

#### 7.2.2 Client Recovery Execution

Define client recovery procedures:

- Recovery authorization requirements
- Recovery execution steps
- Client involvement
- Verification and acceptance
- Documentation and reporting

#### 7.2.3 Client Communication

Establish client communication procedures:

- Recovery request acknowledgment
- Progress updates
- Completion notification
- Post-recovery reporting
- Issue communication

## 8. Cloud System Backup Considerations

### 8.1 Cloud Service Backup

#### 8.1.1 Cloud Backup Strategy

Develop strategies for cloud service backup:

- SaaS data backup approaches
- PaaS environment backup
- IaaS system backup
- Cross-cloud backup considerations
- Hybrid environment backup

#### 8.1.2 Cloud Backup Methods

Implement appropriate cloud backup methods:

- Native cloud backup features
- Third-party backup solutions
- API-based backup
- Data export capabilities
- Snapshot and replication services

#### 8.1.3 Cloud Recovery Planning

Develop cloud recovery procedures:

- Cross-region recovery
- Cross-cloud recovery
- On-premises recovery from cloud
- Cloud-to-cloud recovery
- Service-specific recovery procedures

### 8.2 Cloud Backup Security

#### 8.2.1 Security Controls

Implement security for cloud backups:

- Encryption for cloud backup data
- Access controls for cloud backup systems
- Secure transmission of backup data
- Multi-factor authentication
- Separation of duties

#### 8.2.2 Compliance Considerations

Address compliance for cloud backups:

- Data residency requirements
- Regulatory compliance
- Audit capabilities
- Retention enforcement
- Data sovereignty considerations

## 9. Development Environment Backup

### 9.1 Development Asset Backup

#### 9.1.1 Source Code Backup

Implement source code backup through:

- Version control system backup
- Repository replication
- Regular export backup
- Branch and tag preservation
- Metadata backup

#### 9.1.2 Development Environment Backup

Back up development environments:

- Development server configuration backup
- Development database backup
- Development tool configuration backup
- Reference data backup
- Documentation backup

#### 9.1.3 Recovery Procedures

Establish recovery procedures for development assets:

- Source code repository restoration
- Development environment reconstruction
- Configuration restoration
- Integration environment recovery
- Documentation recovery

### 9.2 Artifact Management

#### 9.2.1 Build Artifact Backup

Implement backup for build artifacts:

- Binary repository backup
- Release package backup
- Build configuration backup
- Dependency cache backup
- Build metadata backup

#### 9.2.2 Documentation Backup

Back up development documentation:

- Design documentation
- API documentation
- User guides
- Test plans and results
- Project documentation

## 10. Mobile and Remote System Backup

### 10.1 Mobile Device Backup

#### 10.1.1 Mobile Backup Strategy

Develop strategies for mobile device backup:

- Corporate data backup requirements
- Approved backup methods
- User guidance and training
- Verification requirements
- Recovery options

#### 10.1.2 Mobile Backup Implementation

Implement mobile backup solutions:

- Mobile device management (MDM) backup features
- Cloud backup services
- Local backup capabilities
- Selective data backup
- Secure transmission and storage

### 10.2 Remote Worker System Backup

#### 10.2.1 Remote System Backup Requirements

Define backup requirements for remote systems:

- Required backup frequency
- Approved backup methods
- Network considerations
- Verification requirements
- User responsibilities

#### 10.2.2 Remote Backup Implementation

Implement remote backup solutions:

- Cloud-based backup services
- VPN-connected backup
- Automated backup clients
- Bandwidth-efficient backup
- Offline backup capabilities

#### 10.2.3 Remote Recovery Support

Provide remote recovery support:

- Remote recovery guidance
- Self-service recovery options
- Remote assistance capabilities
- Backup verification support
- Emergency recovery procedures

## 11. Disaster Recovery Integration

### 11.1 Disaster Recovery Planning

#### 11.1.1 Disaster Recovery Requirements

Define backup requirements for disaster recovery:

- Offsite backup requirements
- Geographic separation
- Recovery capability at alternate locations
- Time-phased recovery planning
- Interdependency management

#### 11.1.2 Backup Integration

Integrate backup procedures with disaster recovery:

- Ensure backup availability at DR site
- Align backup strategy with DR goals
- Document backup dependencies
- Test backup restoration at DR site
- Maintain backup systems during DR events

### 11.2 Business Continuity Support

#### 11.2.1 Critical Business Function Support

Ensure backups support business continuity:

- Identify critical business function data
- Prioritize backup and recovery
- Align RPOs with business requirements
- Define alternating processing capabilities
- Document manual workarounds during recovery

#### 11.2.2 Continuity Testing

Include backup and recovery in continuity testing:

- Business continuity exercise participation
- Recovery time validation
- Procedure effectiveness assessment
- Resource adequacy verification
- Documentation validation

## 12. Roles and Responsibilities

### 12.1 IT Operations Team

- Implementation and management of backup systems
- Execution of backup procedures
- Monitoring backup success and failure
- Troubleshooting backup issues
- Performance of recovery operations

### 12.2 System Owners

- Definition of backup requirements
- Approval of recovery procedures
- Participation in recovery testing
- Verification of recovery success
- Prioritization of systems for recovery

### 12.3 Security Team

- Definition of backup security requirements
- Verification of backup security controls
- Review of recovery procedures
- Monitoring of backup access
- Security validation during recovery

### 12.4 All Staff

- Compliance with backup procedures
- Proper storage of data in backed-up locations
- Prompt reporting of backup or recovery issues
- Participation in recovery testing when required
- Following security guidelines for backups

## 13. Documentation and Reporting

### 13.1 Required Documentation

Maintain the following documentation:

- Backup strategy and policies
- System backup requirements
- Backup schedules and procedures
- Recovery procedures
- Test results and verification reports

### 13.2 Backup Reporting

Produce regular backup reports:

- Daily backup status summary
- Weekly backup performance report
- Monthly backup compliance report
- Quarterly test and verification report
- Annual backup strategy review

### 13.3 Documentation Management

Manage backup documentation:

- Store documentation securely
- Control access to documentation
- Review and update regularly
- Archive outdated documentation
- Ensure availability during recovery

## 14. Exceptions

Exceptions to this procedure may be granted only after a documented risk assessment and formal approval by the IT Operations Manager or CTO. All exceptions must be:

- Documented using the Security Exception Request Form (ISMS-FORM-05)
- Time-limited with a defined expiration date
- Reviewed periodically for continued necessity
- Accompanied by compensating controls where appropriate

## 15. Procedure Review

This procedure will be reviewed annually or when significant changes occur to ensure it remains effective and aligned with business requirements.

## 16. Related Documents

- ISMS-POL-01: Information Security Management Policy
- ISMS-POL-04: Incident Management Policy
- ISMS-PROC-03: Security Incident Response Procedure
- ISMS-PROC-04: Asset Management Procedure
- ISMS-FORM-05: Security Exception Request Form
- ISMS-FORM-12: Backup Verification Form

---

_By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Backup & Recovery Procedure._
