# Enablis Cryptographic Controls Procedure

**Document ID**: DOC-17  
**Version**: 1.0  
**Last Updated**: February 24, 2025  
**Owner**: Security Manager  
**Approved by**: Chief Technology Officer

## 1. Introduction

### 1.1 Purpose

This Cryptographic Controls Procedure provides detailed implementation guidance for the requirements established in the Cryptographic Controls Policy (POL-13). It ensures consistent, secure implementation of cryptographic technologies across Enablis systems and operations.

### 1.2 Scope

This procedure applies to:

- All systems and applications using cryptographic controls
- All development and operations staff implementing or managing cryptography
- All environments including development, testing, staging, and production
- Client systems where Enablis is responsible for implementing cryptographic controls

## 2. Algorithm Implementation Standards

### 2.1 Symmetric Encryption Implementation

#### 2.1.1 AES Implementation

- AES-256 should be the default choice for symmetric encryption
- AES-128 may be used for performance-critical applications where the lower security level is acceptable
- Approved modes of operation:
  - GCM (Galois/Counter Mode) - Preferred for most applications
  - CBC (Cipher Block Chaining) with proper padding and integrity protection
  - CTR (Counter Mode) with proper integrity protection
- Initialization Vectors (IVs):
  - Must be randomly generated for each encryption operation
  - Must never be reused with the same key
  - Must be securely stored or transmitted with the ciphertext

#### 2.1.2 ChaCha20-Poly1305 Implementation

- May be used as an alternative to AES-GCM, particularly on platforms without AES hardware acceleration
- Nonce must be randomly generated for each encryption operation
- Nonce must never be reused with the same key

### 2.2 Asymmetric Encryption Implementation

#### 2.2.1 RSA Implementation

- Minimum key length: 2048 bits
- Recommended key length: 4096 bits
- Key generation must use secure random number generators
- PKCS#1 v2.2 OAEP padding must be used for encryption
- Implementation must be resistant to timing attacks

#### 2.2.2 Elliptic Curve Cryptography Implementation

- Approved curves:
  - P-256, P-384, P-521 (NIST curves)
  - Curve25519 for key agreement
  - Ed25519 for digital signatures
- Secure random number generators must be used for key generation
- Implementations should use standard libraries with mitigations for side-channel attacks

### 2.3 Hash Function Implementation

#### 2.3.1 Secure Hash Implementation

- SHA-256 is the minimum acceptable hash function
- SHA-384 or SHA-512 should be used for higher security requirements
- Hash functions must be implemented using validated libraries

#### 2.3.2 Password Hashing Implementation

- Argon2id is the preferred algorithm for password hashing
- Bcrypt is an acceptable alternative when Argon2 is not available
- PBKDF2-HMAC-SHA256 with at least 100,000 iterations may be used when other options are not available
- Implementation parameters:
  - Argon2id: Memory cost ≥ 64 MiB, Iterations ≥ 3, Parallelism based on system capabilities
  - Bcrypt: Cost factor ≥ 12, increasing as hardware capabilities improve
  - Salt must be randomly generated, unique, and at least 16 bytes

### 2.4 Digital Signature Implementation

#### 2.4.1 RSA Signature Implementation

- Minimum key length: 2048 bits
- Recommended key length: 4096 bits
- PKCS#1 v2.2 PSS padding must be used
- SHA-256 or stronger hash function must be used

#### 2.4.2 ECDSA Implementation

- Approved curves: P-256, P-384, P-521
- Deterministic ECDSA (RFC 6979) should be used when available
- Implementations must use standard libraries with protections against side-channel attacks

#### 2.4.3 EdDSA Implementation

- Ed25519 is the preferred algorithm for new implementations
- Standard library implementations should be used

## 3. Key Management Procedures

### 3.1 Key Generation

#### 3.1.1 Random Number Generation

- Cryptographically secure random number generators must be used
- On modern operating systems, use:
  - `/dev/urandom` or `getrandom()` on Linux/Unix
  - `BCryptGenRandom()` or `CryptGenRandom()` on Windows
  - `SecRandomCopyBytes()` on macOS/iOS
- In languages, use secure RNG implementations:
  - Java: `SecureRandom`
  - Python: `secrets` module
  - Node.js: `crypto.randomBytes()`
  - Go: `crypto/rand`

#### 3.1.2 Key Generation Process

1. Determine the purpose and required security level for the key
2. Select appropriate algorithm and key length
3. Use secure random number generator to create key material
4. For asymmetric keys, follow industry standard key generation procedures
5. Document key properties (algorithm, length, purpose, creation date)
6. Apply appropriate access controls immediately upon generation
7. Generate and securely store any key backup required

### 3.2 Key Storage

#### 3.2.1 Key Storage Mechanisms

- Production environment:
  - AWS: AWS Key Management Service (KMS) or AWS Secrets Manager
  - Azure: Azure Key Vault
  - GCP: Google Cloud KMS or Secret Manager
  - On-premises: Hardware Security Modules (HSMs) when available
- Development and testing environments:
  - Environment-specific secret managers with appropriate access controls
  - Never store keys in code, config files, or repositories

#### 3.2.2 Key Storage Implementation

For each key storage solution, implement:

1. Access control lists limited to required personnel/systems
2. Audit logging of all key access
3. Encryption of key storage at rest
4. Secure backup procedures if applicable
5. Key rotation capability
6. Separate storage for different environments

### 3.3 Key Distribution

#### 3.3.1 Secure Key Transport

- TLS 1.2+ must be used for all key transport over networks
- Asymmetric encryption should be used to exchange symmetric keys
- Key wrapping should be used when distributing symmetric keys
- Key exchange protocols should use Perfect Forward Secrecy where possible

#### 3.3.2 Key Access Control

- Principle of least privilege must be applied to key access
- Authentication and authorization required for key access
- Multi-factor authentication should be required for high-value keys
- Separation of duties should be implemented for critical keys

### 3.4 Key Rotation Procedures

#### 3.4.1 Scheduled Rotation

1. Determine rotation schedule based on key type and purpose
2. Create new key using secure key generation procedures
3. Update systems to use new key while maintaining old key for decryption
4. Monitor for systems still using old key
5. Decommission old key when no longer needed
6. Document rotation in key management log

#### 3.4.2 Emergency Rotation (Key Compromise)

1. Generate new key immediately
2. Revoke compromised key and add to compromised key list
3. Update all systems to use new key with high priority
4. Re-encrypt sensitive data that was protected by the compromised key
5. Investigate cause of compromise
6. Document incident and response

### 3.5 Key Backup and Recovery

#### 3.5.1 Key Backup Procedures

1. Identify keys requiring backup based on criticality
2. Create encrypted backup of key material
3. Store backup in secure, separate location from primary key
4. Implement dual control for backup access (multiple custodians)
5. Test recovery procedures periodically
6. Update backups when keys change

#### 3.5.2 Key Recovery Procedures

1. Validate authorization for recovery request
2. Require multiple approvals for critical key recovery
3. Retrieve key backup from secure storage
4. Decrypt backup using authorized procedures
5. Verify key integrity before use
6. Document recovery event including reason and authorization

### 3.6 Key Destruction

#### 3.6.1 Secure Key Destruction

1. Identify keys for destruction (expired, compromised, or no longer needed)
2. Verify no systems or data still require the key
3. Securely delete key material from primary storage
4. Securely delete key backups
5. Document destruction including verification method
6. For hardware-based keys, follow vendor destruction procedures

#### 3.6.2 Verification of Destruction

- HSM or secure key store logs should confirm deletion
- Backup copies must be verified as destroyed
- Attempt to use destroyed keys should fail
- Document verification steps taken

## 4. Transport Layer Security (TLS) Implementation

### 4.1 TLS Configuration Standards

#### 4.1.1 Minimum TLS Version

- TLS 1.2 is the minimum acceptable version
- TLS 1.3 should be preferred when supported by all endpoints
- SSL 2.0, SSL 3.0, TLS 1.0, and TLS 1.1 must be disabled

#### 4.1.2 Cipher Suite Selection

Approved cipher suites for TLS 1.2:

```
TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384
TLS_ECDHE_ECDSA_WITH_CHACHA20_POLY1305_SHA256
TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
TLS_ECDHE_RSA_WITH_CHACHA20_POLY1305_SHA256
```

Approved cipher suites for TLS 1.3:

```
TLS_AES_128_GCM_SHA256
TLS_AES_256_GCM_SHA384
TLS_CHACHA20_POLY1305_SHA256
```

#### 4.1.3 Certificate Requirements

- Certificates must use RSA (2048-bit minimum) or ECDSA (P-256 minimum)
- Certificates must be signed using SHA-256 or stronger
- Certificates should be issued by trusted Certificate Authorities
- Self-signed certificates should only be used in testing environments
- Wildcard certificates should be limited to specific use cases

#### 4.1.4 Protocol Settings

- Perfect Forward Secrecy (PFS) must be enabled
- Secure renegotiation must be enabled
- Client-initiated renegotiation should be disabled
- HTTP Strict Transport Security (HSTS) should be enabled for web servers
- OCSP Stapling should be enabled when supported

### 4.2 Certificate Management

#### 4.2.1 Certificate Issuance

1. Generate key pair using secure key generation procedures
2. Create Certificate Signing Request (CSR) with appropriate attributes
3. Submit CSR to approved Certificate Authority
4. Validate certificate upon receipt
5. Install certificate and private key with appropriate security controls
6. Test certificate functionality
7. Document certificate details in certificate inventory

#### 4.2.2 Certificate Renewal

1. Identify certificates requiring renewal (90 days before expiration)
2. Generate new key pair (preferred) or reuse existing key
3. Submit renewal request to Certificate Authority
4. Validate renewed certificate
5. Test new certificate in non-production environment if possible
6. Schedule certificate deployment during maintenance window
7. Update certificate inventory

#### 4.2.3 Certificate Revocation

1. Identify compromised or invalid certificates
2. Contact Certificate Authority to request revocation
3. Verify certificate appears on Certificate Revocation List (CRL) or OCSP
4. Remove revoked certificate from all systems
5. Deploy replacement certificate if needed
6. Update certificate inventory
7. Document revocation including reason

## 5. Implementation Procedures for Common Use Cases

### 5.1 Data at Rest Encryption

#### 5.1.1 Full Disk Encryption

- Windows: BitLocker with minimum 256-bit encryption
  - TPM-based key protection when available
  - Recovery keys must be securely stored in enterprise key backup system
- macOS: FileVault with minimum 256-bit encryption
  - Recovery keys must be securely stored in enterprise key backup system
- Linux: LUKS with minimum 256-bit AES encryption
  - Recovery mechanisms must be documented and tested

#### 5.1.2 Database Encryption

- Transparent Data Encryption (TDE) should be implemented where available
- Column-level encryption should use AES-256 in an appropriate mode
- Application-level encryption should use approved libraries
- Key management must be separate from the database
- Encryption should be configured to protect sensitive data as identified by data classification

#### 5.1.3 File-level Encryption

- AES-256 in an appropriate mode must be used
- Key management must follow organizational standards
- Access controls must complement encryption
- File integrity verification should be implemented

### 5.2 Data in Transit Encryption

#### 5.2.1 Web Application Encryption

- TLS 1.2+ must be implemented according to TLS Configuration Standards
- All HTTP traffic must redirect to HTTPS
- Internal application traffic should also use TLS
- APIs must require TLS for all endpoints

#### 5.2.2 Email Encryption

- TLS must be used for SMTP traffic between mail servers
- Opportunistic TLS should be enabled
- S/MIME or PGP should be available for message-level encryption
- Key management procedures for email encryption must be documented

#### 5.2.3 File Transfer Encryption

- SFTP or FTPS must be used instead of FTP
- Public key authentication should be used where possible
- Passwords used for authentication must comply with Password Policy
- Ad-hoc file sharing must use encrypted channels

### 5.3 Authentication Credentials

#### 5.3.1 Password Storage

- Passwords must never be stored in plaintext
- Password hashing must use Argon2id, Bcrypt, or PBKDF2 as specified
- Unique salt must be generated for each password
- Salt and hash parameters must be stored with the hash

#### 5.3.2 Implementation Example (Pseudo-code)

```
// Using Argon2id for password hashing
function hashPassword(password) {
  // Generate a random 16-byte salt
  salt = secureRandomBytes(16);

  // Configure Argon2id parameters
  // Memory: 64 MiB, Iterations: 3, Parallelism: 4
  params = {
    type: Argon2id,
    memoryCost: 65536,  // 64 MiB in KiB
    iterations: 3,
    parallelism: 4,
    saltLength: 16,
    hashLength: 32      // 256 bits
  };

  // Hash the password
  hash = Argon2.hash(password, salt, params);

  // Return the salt, parameters, and hash for storage
  return {
    algorithm: "Argon2id",
    salt: base64Encode(salt),
    memoryCost: params.memoryCost,
    iterations: params.iterations,
    parallelism: params.parallelism,
    hash: base64Encode(hash)
  };
}

function verifyPassword(password, storedHash) {
  // Extract parameters from stored hash
  algorithm = storedHash.algorithm;
  salt = base64Decode(storedHash.salt);
  params = {
    type: getAlgorithmType(algorithm),
    memoryCost: storedHash.memoryCost,
    iterations: storedHash.iterations,
    parallelism: storedHash.parallelism,
    saltLength: salt.length,
    hashLength: base64Decode(storedHash.hash).length
  };

  // Hash the provided password with the same parameters
  hashToCheck = Argon2.hash(password, salt, params);

  // Compare the hashes in constant time
  return secureCompare(hashToCheck, base64Decode(storedHash.hash));
}
```

### 5.4 Code Signing

#### 5.4.1 Internal Application Signing

- RSA (4096-bit) or ECDSA (P-384) keys should be used
- Private keys must be protected using HSM or secure key storage
- Key access should require multiple approvals
- Signing process should be automated and logged
- Verification should be enforced before execution

#### 5.4.2 Mobile Application Signing

- Platform-specific requirements must be followed
- Signing keys must be secured according to key storage standards
- Signing process must be documented and controlled
- Backup procedures must be established for signing keys

## 6. Cloud and Third-Party Cryptography

### 6.1 Cloud Key Management Services

#### 6.1.1 AWS Key Management Service

- Customer Master Keys (CMKs) should be used to protect data keys
- Automatic rotation should be enabled for CMKs
- Key policies should implement least privilege
- Multi-region keys should be used for disaster recovery when appropriate
- AWS KMS should be preferred over client-side key management when possible

#### 6.1.2 Azure Key Vault

- Key rotation should be enabled
- Access policies should implement least privilege
- Soft-delete and purge protection should be enabled
- Monitoring and alerting should be configured
- Azure-managed keys should be used when appropriate

#### 6.1.3 Google Cloud KMS

- Key rotation should be configured
- IAM policies should implement least privilege
- Protection level should be selected based on security requirements
- Monitoring and alerting should be configured

### 6.2 Customer-Managed Encryption Keys (CMEK)

#### 6.2.1 CMEK Implementation

1. Determine business and compliance requirements for key control
2. Select appropriate cloud KMS for key management
3. Generate keys according to key generation procedures
4. Configure cloud service to use customer-managed keys
5. Implement key rotation procedures
6. Document key ownership and procedures

#### 6.2.2 CMEK Management Responsibilities

- Maintain inventory of all CMEKs
- Implement appropriate backup procedures
- Establish clear ownership and responsibilities
- Monitor key usage and access
- Test key rotation and recovery procedures

## 7. Development Implementation Guidelines

### 7.1 Secure Coding for Cryptography

#### 7.1.1 General Guidelines

- Use established cryptographic libraries rather than custom implementations
- Keep cryptographic libraries updated to current versions
- Follow library documentation for secure implementation
- Use higher-level APIs when available
- Implement error handling that doesn't reveal sensitive information

#### 7.1.2 Approved Libraries

Programming language-specific approved libraries:

**Java:**

- Java Cryptography Extension (JCE) with strong providers
- Bouncy Castle (for algorithms not in JCE)
- Tink

**Python:**

- cryptography.io
- PyNaCl
- hashlib (for hashing only)

**JavaScript/Node.js:**

- Web Crypto API (browser)
- Node.js crypto module
- sodium-plus
- noble-crypto libraries

**Go:**

- Go standard crypto packages
- golang.org/x/crypto

**C#/.NET:**

- .NET Cryptography classes
- Bouncy Castle .NET

### 7.2 Testing Cryptographic Implementations

#### 7.2.1 Unit Testing

- Verify correct encryption/decryption with test vectors
- Test key generation produces keys of correct size and format
- Verify error conditions are handled properly
- Test against known weak inputs
- Verify algorithm negotiation selects strongest available option

#### 7.2.2 Security Testing

- Verify no key material is logged or exposed
- Test for side-channel vulnerabilities where applicable
- Verify secure key storage implementation
- Test key rotation procedures
- Verify cryptographic operations timing doesn't leak information

## 8. Compliance Verification

### 8.1 Cryptographic Inventory

#### 8.1.1 Inventory Requirements

Maintain inventory of:

- Cryptographic algorithms in use
- Key lengths and parameters
- Implementation libraries and versions
- Key storage mechanisms
- Certificate details and expiration dates

#### 8.1.2 Inventory Process

1. Automated scanning of code repositories for cryptographic functions
2. Manual review of application architectures
3. Documentation review
4. Regular updates during change management
5. Validation during security assessments

### 8.2 Compliance Checking

#### 8.2.1 Automated Checking

- Static application security testing (SAST) for cryptographic issues
- Configuration analysis for TLS settings
- Key length and algorithm verification
- Certificate validation

#### 8.2.2 Manual Review

- Cryptographic architecture review
- Key management procedure validation
- Implementation review of critical cryptographic components
- Key access control review

## 9. Cryptographic Exception Management

### 9.1 Exception Request Process

1. Document the cryptographic control that cannot be implemented
2. Provide technical justification for the exception
3. Assess security impact and risk
4. Identify compensating controls
5. Specify time limitation for the exception
6. Obtain approval from Security Manager and CTO

### 9.2 Exception Documentation

- Each exception must be documented in the Cryptographic Exceptions Register
- Documentation must include:
  - Description of the exception
  - Business justification
  - Risk assessment
  - Compensating controls
  - Approval details
  - Expiration date
  - Review schedule

### 9.3 Exception Review

- Exceptions must be reviewed:
  - At specified intervals (at least quarterly)
  - When related technology changes
  - Prior to exception expiration
  - During cryptographic compliance assessments

## 10. Related Documents

- POL-01: Information Security Policy
- POL-13: Cryptographic Controls Policy
- DOC-31: Key Management Procedure
- DOC-32: Approved Cryptographic Standards
- FORM-08: Cryptographic Exception Request
- DOC-40: Certificate Management Procedure

---

_By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Cryptographic Controls Procedure._
