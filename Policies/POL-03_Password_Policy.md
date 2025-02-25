# Enablis Password Policy

**Document ID**: POL-03  
**Version**: 1.0  
**Last Updated**: February 24, 2025  
**Owner**: Security Manager  
**Approved by**: Chief Technology Officer  

## 1. Purpose and Scope

### 1.1 Purpose
This Password Policy establishes the requirements for creating, using, and managing secure passwords across Enablis systems, applications, and services. It supports our commitment to technical excellence while providing practical guidance for maintaining a strong security posture.

### 1.2 Scope
This policy applies to:
- All employees, contractors, and temporary staff of Enablis
- All information systems and services owned or operated by Enablis
- Client systems accessed or managed by Enablis personnel
- All authentication credentials, including passwords, passphrases, and PINs

## 2. Password Requirements

### 2.1 Strength Requirements
All passwords used within Enablis systems must meet the following minimum requirements:

- **Length**: Minimum of 12 characters
- **Complexity**: Include at least three of the following four categories:
  - Uppercase letters (A-Z)
  - Lowercase letters (a-z)
  - Numbers (0-9)
  - Special characters (e.g., @, #, $, %, &)
- **Uniqueness**: Must not match previously used passwords
- **Unpredictability**: Must not contain easily guessable information such as:
  - Common dictionary words
  - Variations of "Enablis" or the system name
  - Personal information (name, birth date, etc.)

### 2.2 Passphrases
Users are encouraged to use passphrases (a sequence of words or a sentence) instead of traditional passwords where systems support this approach. Passphrases should:
- Be at least 16 characters long
- Include spaces or punctuation between words
- Not be a common phrase, quote, or lyric

### 2.3 Password Management Systems
Enablis authorizes and encourages the use of approved password management systems to generate, store, and manage complex, unique passwords. The approved systems are documented in the Approved Software List (DOC-14).

## 3. Password Lifecycle Management

### 3.1 Password Creation
- Initial passwords must be securely communicated to users
- Users must change temporary or initial passwords upon first use
- Password creation guidance will be provided during security awareness training

### 3.2 Password Expiration
- Standard user account passwords must be changed every 90 days
- Privileged account passwords must be changed every 60 days
- System and service account passwords must be changed every 180 days or when an administrator with knowledge of the password leaves the organization

### 3.3 Password History
The system will maintain a password history of at least 12 previous passwords and prevent reuse of these passwords.

### 3.4 Account Lockout
- Accounts will be temporarily locked after five consecutive failed login attempts
- Lockout duration will be 15 minutes or until reset by an administrator
- Repeated lockouts will be investigated as potential security incidents

## 4. Multi-Factor Authentication

### 4.1 MFA Requirements
Multi-Factor Authentication (MFA) is required for:
- All remote access to Enablis systems and services
- Access to systems containing confidential or restricted information
- All privileged or administrative accounts
- All cloud service accounts
- Access to client environments where available

### 4.2 Approved MFA Methods
- Time-based One-Time Password (TOTP) applications
- Hardware security keys
- Push notifications to registered mobile devices
- SMS-based verification (only when other methods are not available)

## 5. Special Account Types

### 5.1 Privileged Accounts
Accounts with elevated privileges (such as administrator accounts) must:
- Use passwords of at least 16 characters with high complexity
- Always employ MFA where technically feasible
- Not be shared among multiple users
- Have activities logged and monitored

### 5.2 Service Accounts
Service accounts used for system-to-system communication must:
- Use automatically generated passwords of at least 20 characters
- Have passwords stored securely in an approved password vault
- Be reviewed quarterly to verify continued need and appropriate access
- Employ API keys, certificates, or other secure authentication mechanisms when passwords are not technically feasible

### 5.3 Emergency Access Accounts
Emergency access accounts must:
- Be strictly controlled and documented
- Have credentials stored securely (e.g., in a sealed envelope in a physical safe)
- Be tested periodically to ensure functionality
- Have passwords changed immediately after use

## 6. Password Storage and Transmission

### 6.1 System Implementation Requirements
All systems that store authentication credentials must:
- Never store passwords in plaintext
- Use modern, strong hashing algorithms (e.g., Argon2, bcrypt) with appropriate salting
- Transmit passwords only over encrypted connections (e.g., TLS)
- Implement secure password reset mechanisms that do not reveal existing passwords

### 6.2 User Responsibilities
Users must:
- Never write down passwords in physical form unless necessary and secured
- Never store passwords in unencrypted electronic documents
- Not include passwords in email messages, chat conversations, or other communications
- Use approved password managers for storing and generating passwords

## 7. Client Environment Considerations

### 7.1 Client Password Policies
When accessing client environments:
- Follow client password policies when they are more stringent than Enablis policies
- Recommend improvements to client password policies when appropriate
- Document any exceptions where client policies are less stringent than Enablis standards

### 7.2 Customer System Access
When Enablis staff require access to customer systems:
- Use dedicated, individual credentials for each staff member
- Implement time-limited access where possible
- Maintain a record of all access credentials issued
- Revoke access promptly when no longer required

## 8. Password Security Incident Response

### 8.1 Compromised Passwords
If a password is suspected to be compromised:
- Change the password immediately
- Report the incident to the Security Manager
- Assess whether other accounts or systems may be affected
- Review logs for any unauthorized access

### 8.2 Password Reset Procedures
Password reset procedures must:
- Verify the identity of the requester through mechanisms other than the compromised password
- Not reveal the existing password
- Generate a secure temporary password or reset link with a short expiration time
- Force a password change upon successful login

## 9. Technical Implementation

### 9.1 Authentication Systems
All authentication systems must implement:
- Secure storage of credentials using appropriate hashing
- Account lockout capabilities
- Password complexity enforcement
- Secure password reset mechanisms
- Audit logging of authentication events

### 9.2 Single Sign-On
Where appropriate, Single Sign-On (SSO) solutions may be implemented to:
- Reduce the number of passwords users must remember
- Increase security through centralized authentication controls
- Streamline the user experience
- Provide comprehensive authentication logging

## 10. Exceptions

Exceptions to this policy may be granted only after a documented risk assessment and formal approval by the Security Manager or CTO. All exceptions must be:
- Documented with a clear business justification
- Time-limited with a defined expiration date
- Reviewed periodically for continued necessity

## 11. Policy Compliance

### 11.1 Verification
Compliance with this policy will be verified through:
- Regular security assessments
- Automated password strength audits
- Authentication system configuration reviews
- Security awareness assessments

### 11.2 Consequences of Non-Compliance
Violations of this policy may result in:
- Additional security awareness training
- Restriction of system access
- Disciplinary action in accordance with HR policies

## 12. Policy Review

This policy will be reviewed annually or when significant changes occur to ensure it remains aligned with business requirements, evolving security threats, and industry best practices.

## 13. Related Documents

- POL-01: Information Security Policy
- POL-02: Acceptable Use Policy
- POL-04: Access Control Policy
- DOC-14: Approved Software List
- POL-10: Data Protection Policy

---

*By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Password Policy.*