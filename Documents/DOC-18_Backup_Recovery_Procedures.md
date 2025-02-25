# Enablis Backup and Recovery Procedures

**Document ID**: DOC-18  
**Version**: 1.0  
**Last Updated**: February 24, 2025  
**Owner**: IT Operations Manager  
**Approved by**: Chief Technology Officer

## 1. Introduction

### 1.1 Purpose

This document provides detailed procedures for the implementation of the Enablis Backup Policy (POL-06). It establishes standardized methods for backing up and recovering Enablis information systems and data to ensure business continuity and data protection.

### 1.2 Scope

These procedures apply to:

- All information systems owned or managed by Enablis
- All data stored on Enablis systems and infrastructure
- Cloud services and applications used by Enablis
- Data and systems managed on behalf of clients
- All technical staff responsible for performing backup and recovery operations

## 2. Roles and Responsibilities

### 2.1 IT Operations Manager

- Overall responsibility for backup and recovery operations
- Approving changes to backup schedules and retention periods
- Reviewing backup success/failure reports
- Ensuring adequate resources for backup systems
- Authorizing major recovery operations

### 2.2 System Administrators

- Implementing backup configurations as per these procedures
- Monitoring backup jobs and resolving issues
- Performing routine recovery testing
- Documenting system-specific backup and recovery procedures
- Executing recovery procedures when required

### 2.3 Database Administrators

- Implementing database-specific backup procedures
- Verifying database backup integrity
- Performing database recovery operations
- Maintaining database backup documentation

### 2.4 Cloud Services Team

- Implementing backup procedures for cloud environments
- Managing cloud backup services and configurations
- Verifying cloud data recovery capabilities
- Documenting cloud-specific backup and recovery procedures

### 2.5 Client Services Team

- Communicating backup and recovery capabilities to clients
- Coordinating client-specific backup requirements
- Initiating recovery requests for client environments
- Documenting client backup and recovery arrangements

## 3. Backup Schedule and Retention

### 3.1 Standard Backup Schedule

The following standard backup schedule shall be implemented based on data classification:

| System Type             | Data Classification | Full Backup                   | Incremental Backup        | Retention Period |
| ----------------------- | ------------------- | ----------------------------- | ------------------------- | ---------------- |
| Production servers      | Critical            | Weekly (Sunday)               | Daily (Mon-Sat)           | 12 months        |
| Production servers      | Confidential        | Weekly (Sunday)               | Daily (Mon-Sat)           | 6 months         |
| Production servers      | Internal            | Weekly (Sunday)               | Daily (Mon-Sat)           | 3 months         |
| Development servers     | All classifications | Weekly (Sunday)               | None                      | 1 month          |
| User data (file shares) | All classifications | Weekly (Sunday)               | Daily (Mon-Sat)           | 6 months         |
| Email systems           | All classifications | Weekly (Sunday)               | Daily (Mon-Sat)           | 6 months         |
| Databases               | Critical            | Daily (with transaction logs) | Transaction logs (hourly) | 12 months        |
| Databases               | Confidential        | Daily (with transaction logs) | Transaction logs (hourly) | 6 months         |
| Databases               | Internal            | Weekly (Sunday)               | Daily (Mon-Sat)           | 3 months         |

### 3.2 Client-Specific Backup Schedule

Client-specific backup schedules must be documented separately for each client engagement. The following template should be used:

| Client Name   | System Description   | Data Classification | Full Backup | Incremental Backup | Retention Period | Special Requirements |
| ------------- | -------------------- | ------------------- | ----------- | ------------------ | ---------------- | -------------------- |
| [Client Name] | [System Description] | [Classification]    | [Schedule]  | [Schedule]         | [Period]         | [Requirements]       |

The client-specific backup schedule document must be stored in the client's project documentation repository.

## 4. Backup Methods and Technologies

### 4.1 Server Backup Procedures

#### 4.1.1 Windows Server Backup Procedure

1. Install and configure approved backup software
2. Configure backup destinations according to the 3-2-1 backup strategy
   - Primary backup to local backup storage
   - Secondary backup to network storage
   - Tertiary backup to off-site or cloud storage
3. Configure backup schedule according to Section 3.1
4. Include system state backup for domain controllers and critical servers
5. Exclude temporary files and non-essential data
6. Enable backup encryption using approved encryption methods
7. Configure backup verification to run automatically after completion
8. Set up backup monitoring and alerting
9. Document server-specific backup configuration

#### 4.1.2 Linux Server Backup Procedure

1. Install and configure approved backup software/scripts
2. Configure backup destinations according to the 3-2-1 backup strategy
3. Configure backup schedule according to Section 3.1
4. Include system configuration files in backup selection
5. Exclude temporary directories, cache files, and log archives
6. Enable backup encryption using approved encryption methods
7. Configure automated backup verification
8. Set up backup monitoring and alerting
9. Document server-specific backup configuration

### 4.2 Database Backup Procedures

#### 4.2.1 SQL Server Backup Procedure

1. Configure native SQL Server backup or approved backup solution
2. For Critical and Confidential databases:
   - Configure full daily backups
   - Configure transaction log backups every hour
   - Enable backup compression
   - Configure backup encryption using TDE or backup encryption
3. For Internal databases:
   - Configure full weekly backups
   - Configure differential daily backups
4. Verify backup files are copied to secondary storage
5. Configure backup verification to run automatically
6. Document database-specific backup configuration

#### 4.2.2 PostgreSQL Backup Procedure

1. Configure pg_dump for logical backups or approved backup solution
2. For Critical and Confidential databases:
   - Configure full daily backups
   - Configure WAL archiving for point-in-time recovery
   - Enable backup compression
   - Configure backup encryption
3. For Internal databases:
   - Configure full weekly backups
   - Configure differential daily backups
4. Verify backup files are copied to secondary storage
5. Configure backup verification to run automatically
6. Document database-specific backup configuration

#### 4.2.3 MongoDB Backup Procedure

1. Configure mongodump or approved backup solution
2. For Critical and Confidential databases:
   - Configure full daily backups
   - Enable oplog capturing for point-in-time recovery
   - Enable backup compression
   - Configure backup encryption
3. For Internal databases:
   - Configure full weekly backups
4. Verify backup files are copied to secondary storage
5. Configure backup verification to run automatically
6. Document database-specific backup configuration

### 4.3 Cloud Services Backup Procedures

#### 4.3.1 AWS Backup Procedure

1. Configure AWS Backup or approved third-party solution
2. Create backup plan aligned with requirements from Section 3.1
3. Include EBS volumes, RDS databases, S3 buckets, and other relevant resources
4. Enable cross-region backup copy for critical data
5. Configure appropriate IAM permissions for backup operations
6. Enable backup encryption using KMS
7. Configure backup monitoring through AWS CloudWatch
8. Document AWS-specific backup configuration

#### 4.3.2 Azure Backup Procedure

1. Configure Azure Backup or approved third-party solution
2. Create backup policies aligned with requirements from Section 3.1
3. Include Azure VMs, Azure SQL, Azure Files, and other relevant resources
4. Enable geo-redundant storage for critical backups
5. Configure appropriate RBAC permissions for backup operations
6. Enable backup encryption
7. Configure backup monitoring through Azure Monitor
8. Document Azure-specific backup configuration

#### 4.3.3 Google Cloud Backup Procedure

1. Configure Google Cloud Backup or approved third-party solution
2. Create backup schedule aligned with requirements from Section 3.1
3. Include Compute Engine instances, Cloud SQL, Cloud Storage, and other relevant resources
4. Enable multi-regional backup for critical data
5. Configure appropriate IAM permissions for backup operations
6. Enable backup encryption
7. Configure backup monitoring
8. Document GCP-specific backup configuration

### 4.4 SaaS Application Backup Procedures

#### 4.4.1 Microsoft 365 Backup Procedure

1. Configure approved Microsoft 365 backup solution
2. Include Exchange Online, SharePoint Online, OneDrive, and Teams data
3. Configure backup schedule according to Section 3.1
4. Enable backup encryption
5. Verify backup storage location meets retention requirements
6. Configure backup monitoring and alerting
7. Document M365-specific backup configuration

#### 4.4.2 Salesforce Backup Procedure

1. Configure approved Salesforce backup solution
2. Include all relevant Salesforce objects and attachments
3. Configure backup schedule according to Section 3.1
4. Enable backup encryption
5. Verify backup storage location meets retention requirements
6. Configure backup monitoring and alerting
7. Document Salesforce-specific backup configuration

## 5. Backup Verification and Testing

### 5.1 Routine Backup Verification

#### 5.1.1 Daily Verification Procedure

1. Review backup job status reports each morning
2. Verify all scheduled backups completed successfully
3. Investigate and resolve any backup failures
4. Document resolution in the incident tracking system
5. Update backup documentation if configuration changes were made

#### 5.1.2 Weekly Verification Procedure

1. Perform automated integrity check of recent backup files
2. Verify backup size and content matches expectations
3. Confirm backup storage capacity remains sufficient
4. Verify offsite/cloud backup synchronization
5. Document verification results

### 5.2 Recovery Testing

#### 5.2.1 Monthly File Recovery Testing

1. Select random files from each major system
2. Perform recovery to a test location
3. Verify file contents match the original
4. Document recovery time and results
5. Address any issues identified during testing

#### 5.2.2 Quarterly System Recovery Testing

1. Select a non-production system for recovery testing
2. Prepare isolated test environment
3. Perform full system recovery from backups
4. Verify system functionality post-recovery
5. Measure recovery time against RTO objectives
6. Document recovery procedure effectiveness
7. Update recovery procedures based on findings

#### 5.2.3 Bi-Annual Database Recovery Testing

1. Select a non-production database for recovery testing
2. Prepare isolated test environment
3. Perform database recovery from backups
4. For Critical databases, test point-in-time recovery
5. Verify data integrity post-recovery
6. Measure recovery time against RTO objectives
7. Document recovery procedure effectiveness
8. Update recovery procedures based on findings

#### 5.2.4 Annual Full Disaster Recovery Testing

1. Prepare comprehensive disaster recovery scenario
2. Establish isolated recovery environment
3. Recover multiple interdependent systems from backups
4. Verify system functionality and data integrity
5. Test application connectivity and functionality
6. Measure recovery time against RTO objectives
7. Document recovery procedure effectiveness
8. Update recovery procedures based on findings

### 5.3 Client Environment Testing

Client environment recovery testing must be performed according to client agreements. At minimum:

1. Document client-specific recovery testing requirements
2. Schedule testing as required by client agreements
3. Perform testing according to client-specific procedures
4. Document test results and provide to client if required
5. Address any issues identified during testing

## 6. Recovery Procedures

### 6.1 Recovery Preparation

#### 6.1.1 Recovery Request Procedure

1. Document recovery request details:
   - System/data to be recovered
   - Reason for recovery
   - Required recovery point (date/time)
   - Required completion timeframe
   - Requestor contact information
2. Obtain appropriate approval based on system criticality
3. Assign recovery to appropriate technical team
4. Establish communication plan for the recovery operation

#### 6.1.2 Recovery Environment Preparation

1. Identify appropriate recovery environment based on system requirements
2. Verify recovery environment readiness:
   - Sufficient storage capacity
   - Required network connectivity
   - Appropriate system access
   - Required software prerequisites
3. Isolate recovery environment if necessary to prevent production impact
4. Document recovery environment configuration

### 6.2 File and Folder Recovery

#### 6.2.1 Standard File Recovery Procedure

1. Identify specific files/folders to be recovered
2. Identify appropriate backup to restore from
3. Mount backup in read-only mode if possible
4. Locate requested files/folders in backup
5. Restore to requested location or temporary recovery location
6. Verify file integrity and permissions
7. Notify requestor of successful recovery
8. Document recovery details

#### 6.2.2 User Data Recovery Procedure

1. Verify recovery request is authorized
2. Identify appropriate backup to restore from
3. Mount backup in read-only mode if possible
4. Locate requested user data in backup
5. Restore to temporary recovery location
6. Verify file integrity and permissions
7. Provide restored data to user with appropriate access controls
8. Document recovery details

### 6.3 Server Recovery

#### 6.3.1 Windows Server Recovery Procedure

1. Prepare recovery environment according to Section 6.1.2
2. Boot recovery environment using appropriate media
3. Identify and mount appropriate backup
4. Execute server recovery process:
   - For bare-metal recovery, follow backup software's bare-metal recovery procedure
   - For VM recovery, restore VM configuration and disk images
5. Apply any necessary post-recovery configurations
6. Verify system startup and basic functionality
7. Verify network connectivity and services
8. Document recovery process and outcomes

#### 6.3.2 Linux Server Recovery Procedure

1. Prepare recovery environment according to Section 6.1.2
2. Boot recovery environment using appropriate media
3. Identify and mount appropriate backup
4. Execute server recovery process:
   - For bare-metal recovery, restore partition layout and system files
   - For VM recovery, restore VM configuration and disk images
5. Restore bootloader configuration
6. Apply any necessary post-recovery configurations
7. Verify system startup and basic functionality
8. Verify network connectivity and services
9. Document recovery process and outcomes

### 6.4 Database Recovery

#### 6.4.1 SQL Server Database Recovery Procedure

1. Prepare recovery environment according to Section 6.1.2
2. Identify appropriate backup files:
   - Full backup
   - Differential backups (if applicable)
   - Transaction log backups (if applicable)
3. Restore database to specified point in time:
   - Restore full backup with NORECOVERY option
   - Restore differential backup with NORECOVERY option (if applicable)
   - Restore transaction logs in sequence with NORECOVERY option (if applicable)
   - Restore final transaction log with RECOVERY option
4. Verify database consistency using DBCC CHECKDB
5. Verify data integrity through application-level validation
6. Apply any necessary post-recovery configurations
7. Document recovery process and outcomes

#### 6.4.2 PostgreSQL Database Recovery Procedure

1. Prepare recovery environment according to Section 6.1.2
2. Identify appropriate backup files:
   - Full backup
   - WAL archives (if applicable)
3. Create recovery.conf file with appropriate settings
4. Restore database to specified point in time:
   - Restore full backup
   - Place WAL archives in pg_wal directory (if applicable)
   - Set recovery_target_time in recovery.conf (if applicable)
5. Start database server to begin recovery process
6. Verify database consistency
7. Verify data integrity through application-level validation
8. Apply any necessary post-recovery configurations
9. Document recovery process and outcomes

#### 6.4.3 MongoDB Database Recovery Procedure

1. Prepare recovery environment according to Section 6.1.2
2. Identify appropriate backup files:
   - Full backup
   - Oplog entries (if applicable)
3. Restore database to specified point in time:
   - Restore full backup using mongorestore
   - Apply oplog entries up to specified point in time (if applicable)
4. Verify database consistency
5. Verify data integrity through application-level validation
6. Apply any necessary post-recovery configurations
7. Document recovery process and outcomes

### 6.5 Cloud Services Recovery

#### 6.5.1 AWS Recovery Procedure

1. Identify AWS resources to be recovered
2. Locate appropriate backups in AWS Backup or third-party solution
3. For EC2 instances:
   - Restore AMI or EBS volumes to new instances
   - Configure appropriate security groups and network settings
4. For RDS databases:
   - Restore to new instance
   - Configure appropriate security groups and network settings
5. For S3 data:
   - Restore from backup to original or alternate location
6. Verify recovered resources functionality
7. Update DNS or load balancer configurations if needed
8. Document recovery process and outcomes

#### 6.5.2 Azure Recovery Procedure

1. Identify Azure resources to be recovered
2. Locate appropriate backups in Azure Backup or third-party solution
3. For Azure VMs:
   - Restore VM to original or alternate location
   - Configure appropriate NSGs and network settings
4. For Azure SQL:
   - Restore to new instance
   - Configure appropriate security settings
5. For Azure Files/Blobs:
   - Restore from backup to original or alternate location
6. Verify recovered resources functionality
7. Update DNS or load balancer configurations if needed
8. Document recovery process and outcomes

#### 6.5.3 Google Cloud Recovery Procedure

1. Identify GCP resources to be recovered
2. Locate appropriate backups in Google Cloud Backup or third-party solution
3. For Compute Engine instances:
   - Restore from snapshot or backup to new instances
   - Configure appropriate firewall rules and network settings
4. For Cloud SQL:
   - Restore to new instance
   - Configure appropriate security settings
5. For Cloud Storage:
   - Restore from backup to original or alternate location
6. Verify recovered resources functionality
7. Update DNS or load balancer configurations if needed
8. Document recovery process and outcomes

### 6.6 SaaS Application Recovery

#### 6.6.1 Microsoft 365 Recovery Procedure

1. Identify specific M365 data to be recovered
2. Locate appropriate backup in M365 backup solution
3. Select specific items for recovery:
   - For Exchange: Specific emails, folders, or mailboxes
   - For SharePoint/OneDrive: Specific files, folders, or sites
   - For Teams: Specific teams, channels, or conversations
4. Select recovery destination (original location or alternate)
5. Execute recovery operation
6. Verify recovered data availability and integrity
7. Document recovery process and outcomes

#### 6.6.2 Salesforce Recovery Procedure

1. Identify specific Salesforce data to be recovered
2. Locate appropriate backup in Salesforce backup solution
3. Select specific items for recovery:
   - Specific objects
   - Specific records
   - Attachments or files
4. Select recovery destination (original location or alternate)
5. Execute recovery operation
6. Verify recovered data availability and integrity
7. Document recovery process and outcomes

## 7. Client-Specific Recovery Procedures

### 7.1 Client Recovery Request Management

1. Document client recovery request details:
   - Client name and contact information
   - System/data to be recovered
   - Reason for recovery
   - Required recovery point (date/time)
   - Required completion timeframe
2. Verify request authorization according to client agreement
3. Assign recovery to appropriate technical team
4. Establish communication plan with client

### 7.2 Client Environment Recovery Procedure

1. Retrieve client-specific recovery procedures from documentation
2. Review client-specific security and compliance requirements
3. Prepare recovery environment according to client specifications
4. Execute recovery according to client-specific procedures
5. Verify recovery according to client acceptance criteria
6. Provide recovery documentation to client as required
7. Update client documentation with any procedural improvements

## 8. Post-Recovery Procedures

### 8.1 Recovery Validation

#### 8.1.1 System Validation Procedure

1. Verify system boot and login functionality
2. Verify network connectivity and DNS resolution
3. Verify critical service functionality
4. Verify application functionality
5. Verify data integrity
6. Perform security validation checks
7. Document validation results

#### 8.1.2 Data Validation Procedure

1. Verify data completeness based on recovery point objectives
2. Perform sample data validation checks
3. Run data integrity reports if available
4. Verify application interaction with recovered data
5. Have business users validate critical data if appropriate
6. Document validation results

### 8.2 Post-Recovery Documentation

#### 8.2.1 Recovery Report Procedure

1. Document recovery details:
   - Systems/data recovered
   - Recovery point used
   - Recovery start and end times
   - Recovery team members involved
   - Recovery steps performed
   - Any issues encountered and resolutions
   - Validation results
2. Calculate actual recovery metrics:
   - Recovery Time Actual (RTA)
   - Recovery Point Actual (RPA)
3. Compare actual metrics to objectives (RTO/RPO)
4. Document any procedural improvements identified
5. Share report with appropriate stakeholders

#### 8.2.2 Lessons Learned Procedure

1. Schedule post-recovery review meeting
2. Review recovery process effectiveness
3. Identify areas for improvement
4. Document lessons learned
5. Update recovery procedures based on findings
6. Schedule follow-up actions as needed

## 9. Special Recovery Scenarios

### 9.1 Ransomware Recovery

#### 9.1.1 Ransomware Recovery Preparation

1. Isolate affected systems immediately
2. Report incident according to Incident Management Policy (POL-08)
3. Perform initial investigation to determine scope of infection
4. Identify clean recovery point prior to infection
5. Prepare clean recovery environment
6. Document recovery strategy and obtain approval

#### 9.1.2 Ransomware Recovery Procedure

1. Do not pay ransom without explicit executive approval and legal consultation
2. Use offline backups where possible to prevent backup encryption
3. Restore system to clean state using approved media
4. Restore data from verified clean backups
5. Apply security patches and hardening before reconnecting
6. Implement additional security controls as needed
7. Verify system is free from malware before reconnection
8. Document recovery process and outcomes

### 9.2 Corrupt Database Recovery

#### 9.2.1 Database Corruption Assessment

1. Identify type and extent of corruption
2. Attempt to determine root cause
3. Evaluate repair options:
   - Native database repair tools
   - Recovery from backup
   - Partial data extraction and repair
4. Document assessment and recommended approach
5. Obtain approval for recovery strategy

#### 9.2.2 Database Corruption Recovery Procedure

1. If viable, attempt database repair using native tools
2. If repair fails, restore from last known good backup
3. Apply transaction logs to reach point just before corruption
4. Verify database consistency and functionality
5. Document recovery process and outcomes
6. Implement preventive measures based on root cause

### 9.3 Cloud Service Outage Recovery

#### 9.3.1 Cloud Outage Assessment

1. Identify affected cloud services and dependent systems
2. Determine estimated outage duration from provider status
3. Evaluate recovery options:
   - Wait for provider restoration
   - Fail over to alternate region
   - Activate on-premises contingency if available
4. Document assessment and recommended approach
5. Obtain approval for recovery strategy

#### 9.3.2 Cloud Outage Recovery Procedure

1. Implement approved recovery strategy
2. For region failover:
   - Activate resources in alternate region
   - Update DNS or routing configurations
   - Verify functionality in alternate region
3. For on-premises contingency:
   - Activate on-premises systems
   - Restore data from most recent backup
   - Update DNS or routing configurations
4. Communicate status to affected users
5. Monitor provider status for primary service restoration
6. Plan return to primary service when available
7. Document recovery process and outcomes

## 10. Backup Infrastructure Management

### 10.1 Backup System Maintenance

#### 10.1.1 Backup Software Updates

1. Review vendor release notes for backup software updates
2. Test updates in non-production environment
3. Schedule maintenance window for update
4. Create pre-update backup of backup system configuration
5. Apply updates according to vendor recommendations
6. Verify backup system functionality post-update
7. Verify backup job functionality post-update
8. Document update process and outcomes

#### 10.1.2 Backup Storage Maintenance

1. Monitor backup storage capacity weekly
2. Maintain minimum 30% free space on backup storage
3. Archive or purge expired backups according to retention policy
4. Perform storage system health checks monthly
5. Apply storage system updates quarterly
6. Document maintenance activities

### 10.2 Backup Security Management

#### 10.2.1 Backup Access Control

1. Review backup system access quarterly
2. Implement least privilege access model
3. Require multi-factor authentication for backup system administration
4. Maintain separation of duties for backup administration
5. Document access control configuration

#### 10.2.2 Backup Encryption Management

1. Implement encryption for all backup data
2. Securely manage encryption keys according to the Cryptographic Controls Procedure (DOC-17)
3. Test backup encryption quarterly
4. Rotate encryption keys annually
5. Document encryption configuration and key management

## 11. Documentation and Training

### 11.1 Backup and Recovery Documentation

#### 11.1.1 Documentation Requirements

The following documentation must be maintained:

1. System-specific backup configurations
2. Backup schedules and retention settings
3. Recovery procedures for each major system
4. Backup verification and testing results
5. Recovery test results
6. Client-specific backup and recovery procedures

#### 11.1.2 Documentation Review Procedure

1. Review all backup and recovery documentation quarterly
2. Update documentation to reflect system changes
3. Verify documentation accuracy during recovery testing
4. Maintain version control for all documentation
5. Ensure documentation is accessible during disruptions

### 11.2 Staff Training

#### 11.2.1 Training Requirements

1. All IT operations staff must receive backup and recovery training
2. Training must include:
   - Backup system operation
   - Recovery procedures for assigned systems
   - Backup verification procedures
   - Recovery testing procedures
   - Incident response for backup failures
3. Training must be refreshed annually
4. New IT operations staff must receive training during onboarding

#### 11.2.2 Training Documentation

1. Document training materials and procedures
2. Maintain training records for all staff
3. Update training materials when procedures change
4. Perform knowledge verification after training
5. Document staff system recovery competencies

## 12. Related Documents

- POL-01: Information Security Policy
- POL-06: Backup Policy
- DOC-09: Business Continuity Plan
- POL-08: Incident Management Policy
- DOC-17: Cryptographic Controls Procedure
- DOC-41: System Restoration Checklist
- DOC-42: Recovery Test Plan Template

---

_By working for Enablis, you acknowledge that you have read, understood, and agree to comply with these Backup and Recovery Procedures._
