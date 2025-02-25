---
layout: document
title: "Asset Management Procedure"
permalink: /procedures/isms-proc-04/
---

# Enablis Asset Management Procedure

**Document ID**: ISMS-PROC-04  
**Version**: 1.0  
**Last Updated**: February 25, 2025  
**Owner**: Chief Technology Officer  
**Approved by**: Board of Directors

## 1. Purpose and Scope

### 1.1 Purpose

This Asset Management Procedure establishes the requirements for identifying, recording, and managing information assets throughout their lifecycle at Enablis. It ensures that assets are properly tracked, protected, and maintained to support business operations and security requirements.

### 1.2 Scope

This procedure applies to:

- All information assets owned or used by Enablis
- All hardware, software, data, and supporting assets
- All employees, contractors, and temporary staff responsible for managing assets
- All locations where Enablis assets are stored or used, including remote environments
- Client assets managed by Enablis where contractually responsible

## 2. Asset Categories and Classification

### 2.1 Asset Categories

Enablis assets are categorized as follows:

#### 2.1.1 Hardware Assets

- Endpoint devices (laptops, desktops, tablets, smartphones)
- Servers (physical and virtual)
- Network equipment (routers, switches, firewalls, access points)
- Peripherals (printers, scanners, external drives)
- IoT devices and specialized equipment

#### 2.1.2 Software Assets

- Operating systems
- Commercial applications
- Open source software
- Custom-developed applications
- Cloud services and subscriptions
- Development tools and platforms

#### 2.1.3 Data Assets

- Business data (financial, operational, HR)
- Client data
- Intellectual property
- Configuration data
- Backup data

#### 2.1.4 Supporting Assets

- Documentation
- System configurations
- Encryption keys and certificates
- Authentication systems
- Physical security systems

### 2.2 Asset Classification

#### 2.2.1 Classification Criteria

Assets are classified based on:

- Confidentiality requirements
- Integrity requirements
- Availability requirements
- Business value
- Regulatory requirements

#### 2.2.2 Classification Levels

Assets are assigned one of the following classification levels aligned with the Data Protection & Classification Policy (ISMS-POL-02):

| Classification   | Description                                                  | Asset Examples                                                                                |
| ---------------- | ------------------------------------------------------------ | --------------------------------------------------------------------------------------------- |
| **Public**       | Assets containing information approved for public disclosure | - Marketing materials<br>- Public website infrastructure<br>- Open source contributions       |
| **Internal**     | Assets for internal use with minimal risk if disclosed       | - Internal documentation<br>- Development tools<br>- General business systems                 |
| **Confidential** | Sensitive assets requiring protection                        | - Client project systems<br>- Financial systems<br>- HR systems<br>- Source code repositories |

## 3. Asset Management Roles and Responsibilities

### 3.1 Primary Roles

#### 3.1.1 IT Operations Manager

- Overall responsibility for asset management
- Approval of asset management procedures
- Resource allocation for asset management
- Reporting on asset management effectiveness

#### 3.1.2 Asset Manager

- Day-to-day management of asset inventory
- Administration of asset management tools
- Asset tracking and reporting
- Coordination of asset management activities

#### 3.1.3 Asset Owners

- Accountability for specific assets or asset groups
- Classification of assets
- Approval of access rights
- Risk acceptance for their assets

#### 3.1.4 Asset Custodians

- Implementation of security controls
- Day-to-day protection of assets
- Reporting of security incidents
- Maintenance of assigned assets

### 3.2 Supporting Roles

#### 3.2.1 Security Manager

- Security requirements for assets
- Security control validation
- Security incident management
- Security awareness related to assets

#### 3.2.2 Procurement Manager

- Asset acquisition
- Vendor management
- License management
- Asset retirement coordination

#### 3.2.3 All Staff

- Proper use of assigned assets
- Protection of assets under their control
- Reporting asset issues or incidents
- Compliance with asset management requirements

## 4. Asset Lifecycle Management

### 4.1 Asset Planning and Acquisition

#### 4.1.1 Needs Assessment

- Identify business requirements for new assets
- Evaluate security requirements
- Consider compatibility with existing assets
- Determine support and maintenance requirements
- Document justification for acquisition

#### 4.1.2 Procurement Process

- Follow established procurement procedures
- Include security requirements in specifications
- Evaluate vendor security practices
- Review license terms and conditions
- Maintain procurement documentation

#### 4.1.3 Pre-deployment Testing

- Verify asset functionality
- Test security configurations
- Validate compatibility
- Document baseline configuration
- Prepare deployment plan

### 4.2 Asset Deployment

#### 4.2.1 Asset Registration

- Record asset in inventory system
- Assign unique identifier
- Document asset details (model, serial number, specifications)
- Assign owner and custodian
- Apply asset tagging where applicable

#### 4.2.2 Secure Configuration

- Apply security baseline configuration
- Install required security controls
- Apply patches and updates
- Remove unnecessary features or services
- Document applied configuration

#### 4.2.3 Access Control Setup

- Configure appropriate access rights
- Implement authentication requirements
- Apply authorization controls
- Document access control configuration
- Verify access control effectiveness

### 4.3 Asset Operation and Maintenance

#### 4.3.1 Routine Maintenance

- Apply updates and patches
- Perform preventive maintenance
- Monitor asset health and performance
- Maintain asset documentation
- Schedule maintenance activities

#### 4.3.2 Change Management

- Follow established change management procedures
- Document changes to asset configuration
- Test changes before implementation
- Update asset inventory after changes
- Review security impact of changes

#### 4.3.3 Asset Monitoring

- Monitor asset availability
- Track asset performance
- Detect security issues
- Identify unauthorized changes
- Generate alerts for abnormal conditions

### 4.4 Asset Transfer and Reassignment

#### 4.4.1 Internal Transfer Process

- Update asset inventory
- Remove previous user access
- Sanitize sensitive data if needed
- Reconfigure for new use
- Document transfer details

#### 4.4.2 Temporary Assignment

- Record temporary custodian
- Define return date
- Clarify responsibilities
- Monitor compliance with return schedule
- Verify asset condition upon return

### 4.5 Asset Retirement and Disposal

#### 4.5.1 Retirement Decision

- Assess end-of-life criteria
- Evaluate continued value
- Consider security implications
- Document retirement justification
- Obtain appropriate approval

#### 4.5.2 Data Sanitization

- Identify media containing data
- Select appropriate sanitization method based on classification
- Verify sanitization effectiveness
- Document sanitization process
- Maintain sanitization records

#### 4.5.3 Disposal Methods

- Select disposal method based on asset type
- Follow environmental regulations
- Use authorized disposal vendors
- Obtain disposal certificates where applicable
- Update asset inventory after disposal

## 5. Asset Inventory Management

### 5.1 Asset Inventory System

#### 5.1.1 Inventory Requirements

The asset inventory system must:

- Support unique identification of assets
- Allow recording of asset details
- Track asset status and location
- Support asset relationships and dependencies
- Enable reporting and analysis

#### 5.1.2 Minimum Asset Information

The following information must be recorded for each asset:

- Unique identifier
- Asset type and category
- Manufacturer and model
- Serial number or other unique identifiers
- Location
- Owner and custodian
- Classification
- Purchase date and cost
- Support and warranty information
- End-of-life date
- Current status

#### 5.1.3 Inventory Updates

The asset inventory must be updated:

- When new assets are acquired
- When assets are reassigned
- After significant configuration changes
- When asset status changes
- When assets are retired or disposed

### 5.2 Asset Discovery and Validation

#### 5.2.1 Automated Discovery

- Implement automated discovery tools where appropriate
- Schedule regular discovery scans
- Compare discovered assets with inventory
- Investigate discrepancies
- Update inventory based on findings

#### 5.2.2 Physical Verification

- Conduct periodic physical inventories
- Verify asset location and condition
- Validate asset tags and identifiers
- Document verification results
- Address discrepancies

#### 5.2.3 Reconciliation Process

- Compare physical and automated inventory results
- Identify missing assets
- Investigate discrepancies
- Update inventory records
- Report significant issues

### 5.3 Software Asset Management

#### 5.3.1 License Management

- Track software licenses
- Monitor license compliance
- Manage license renewals
- Optimize license utilization
- Document license terms and conditions

#### 5.3.2 Software Inventory

- Maintain inventory of installed software
- Track software versions
- Record installation locations
- Monitor unauthorized software
- Update inventory after software changes

#### 5.3.3 Cloud Service Management

- Maintain inventory of cloud services
- Track service subscriptions and costs
- Monitor cloud resource utilization
- Manage cloud service access
- Review cloud service security

## 6. Mobile Asset Management

### 6.1 Mobile Device Management

#### 6.1.1 Mobile Device Registration

- Register all mobile devices in inventory
- Deploy mobile device management (MDM) solutions
- Document device assignment
- Record device specifications
- Track device status

#### 6.1.2 Mobile Device Security

- Implement mobile security policies
- Configure encryption
- Enforce authentication requirements
- Enable remote wipe capability
- Install security applications

#### 6.1.3 Mobile Device Monitoring

- Track device location where appropriate
- Monitor security compliance
- Detect jailbreaking or rooting
- Alert on policy violations
- Generate usage reports

### 6.2 Remote Worker Asset Management

#### 6.2.1 Remote Asset Tracking

- Maintain inventory of remote assets
- Document home office locations
- Periodically verify remote assets
- Track asset movements
- Update inventory for location changes

#### 6.2.2 Remote Asset Security

- Implement security controls for remote assets
- Verify security compliance
- Provide secure connectivity
- Enforce encryption requirements
- Establish remote support procedures

## 7. Client Asset Management

### 7.1 Client-Owned Asset Management

#### 7.1.1 Asset Responsibility Definition

- Clearly define responsibility for client assets
- Document in service agreements
- Specify security responsibilities
- Determine incident response procedures
- Establish asset return procedures

#### 7.1.2 Client Asset Inventory

- Maintain separate inventory of client assets
- Record client ownership information
- Document asset purpose and project association
- Track asset location and status
- Update inventory as required by client

#### 7.1.3 Client Asset Security

- Apply security controls as specified by client
- Follow client security policies
- Document security implementations
- Report security issues according to client requirements
- Verify security compliance

### 7.2 Enablis-Managed Client Assets

#### 7.2.1 Client Environment Assets

- Inventory assets in client environments
- Document asset ownership and responsibilities
- Track assets by client project
- Maintain asset status information
- Record support and maintenance details

#### 7.2.2 Client Project Asset Handling

- Assign project-specific assets
- Track asset allocation to projects
- Return or reassign assets upon project completion
- Document asset chain of custody
- Follow client-specific asset procedures

## 8. Asset Security Requirements

### 8.1 Security Controls by Asset Type

#### 8.1.1 Endpoint Device Security

- Encryption requirements
- Authentication controls
- Endpoint protection solutions
- Patch management
- Configuration standards

#### 8.1.2 Server Security

- Hardening standards
- Access control requirements
- Monitoring solutions
- Backup requirements
- Update management

#### 8.1.3 Network Device Security

- Configuration standards
- Access control requirements
- Monitoring and logging
- Update management
- Secure administration

#### 8.1.4 Software Security

- Update requirements
- Configuration guidelines
- Authentication requirements
- Authorization controls
- Logging standards

### 8.2 Security Control Validation

#### 8.2.1 Compliance Checking

- Verify security control implementation
- Assess compliance with security standards
- Identify security gaps
- Document compliance status
- Report non-compliance

#### 8.2.2 Vulnerability Assessment

- Conduct regular vulnerability scans
- Prioritize vulnerabilities based on risk
- Remediate identified vulnerabilities
- Verify remediation effectiveness
- Document vulnerability status

## 9. Asset Documentation

### 9.1 Documentation Requirements

#### 9.1.1 Asset Documentation Types

- Technical specifications
- User manuals and guides
- Configuration documentation
- Security documentation
- Support and maintenance procedures

#### 9.1.2 Documentation Management

- Store documentation securely
- Maintain documentation currency
- Control documentation access
- Version control documentation
- Archive outdated documentation

### 9.2 Documentation Updates

#### 9.2.1 Change Documentation

- Update documentation after changes
- Document configuration modifications
- Record security control changes
- Update diagrams and schematics
- Maintain change history

#### 9.2.2 Documentation Review

- Periodically review documentation
- Verify documentation accuracy
- Identify documentation gaps
- Update as required
- Archive obsolete documentation

## 10. Asset Management Reporting

### 10.1 Operational Reporting

#### 10.1.1 Inventory Reports

- Current asset inventory
- Asset allocation by department
- Asset status reports
- End-of-life forecasts
- License compliance

#### 10.1.2 Performance Reports

- Asset utilization
- Asset health metrics
- Support and maintenance activities
- Asset-related incidents
- Asset availability

### 10.2 Management Reporting

#### 10.2.1 Strategic Reports

- Asset lifecycle status
- Technology refresh plans
- Asset investment analysis
- Asset management effectiveness
- Asset risk status

#### 10.2.2 Compliance Reports

- Security compliance status
- Regulatory compliance
- License compliance
- Policy compliance
- Audit findings and remediation

## 11. Asset Management Audit and Improvement

### 11.1 Asset Management Audit

#### 11.1.1 Internal Audit

- Periodic audit of asset inventory
- Verification of physical assets
- Review of asset documentation
- Assessment of process compliance
- Validation of security controls

#### 11.1.2 External Audit

- Independent validation of asset inventory
- Compliance assessment
- Control effectiveness evaluation
- Security assessment
- Recommendations for improvement

### 11.2 Continuous Improvement

#### 11.2.1 Process Improvement

- Identify improvement opportunities
- Implement process enhancements
- Update procedures as needed
- Automate manual processes where possible
- Monitor effectiveness of improvements

#### 11.2.2 Tool Enhancement

- Evaluate asset management tools
- Identify tool limitations
- Implement tool improvements
- Integrate with other systems
- Optimize tool configuration

## 12. Exceptions

Exceptions to this procedure may be granted only after a documented risk assessment and formal approval by the IT Operations Manager or CTO. All exceptions must be:

- Documented using the Security Exception Request Form (ISMS-FORM-05)
- Time-limited with a defined expiration date
- Reviewed periodically for continued necessity
- Accompanied by compensating controls where appropriate

## 13. Procedure Review

This procedure will be reviewed annually or when significant changes occur to ensure it remains effective and aligned with business requirements.

## 14. Related Documents

- ISMS-POL-01: Information Security Management Policy
- ISMS-POL-02: Data Protection & Classification Policy
- ISMS-POL-03: Access Control & Identity Management Policy
- ISMS-FORM-05: Security Exception Request Form
- ISMS-FORM-11: Asset Management Form

---

_By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Asset Management Procedure._
