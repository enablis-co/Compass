# Enablis Network Security Policy

**Document ID**: POL-07  
**Version**: 1.0  
**Last Updated**: February 24, 2025  
**Owner**: IT Operations Manager  
**Approved by**: Chief Technology Officer

## 1. Purpose and Scope

### 1.1 Purpose

This Network Security Policy establishes the requirements for designing, implementing, and managing secure network infrastructure at Enablis. It ensures that our networks maintain appropriate security controls while supporting business operations and enabling technical excellence in service delivery.

### 1.2 Scope

This policy applies to:

- All network infrastructure owned or managed by Enablis
- All network services provided by or used by Enablis
- All connections to external networks, including the internet and client networks
- All employees, contractors, and temporary staff who manage or use Enablis networks
- Client networks designed, implemented, or managed by Enablis

## 2. Network Architecture and Design

### 2.1 Network Segmentation

Networks must be segmented according to security requirements and business functions:

- Network segments must be defined based on data classification and access requirements
- Production environments must be separated from development and testing environments
- Client environments must be isolated from each other and from Enablis corporate networks
- Administrative networks must be separated from user networks

### 2.2 Defense in Depth

Network design must incorporate multiple layers of security controls:

- Perimeter security must be implemented at network boundaries
- Internal security controls must be implemented between network segments
- Host-based security controls must complement network-based controls
- Application-level security must be implemented where appropriate

### 2.3 Zero Trust Architecture

Zero trust principles must be incorporated into network design:

- All network traffic must be authenticated and authorized
- Network access must be granted based on least privilege
- Continuous verification and validation must be implemented
- Micro-segmentation should be implemented where feasible

## 3. Network Access Control

### 3.1 External Access Control

- Internet-facing systems must be protected by firewalls and other security controls
- Remote access must be provided through secure, encrypted connections
- Multi-factor authentication must be required for all remote access
- External access must be limited to required services and authorized personnel

### 3.2 Internal Access Control

- Internal network traffic must be controlled based on business requirements
- Access between network segments must be restricted to necessary communication
- Internal firewalls must be implemented between network segments
- Network Access Control (NAC) solutions should be implemented where appropriate

### 3.3 Wireless Network Security

- Wireless networks must use WPA3 Enterprise or equivalent security
- Corporate and guest wireless networks must be segregated
- Wireless access points must be secured against unauthorized access
- Wireless networks must be regularly scanned for rogue access points

## 4. Network Protection

### 4.1 Intrusion Detection and Prevention

- Intrusion Detection Systems (IDS) and Intrusion Prevention Systems (IPS) must be deployed
- Network traffic must be monitored for suspicious activity
- Alerts must be generated for potential security incidents
- Response procedures must be established for security events

### 4.2 Malware Protection

- Network-based malware protection must be implemented
- Malware signatures must be kept current
- Traffic to known malicious destinations must be blocked
- Suspicious files must be analyzed in a secure environment

### 4.3 Denial of Service Protection

- DDoS protection must be implemented for critical services
- Network capacity planning must account for potential attack traffic
- Traffic rate limiting must be available for implementation during attacks
- Response procedures must be established for DoS events

## 5. Network Device Management

### 5.1 Device Configuration

- Network devices must be configured according to security best practices
- Default credentials must be changed before deployment
- Unused services and ports must be disabled
- Configuration templates should be used to ensure consistency

### 5.2 Authentication and Authorization

- Strong authentication must be required for device management
- Multi-factor authentication should be used where supported
- Administrative access must be limited to authorized personnel
- Privilege levels must be assigned based on job requirements

### 5.3 Software Updates

- Network device firmware must be kept current
- Security patches must be applied according to criticality:
  - Critical patches: within 7 days
  - High severity patches: within 14 days
  - Medium severity patches: within 30 days
  - Low severity patches: during scheduled maintenance
- Patch management procedures must be documented

### 5.4 Configuration Backup

- Network device configurations must be backed up:
  - Before configuration changes
  - After successful configuration changes
  - At least weekly for active devices
- Backups must be stored securely and tested periodically

## 6. Network Traffic Security

### 6.1 Encryption Requirements

- Sensitive data must be encrypted during transmission
- TLS 1.2 or higher must be used for secure communications
- Obsolete encryption protocols and ciphers must be disabled
- Virtual Private Network (VPN) connections must use strong encryption

### 6.2 Traffic Filtering

- Traffic filtering must be implemented at network boundaries
- Rules must be based on the principle of least privilege
- Filtering rules must be documented and regularly reviewed
- Changes to filtering rules must follow change management procedures

### 6.3 Data Flow Control

- Data flows must be mapped and documented
- Unnecessary data flows must be prohibited
- Data flow controls must be implemented based on business requirements
- Data flow documentation must be kept current

## 7. Cloud Network Security

### 7.1 Cloud Network Design

- Cloud networks must follow the same security principles as on-premises networks
- Virtual networks must be properly segmented
- Security groups and network access controls must be implemented
- Private connection services should be used for hybrid cloud connectivity

### 7.2 Cloud Network Monitoring

- Cloud network traffic must be monitored
- Cloud security services must be implemented where available
- Cloud network logs must be collected and analyzed
- Integration between cloud and on-premises security monitoring must be established

### 7.3 Serverless Security

- API gateways must be secured with appropriate authentication and authorization
- Function-to-function communication must be secured
- Least privilege principles must be applied to serverless functions
- Serverless applications must be monitored for suspicious activity

## 8. Client Network Security

### 8.1 Client Network Design

- Client network designs must incorporate security best practices
- Design documentation must include security considerations
- Security requirements must be clarified with clients before implementation
- Compliance requirements must be incorporated into network designs

### 8.2 Client Network Management

- Client networks managed by Enablis must follow this policy where not superseded by client policies
- Differences between this policy and client requirements must be documented
- Security recommendations must be provided to clients when appropriate
- Knowledge transfer to client personnel must include security aspects

## 9. Network Monitoring and Logging

### 9.1 Monitoring Requirements

- Networks must be monitored for:
  - Performance and availability
  - Security events and anomalies
  - Configuration changes
  - Compliance with policies
- Monitoring must be continuous and automated where possible

### 9.2 Logging Requirements

- Network device logs must be centrally collected
- Logs must include:
  - Authentication events
  - Configuration changes
  - Security events
  - System status changes
- Logs must be retained according to retention requirements
- Logs must be protected against unauthorized access or modification

### 9.3 Security Information and Event Management

- SIEM solutions should be implemented for correlation and analysis
- Critical security events must generate alerts
- Alert thresholds must be regularly reviewed and tuned
- Response procedures must be established for different types of alerts

## 10. Network Documentation

### 10.1 Documentation Requirements

- Network architecture must be documented and kept current
- Network device inventory must be maintained
- IP address allocation must be documented
- Security controls must be documented

### 10.2 Diagram Requirements

- Network diagrams must be created and maintained
- Diagrams must show:
  - Network segments and boundaries
  - Security controls and devices
  - External connections
  - Critical systems
- Diagrams must be classified and protected according to their sensitivity

### 10.3 Procedure Documentation

- Standard operating procedures must be documented for:
  - Network changes
  - Incident response
  - Troubleshooting
  - Recovery
- Procedures must be regularly reviewed and updated

## 11. Network Security Assessment

### 11.1 Regular Assessments

- Network vulnerability assessments must be conducted monthly
- Network penetration tests must be conducted annually
- Assessment results must be documented and reviewed
- Identified vulnerabilities must be addressed according to risk

### 11.2 Assessment Scope

- Assessments must include:
  - External perimeter security
  - Internal network security
  - Wireless network security
  - Remote access security
- Assessment methodology must be documented

### 11.3 Continuous Improvement

- Security assessment findings must inform security improvements
- Security controls must be updated based on emerging threats
- Industry developments must be monitored for security implications
- Feedback from security incidents must be incorporated into security planning

## 12. Exceptions

Exceptions to this policy may be granted only after a documented risk assessment and formal approval by the IT Operations Manager or CTO. All exceptions must be:

- Documented with a clear business justification
- Time-limited with a defined expiration date
- Reviewed periodically for continued necessity

## 13. Policy Compliance

### 13.1 Verification

Compliance with this policy will be verified through:

- Regular security assessments
- Network configuration audits
- Log reviews
- Penetration testing

### 13.2 Consequences of Non-Compliance

Failures to comply with this policy may result in:

- Additional security controls or oversight
- Remediation requirements
- Disciplinary action in accordance with HR policies

## 14. Policy Review

This policy will be reviewed annually or when significant changes occur to ensure it remains aligned with business requirements, evolving technology, and regulatory obligations.

## 15. Related Documents

- POL-01: Information Security Policy
- POL-04: Access Control Policy
- POL-06: Backup Policy
- POL-08: Incident Management Policy
- DOC-19: Network Architecture Document
- DOC-20: Network Change Management Procedure

---

_By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Network Security Policy._
