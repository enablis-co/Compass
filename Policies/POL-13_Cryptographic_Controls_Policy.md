# Enablis Cryptographic Controls Policy

**Document ID**: POL-13  
**Version**: 1.0  
**Last Updated**: February 24, 2025  
**Owner**: Security Manager  
**Approved by**: Chief Technology Officer  

## 1. Purpose and Scope

### 1.1 Purpose
This Cryptographic Controls Policy establishes the requirements for implementing and managing cryptographic technologies within Enablis systems and operations. It ensures that cryptographic controls are applied consistently and effectively to protect the confidentiality, integrity, and authenticity of information assets.

### 1.2 Scope
This policy applies to:
- All information systems owned or managed by Enablis
- All data encryption activities across Enablis operations
- All employees, contractors, and temporary staff involved in implementing or managing cryptographic controls
- Client systems and data where Enablis is responsible for implementing cryptographic controls
- All environments including development, testing, staging, and production

## 2. Cryptographic Control Principles

### 2.1 Defense in Depth
Cryptographic controls should be implemented as part of a defense-in-depth strategy, complementing other security controls rather than serving as the sole protection mechanism.

### 2.2 Appropriate Protection
The strength and type of cryptographic controls should be proportionate to the sensitivity of the information being protected and the identified risks.

### 2.3 Technical Excellence
Cryptographic implementations should reflect industry best practices and be reviewed regularly to maintain effectiveness against evolving threats.

### 2.4 Operational Efficiency
Cryptographic controls should be implemented in a manner that protects information while enabling efficient business operations.

### 2.5 Regulatory Compliance
Cryptographic controls must comply with relevant legal and regulatory requirements in jurisdictions where Enablis and its clients operate.

## 3. Cryptographic Requirements

### 3.1 Encryption Algorithms and Protocols

#### 3.1.1 Approved Algorithms
The following encryption algorithms are approved for use:
- **Symmetric Encryption**: AES-256, AES-192, AES-128
- **Asymmetric Encryption**: RSA (minimum 2048-bit), Elliptic Curve Cryptography (ECC)
- **Hashing**: SHA-256, SHA-384, SHA-512
- **Digital Signatures**: RSA-PSS, ECDSA, Ed25519

#### 3.1.2 Prohibited Algorithms
The following algorithms are considered insecure and must not be used:
- DES, 3DES
- RC4
- MD5, SHA-1
- RSA with key lengths less than 2048 bits

#### 3.1.3 Protocol Requirements
- TLS 1.2 or higher must be used for secure communications
- Secure cipher suites must be configured according to current best practices
- Obsolete protocols (SSL 2.0, SSL 3.0, TLS 1.0, TLS 1.1) must be disabled

### 3.2 Key Management

#### 3.2.1 Key Generation
- Keys must be generated using approved random number generators
- Cryptographic keys must be of sufficient length for the algorithm and use case
- Key generation must occur in secure environments

#### 3.2.2 Key Storage
- Private and symmetric keys must be stored in secured locations
- Hardware Security Modules (HSMs) should be used for high-value keys when feasible
- Keys must never be stored in plaintext in code, configuration files, or repositories

#### 3.2.3 Key Distribution
- Secure methods must be used for key distribution
- Keys must be transmitted using encrypted channels
- Out-of-band methods should be used for initial key exchange when appropriate

#### 3.2.4 Key Rotation
- Encryption keys must be rotated according to the following schedule:
  - Symmetric encryption keys: At least annually
  - Asymmetric encryption keys: At least every two years
  - Session keys: Each session or transaction
- More frequent rotation may be required based on data sensitivity or usage patterns

#### 3.2.5 Key Revocation
- Procedures must be established for emergency key revocation
- Compromised keys must be revoked immediately
- Systems using the compromised keys must be updated promptly

#### 3.2.6 Key Backup and Recovery
- Critical keys must be securely backed up
- Key recovery procedures must be documented and tested
- Access to key backups must be strictly controlled

## 4. Use Cases for Cryptographic Controls

### 4.1 Data at Rest
- Sensitive data stored in databases must be encrypted using appropriate algorithms
- File system encryption must be implemented for devices containing sensitive information
- Backup media must be encrypted
- Cloud storage must use encryption with customer-managed keys where possible

### 4.2 Data in Transit
- All sensitive data transmitted over networks must be encrypted
- VPN or equivalent secure channels must be used for remote access
- Secure file transfer protocols must be used for file transmission
- APIs handling sensitive data must use TLS encryption

### 4.3 Data in Use
- Memory protection techniques should be implemented where feasible
- Temporary files containing sensitive data must be encrypted
- Clear-text data should be kept in memory only as long as necessary

### 4.4 Authentication and Authorization
- Passwords must be stored using strong hashing algorithms with appropriate salting
- Multi-factor authentication should use cryptographically strong mechanisms
- Session tokens must be cryptographically secure
- Digital signatures must be used for critical authorizations

### 4.5 Code Signing
- Code must be signed to verify authenticity and integrity
- Code signing keys must be highly protected
- Code signatures must be verified before execution of critical code

## 5. Cryptographic Controls in Cloud and Third-Party Services

### 5.1 Cloud Service Requirements
- Cloud services storing sensitive data must provide encryption
- Encryption key management options must be evaluated for each service
- Customer-managed keys should be used where available
- Encryption implementation details should be verified

### 5.2 SaaS Application Requirements
- SaaS applications handling sensitive data must implement encryption
- Transport encryption requirements must be verified
- Data encryption at rest capabilities must be enabled
- Key management practices of vendors must be assessed

### 5.3 Third-Party Integration Requirements
- APIs to third-party services must use secure protocols
- Data shared with third parties must be encrypted when containing sensitive information
- Authentication to third-party services must use secure methods
- Encryption requirements must be included in contracts and service agreements

## 6. Cryptographic Controls for Development

### 6.1 Secure Coding Practices
- Developers must be trained on secure cryptographic implementation
- Standard, tested cryptographic libraries must be used
- Cryptographic implementations must be reviewed during code reviews
- Cryptographic functions must be tested for correct operation

### 6.2 Cryptographic Libraries
- Only approved cryptographic libraries may be used
- Open-source cryptographic libraries must be from reputable sources and actively maintained
- Library updates must be applied promptly, especially security patches
- Custom cryptographic implementations are prohibited without explicit approval

### 6.3 Secrets Management
- Application secrets must not be hardcoded
- Secure secrets management solutions must be used
- Environment variables should be used only for non-sensitive configuration
- Secrets rotation must be supported in application design

## 7. Client Environment Considerations

### 7.1 Client Security Requirements
- Client-specific cryptographic requirements must be documented
- Compliance with client standards must be verified
- Exceptions to client requirements must be approved and documented
- Client approval must be obtained for cryptographic implementations affecting their data

### 7.2 Cross-Client Considerations
- Encryption must maintain appropriate segregation between client environments
- Shared infrastructure must ensure cryptographic separation of client data
- Key management must support client-specific keys where required
- Documentation must be maintained for client-specific configurations

## 8. Cryptographic Hardware and Modules

### 8.1 Hardware Security Modules (HSMs)
- HSMs should be considered for high-value key protection
- HSMs must be certified to appropriate standards when required
- HSM access must be strictly controlled
- HSM operations must be logged and monitored

### 8.2 Trusted Platform Modules (TPMs)
- TPM capabilities should be leveraged when available
- TPM-based encryption should be used for device protection
- TPM measurements should be used for boot verification where appropriate

### 8.3 Smart Cards and Tokens
- Hardware tokens for authentication must use strong cryptographic mechanisms
- Token distribution must be controlled and documented
- Token revocation procedures must be established
- Lifecycle management for cryptographic tokens must be implemented

## 9. Compliance and Verification

### 9.1 Cryptographic Standards Compliance
- Cryptographic implementations must comply with relevant standards:
  - FIPS 140-2/140-3 where required
  - NIST guidelines for algorithm selection
  - Industry-specific standards as applicable

### 9.2 Cryptographic Assessment
- Periodic reviews of cryptographic implementations must be conducted
- Cryptographic systems must be included in security assessments
- Penetration testing should include cryptographic control verification
- Vulnerabilities in cryptographic implementations must be addressed promptly

### 9.3 Documentation Requirements
- Cryptographic implementations must be documented
- Key management procedures must be documented
- System cryptographic architecture must be maintained
- Cryptographic exception handling must be documented

## 10. Incident Response for Cryptographic Failures

### 10.1 Types of Cryptographic Incidents
- Algorithm compromise or deprecation
- Key compromise
- Implementation vulnerabilities
- Certificate expiration or revocation

### 10.2 Incident Handling
- Cryptographic incidents must follow the Incident Management Policy (POL-08)
- Response plans must be established for common cryptographic failures
- Critical system recovery must include cryptographic recovery procedures
- Forensic analysis must be conducted for significant cryptographic failures

### 10.3 Communication Plan
- Stakeholders must be notified of cryptographic incidents according to their impact
- Clear communication must be provided about remediation steps
- Technical details of cryptographic vulnerabilities must be handled securely
- Regulatory reporting requirements must be followed

## 11. Training and Awareness

### 11.1 Technical Staff Training
- Staff implementing cryptographic controls must receive specialized training
- Developers must be trained on secure cryptographic implementation
- Operational staff must understand key management procedures
- Security staff must be knowledgeable about cryptographic vulnerabilities

### 11.2 General Awareness
- All staff should understand basic concepts of cryptography
- Staff should be aware of when encryption is required
- Staff should understand the risks of improper cryptographic implementation
- Awareness materials should be updated to reflect current threats

## 12. Exceptions

Exceptions to this policy may be granted only after a documented risk assessment and formal approval by the Security Manager or CTO. All exceptions must be:
- Documented with a clear business justification
- Time-limited with a defined expiration date
- Reviewed periodically for continued necessity
- Include compensating controls where appropriate

## 13. Policy Compliance

### 13.1 Verification
Compliance with this policy will be verified through:
- System configuration reviews
- Code reviews for cryptographic implementation
- Security assessments and audits
- Key management procedure reviews

### 13.2 Consequences of Non-Compliance
Failures to comply with this policy may result in:
- Remediation requirements
- System isolation until compliance is achieved
- Additional oversight or controls
- Disciplinary action in accordance with HR policies

## 14. Policy Review

This policy will be reviewed annually or when significant changes occur to ensure it remains aligned with business requirements, technological developments, evolving threats, and industry best practices.

## 15. Related Documents

- POL-01: Information Security Policy
- POL-07: Network Security Policy
- POL-08: Incident Management Policy
- DOC-17: Cryptographic Controls Procedure
- DOC-31: Key Management Procedure
- DOC-32: Approved Cryptographic Standards

---

*By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Cryptographic Controls Policy.*