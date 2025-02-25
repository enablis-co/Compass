# Enablis Access Control Policy

**Document ID**: POL-04  
**Version**: 1.0  
**Last Updated**: February 24, 2025  
**Owner**: Security Manager  
**Approved by**: Chief Technology Officer

## 1. Purpose and Scope

### 1.1 Purpose

This Access Control Policy establishes the requirements for controlling access to Enablis information systems, applications, data, and facilities. It ensures that access rights are granted according to business requirements while maintaining appropriate security controls.

### 1.2 Scope

This policy applies to:

- All employees, contractors, and temporary staff of Enablis
- All information systems, applications, and data owned or managed by Enablis
- Client systems accessed or managed by Enablis personnel
- All physical locations and facilities operated by Enablis
- Remote access to Enablis networks and resources

## 2. Access Control Principles

### 2.1 Least Privilege

Access rights shall be granted based on the principle of least privilege, providing users with only the minimum access necessary to perform their job functions.

### 2.2 Need-to-Know

Access to information shall be granted only when there is a legitimate business need to access that information.

### 2.3 Segregation of Duties

Responsibilities and associated access rights shall be divided among different individuals where possible to reduce the risk of accidental or deliberate system misuse.

### 2.4 Default Denial

Access control systems shall follow the principle of "default denial," where access is denied unless explicitly granted.

### 2.5 Regular Review

Access rights shall be reviewed regularly to ensure they remain appropriate as roles and responsibilities change.

## 3. User Access Management

### 3.1 User Registration and Deregistration

#### 3.1.1 New User Access

- Access requests must be submitted by authorized personnel using the Access Request Form (FORM-01)
- All access requests must be approved by the relevant manager or data owner
- User accounts must be created with a unique identifier for each individual
- Initial access rights must align with job requirements and business needs

#### 3.1.2 User Deregistration

- Upon termination, all user access rights must be revoked within 24 hours
- For voluntary departures, access rights must be reviewed and adjusted during the notice period
- Managers must notify the IT department promptly of any staff changes affecting access requirements
- The offboarding process must include verification that all access has been revoked

### 3.2 Privilege Management

#### 3.2.1 Privileged Access Rights

- Privileged access rights (e.g., system administration) must be allocated only when required for specific job functions
- Privileged accounts must be separate from regular user accounts
- Privileged access must be granted for limited periods and regularly reviewed
- All privileged account activities must be logged and monitored

#### 3.2.2 Temporary and Emergency Access

- Temporary access must have a defined expiration date
- Emergency access must follow documented procedures and require senior management approval
- All temporary and emergency access must be reviewed and revoked when no longer required

### 3.3 Access Reviews

#### 3.3.1 Regular Reviews

- Manager reviews of user access rights must occur quarterly
- Privileged access rights must be reviewed monthly
- System and service accounts must be reviewed quarterly
- Client system access must be reviewed at intervals specified in client agreements

#### 3.3.2 Review Documentation

- Access reviews must be documented, including confirmation of appropriate access or changes made
- Review results must be retained for audit purposes
- Anomalies identified during reviews must be investigated and addressed

## 4. User Responsibilities

### 4.1 Password Management

Users must follow the Password Policy (POL-03) for managing authentication credentials.

### 4.2 Unattended Equipment

Users must:

- Lock their screens or log off when leaving workstations unattended
- Terminate active sessions when no longer required
- Secure mobile devices when not in use

### 4.3 Clean Desk

Users must:

- Secure physical documents and removable media when not in use
- Clear sensitive information from desks at the end of each workday
- Ensure sensitive information is not visible to unauthorized individuals

## 5. Network Access Control

### 5.1 Network Segmentation

- Internal networks shall be segmented based on security requirements and business functions
- Production environments shall be separated from development and testing environments
- Client environments shall be segregated from each other and from Enablis corporate networks

### 5.2 Remote Access

- Remote access to Enablis networks and systems must use secure, encrypted connections (e.g., VPN)
- Multi-factor authentication is mandatory for all remote access
- Remote access sessions must automatically time out after a period of inactivity
- Remote access must comply with the Remote Working Policy (POL-11)

### 5.3 Wireless Network Access

- Wireless networks must use strong encryption (WPA2/WPA3 Enterprise or better)
- Corporate and guest wireless networks must be segregated
- Guest wireless access must be time-limited and restricted from accessing internal resources

## 6. Application and Information Access Control

### 6.1 Application Access Control

- Applications must authenticate users using secure methods
- Applications must restrict functionality based on user roles and permissions
- Application access controls must be documented and regularly tested
- Access to application source code must be strictly controlled

### 6.2 Information Access Restriction

- Information must be classified according to the Information Classification Scheme (DOC-12)
- Access controls must be aligned with information classification levels
- Sensitive information must have additional controls, such as encryption
- Access to production data for development or testing purposes must be restricted and controlled

## 7. Cloud and Third-Party Access Control

### 7.1 Cloud Service Access

- Cloud service access must follow the same principles as internal systems
- Identity and access management solutions should be integrated across cloud platforms where possible
- Cloud service provider access to Enablis data must be restricted and monitored
- Cloud security configurations must be regularly reviewed and validated

### 7.2 Third-Party Access

- Third-party access must be limited to specific systems and information required
- All third-party access must be documented and approved
- Third-party connections must be monitored and periodically reviewed
- Third-party access must be promptly revoked when no longer required

## 8. Client Environment Access Control

### 8.1 Client Access Requirements

- Access to client environments must comply with both Enablis and client access control policies
- Client-specific access control requirements must be documented and communicated to relevant staff
- Access to client systems must be limited to staff directly involved in client projects
- Client environment access credentials must not be shared among Enablis staff

### 8.2 Client Project Transitions

- Access requirements must be reviewed during project transitions
- Access rights must be updated promptly when staff roles change on client projects
- Knowledge transfer processes must include access control considerations
- Client approval must be obtained for significant access changes during project delivery

## 9. Physical Access Control

### 9.1 Secure Areas

- Physical access to areas containing sensitive information or equipment must be restricted
- Secure areas must be protected by appropriate entry controls
- Access to secure areas must be logged and monitored
- Visitor access to secure areas must be supervised and recorded

### 9.2 Equipment Security

- Critical equipment must be located in secure areas with appropriate access controls
- Equipment maintenance must be performed only by authorized personnel
- Removal of equipment must be authorized and documented
- Unattended equipment must be physically secured

## 10. Monitoring and Logging

### 10.1 Access Monitoring

- All access to critical systems must be logged and monitored
- Authentication failures must be logged and analyzed for potential security incidents
- Unusual access patterns must be investigated
- Real-time alerts must be generated for critical access control failures

### 10.2 Log Management

- Access logs must be protected from unauthorized modification or deletion
- Logs must be retained in accordance with retention requirements
- Log review procedures must be established and followed
- Log analysis tools should be employed to identify potential security issues

## 11. Exceptions

Exceptions to this policy may be granted only after a documented risk assessment and formal approval by the Security Manager or CTO. All exceptions must be:

- Documented with a clear business justification
- Time-limited with a defined expiration date
- Reviewed periodically for continued necessity

## 12. Policy Compliance

### 12.1 Verification

Compliance with this policy will be verified through:

- Regular security assessments and audits
- Access rights reviews
- Automated monitoring and alerting
- Periodic penetration testing

### 12.2 Consequences of Non-Compliance

Violations of this policy may result in:

- Additional security awareness training
- Restriction or revocation of access rights
- Disciplinary action in accordance with HR policies

## 13. Policy Review

This policy will be reviewed annually or when significant changes occur to ensure it remains aligned with business requirements, evolving security threats, and regulatory obligations.

## 14. Related Documents

- POL-01: Information Security Policy
- POL-02: Acceptable Use Policy
- POL-03: Password Policy
- POL-05: Physical Security Policy
- POL-11: Remote Working Policy
- DOC-12: Information Classification Scheme
- FORM-01: Access Request Form

---

_By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Access Control Policy._
