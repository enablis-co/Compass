---
layout: page
title: "Access Control & Identity Management Policy"
permalink: /policies/isms-pol-03/
---

**Document ID**: ISMS-POL-03  
**Version**: 1.0  
**Last Updated**: February 25, 2025  
**Owner**: Chief Technology Officer  
**Approved by**: Board of Directors

## 1. Purpose and Scope

### 1.1 Purpose

This Access Control & Identity Management Policy establishes the requirements for managing access to Enablis systems, applications, and information assets. It ensures appropriate protection through effective authentication, authorization, and accountability measures while supporting operational efficiency and business agility.

### 1.2 Scope

This policy applies to:

- All information systems, applications, and environments owned or managed by Enablis
- All employees, contractors, and temporary staff of Enablis
- Client systems accessed or managed by Enablis personnel
- All cloud services and third-party applications used for business purposes
- All locations from which Enablis business is conducted, including remote environments

## 2. Access Control Principles

Enablis applies these core principles to our access control approach:

### 2.1 Least Privilege

Access rights are granted according to the minimum level required for users to fulfill their job responsibilities. This reduces risk exposure while maintaining operational effectiveness.

### 2.2 Need-to-Know

Access to information is provided only to those who require it for legitimate business purposes, limiting information exposure.

### 2.3 Zero Trust

We operate under the principle that threats may exist both outside and inside our network, requiring verification of all access regardless of source.

### 2.4 Separation of Duties

Critical functions are divided among multiple individuals where practical to prevent conflicts of interest and reduce fraud risk.

### 2.5 Default Denial

All access is denied by default and only permitted when explicitly authorized, configured, and approved.

### 2.6 Usability Balance

Security controls should balance protection with usability, avoiding unnecessary friction that might lead to workarounds.

## 3. Identity Management

### 3.1 User Identity Creation

#### 3.1.1 Unique Identifiers

- Each user must be assigned a unique identifier for access to Enablis systems
- Shared accounts are prohibited except for documented business-critical exceptions
- Service accounts must be used only for system-to-system interactions

#### 3.1.2 Identity Verification

- User identity must be verified before account creation
- Verification must be performed by authorized personnel
- Documentation of verification must be maintained

#### 3.1.3 Account Request and Approval

- Access requests must be submitted and approved through the designated process
- Approvals must be documented and retained
- Provisioning must be performed only after appropriate approval

### 3.2 Identity Lifecycle Management

#### 3.2.1 Onboarding

- Account provisioning must be part of the formal onboarding process
- Initial access rights must be based on role requirements
- Temporary credentials must be changed on first use

#### 3.2.2 Changes in Role or Responsibility

- Access rights must be reviewed when users change roles
- Unnecessary access must be removed promptly
- New access must be requested and approved through the standard process

#### 3.2.3 Extended Absence

- Access may be temporarily suspended during extended absence
- Reactivation must verify continued need for access
- Critical systems may require re-authorization

#### 3.2.4 Offboarding

- Access revocation must be part of the formal offboarding process
- Access must be revoked within 24 hours of termination
- Access revocation must be documented and verified

### 3.3 Federated Identity

#### 3.3.1 Single Sign-On (SSO)

- SSO should be implemented where practical to reduce authentication friction
- SSO implementations must maintain appropriate security controls
- Authentication security must not be compromised for convenience

#### 3.3.2 External Identity Providers

- External identity providers must be assessed for security
- Federation agreements must define security requirements
- Authentication strength must be appropriate to the access provided

## 4. Authentication

### 4.1 Authentication Methods

#### 4.1.1 Passwords

- Password creation, management, and complexity must follow the requirements in Section 5
- Password authentication alone is insufficient for access to sensitive systems
- Password managers are recommended for generating and storing complex passwords

#### 4.1.2 Multi-Factor Authentication (MFA)

- MFA is required for:
  - Remote access to Enablis networks and systems
  - Access to systems storing confidential information
  - Administrative access to critical systems
  - Cloud service administrative accounts
  - Client systems where supported
- Approved MFA methods include:
  - Time-based One-Time Password (TOTP) applications
  - Hardware security keys
  - Push notifications to registered mobile devices
  - Biometric authentication (where appropriate)

#### 4.1.3 Certificates and Keys

- Certificate-based authentication should be used where appropriate
- SSH keys must be managed securely
- Key-based authentication must follow secure key management practices

### 4.2 Authentication Security

#### 4.2.1 Authentication Attempts

- Failed authentication attempts should be limited to prevent brute-force attacks
- Accounts should be temporarily locked after multiple failed attempts
- Failed authentication attempts should be logged and monitored

#### 4.2.2 Session Management

- Authenticated sessions must have appropriate timeouts
- Sessions must be terminated after a period of inactivity
- Users must be able to terminate active sessions
- Concurrent sessions may be limited where appropriate

## 5. Password Requirements

### 5.1 Password Complexity

- Minimum length: 12 characters
- Should contain a mix of different character types
- Should not contain easily guessable information
- Should not be a commonly used password

### 5.2 Password Management

- Initial passwords must be changed on first use
- Passwords must not be shared
- Passwords must not be stored in unsecured locations
- Password reuse should be prevented

### 5.3 Password Changes

- Password changes should be required if:
  - There is suspicion of compromise
  - After a security incident
  - When changing roles with different access levels
- Regular password expiration is not required if:
  - Strong passwords are used
  - MFA is implemented
  - No indication of compromise exists

### 5.4 Password Storage

- Passwords must be stored using strong, modern hashing algorithms
- Plain text storage of passwords is prohibited
- Password hashes must be salted and stretched

## 6. Authorization and Access Control

### 6.1 Role-Based Access Control (RBAC)

#### 6.1.1 Role Definition

- Access roles must be defined based on job functions
- Roles must be documented and regularly reviewed
- Role permissions must follow least privilege principles

#### 6.1.2 Role Assignment

- Users should be assigned to appropriate roles
- Role assignments must be approved by managers
- Multiple role assignments should be reviewed for potential conflicts

#### 6.1.3 Role Review

- Role definitions must be reviewed annually
- Unnecessary permissions should be removed from roles
- Role assignments must be verified during access reviews

### 6.2 Access Approval Process

#### 6.2.1 Standard Access

- Standard access based on job roles should be pre-approved
- Access templates should be used for common role types
- Deviations from standard access must be specifically justified and approved

#### 6.2.2 Elevated Access

- Elevated access must have additional approval requirements
- Business justification must be documented
- Time limitations should be applied where appropriate

#### 6.2.3 Emergency Access

- Emergency access procedures must be established
- Emergency access must be time-limited
- Emergency access must be monitored and documented
- Normal approval processes must be followed retrospectively

### 6.3 Privileged Access Management

#### 6.3.1 Privileged Accounts

- Privileged accounts must be strictly controlled
- Privilege elevation should be used instead of separate privileged accounts where possible
- Privileged account usage must be logged and monitored

#### 6.3.2 Just-in-Time Access

- Just-in-time privileged access should be implemented where possible
- Privilege elevation should be time-limited
- Re-authentication should be required for privilege elevation

#### 6.3.3 Administrative Access

- Administrative access must be restricted to authorized personnel
- Administrative activities must be performed using dedicated accounts
- Administrative sessions must be recorded where appropriate

### 6.4 Access Reviews

#### 6.4.1 Review Frequency

- User access rights must be reviewed:
  - Every 90 days for highly privileged accounts
  - Every 180 days for standard accounts
  - Upon significant organizational changes
  - After major system changes

#### 6.4.2 Review Responsibility

- Managers are responsible for reviewing access of their direct reports
- System owners are responsible for reviewing system access
- The Security Manager is responsible for overseeing the review process

#### 6.4.3 Review Documentation

- Access reviews must be documented
- Review results must be retained for audit purposes
- Identified issues must be addressed promptly

## 7. Remote Access

### 7.1 Remote Access Methods

- Remote access must use secure, encrypted connections
- VPN or equivalent secure access solutions must be used
- Remote sessions to critical systems should be monitored

### 7.2 Remote Access Security

- MFA is mandatory for all remote access
- Remote access must be logged and monitored
- Inactive remote sessions must be automatically terminated
- Split tunneling should be controlled based on risk

### 7.3 Personal Devices (BYOD)

- Personal devices used for business purposes must:
  - Meet minimum security requirements
  - Be enrolled in device management where appropriate
  - Maintain separation between business and personal data
  - Adhere to the Remote Working Policy

## 8. Cloud Access Security

### 8.1 Cloud Service Authentication

- Cloud services must use strong authentication
- MFA must be enabled for all cloud service accounts
- Administrative access to cloud services requires MFA
- SSO should be implemented for cloud services where supported

### 8.2 Cloud Authorization Controls

- Cloud access must follow least privilege principles
- Access to cloud resources must be based on defined roles
- Permissions must be regularly reviewed and refined
- Broad permissions should be avoided in favor of specific grants

### 8.3 Cloud Identity Governance

- Cloud identities must be integrated with identity lifecycle management
- Centralized identity governance should be implemented
- Cloud identity configurations must be regularly audited
- Automated deprovisioning should be implemented where possible

## 9. Client System Access

### 9.1 Client-Specific Requirements

- Access to client systems must comply with client security policies
- Client-specific access requirements must be documented
- Exceptions to standard practices must be approved and documented

### 9.2 Client Credential Management

- Client credentials must be securely stored
- Shared client credentials must be avoided
- Client credential rotation must follow client requirements
- Client access must be promptly revoked when no longer needed

### 9.3 Client System Authentication

- Authentication to client systems must use strongest available methods
- MFA should be used where supported by client systems
- Client system sessions must be terminated when not in use
- Authentication to client systems must be logged

## 10. Physical Access Control

### 10.1 Facility Access

- Physical access to Enablis facilities must be controlled
- Access cards or keys must be issued to authorized personnel
- Visitor access must be logged and supervised
- Physical access rights must be promptly revoked when no longer needed

### 10.2 Secure Areas

- Critical infrastructure must be located in secure areas
- Secure area access must be restricted to authorized personnel
- Secure area access must be logged
- Regular reviews of physical access rights must be conducted

## 11. Monitoring and Logging

### 11.1 Authentication Logging

- Authentication attempts must be logged, including:
  - Successful and failed authentication
  - Account lockouts
  - Password changes
  - Privilege changes

### 11.2 Access Activity Monitoring

- User activities must be logged appropriate to the sensitivity of the system
- Privileged user activities must be monitored
- Anomalous access patterns must be detected and investigated
- Access to logs must be restricted and monitored

### 11.3 Log Management

- Logs must be protected from unauthorized access and modification
- Logs must be retained in accordance with retention requirements
- Log review procedures must be established
- Log correlation tools should be employed to identify potential security issues

## 12. Access-Related Incident Management

### 12.1 Authentication Failures

- Multiple authentication failures must be investigated
- Account lockouts must be responded to according to defined procedures
- Credential compromise must be treated as a security incident

### 12.2 Unauthorized Access

- Signs of unauthorized access must be promptly investigated
- Incident response procedures must be followed
- Affected systems must be secured
- Root causes must be identified and addressed

### 12.3 Post-Incident Actions

- Compromised credentials must be changed
- Access rights must be reviewed following security incidents
- Authentication systems must be assessed for vulnerabilities
- Improvements must be implemented to prevent recurrence

## 13. Access Control in Development

### 13.1 Development Environment Access

- Development environments must have appropriate access controls
- Production credentials must not be used in development
- Development environment access must be limited to authorized developers
- Separation between development, testing, and production environments must be maintained

### 13.2 Source Code Access

- Source code access must be restricted to authorized personnel
- Code repositories must use appropriate access controls
- Code changes must be reviewed before acceptance
- Administrative access to code repositories must be limited

### 13.3 Deployment Access

- Application deployment capabilities must be restricted
- Deployment to production must follow appropriate approval processes
- Deployment credentials must be tightly controlled
- Deployment activities must be logged and auditable

## 14. Technical Implementation Guidance

### 14.1 Identity Providers

- Centralized identity management should be implemented
- Directory services must be secured according to best practices
- Identity provider redundancy should be considered for critical systems

### 14.2 Authentication Systems

- Authentication systems must be hardened according to best practices
- Authentication services must be highly available
- Authentication system changes must follow change management procedures

### 14.3 Authorization Systems

- Authorization systems must enforce defined policies
- Authorization decisions should be centralized where possible
- Authorization systems must be regularly tested

## 15. Exceptions

Exceptions to this policy may be granted only after a documented risk assessment and formal approval by the Security Manager or CTO. All exceptions must be:

- Documented using the Security Exception Request Form (ISMS-FORM-05)
- Time-limited with a defined expiration date
- Reviewed periodically for continued necessity
- Accompanied by compensating controls where appropriate

## 16. Responsibilities

### 16.1 All Staff

- Protect authentication credentials
- Report suspected security issues
- Follow access control procedures
- Access only systems they are authorized to use

### 16.2 Managers

- Review and approve access requests for their team members
- Participate in regular access reviews
- Ensure staff understand their access control responsibilities
- Promptly report personnel changes affecting access requirements

### 16.3 IT and Security Teams

- Implement and maintain access control systems
- Process access requests according to policy
- Monitor access control effectiveness
- Investigate access-related security events

### 16.4 System Owners

- Define access requirements for their systems
- Approve access to their systems
- Regularly review access to their systems
- Implement appropriate access controls

## 17. Policy Review

This policy will be reviewed annually or when significant changes occur to ensure it remains aligned with business requirements, security best practices, and regulatory obligations.

## 18. Related Documents

- [Information Security Management Policy]({{ site.baseurl }}/policies/isms-pol-01/)
- [Data Protection & Classification Policy]({{ site.baseurl }}/policies/isms-pol-02/)
- [Incident Management Policy]({{ site.baseurl }}/policies/isms-pol-04/)
- [Asset Management Procedure]({{ site.baseurl }}/procedures/isms-proc-04/)
- ISMS-FORM-05: Security Exception Request Form

---

_By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Access Control & Identity Management Policy._
