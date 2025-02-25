---
layout: page
title: "Secure Development Policy"
permalink: /policies/isms-pol-05/
---

**Document ID**: ISMS-POL-05  
**Version**: 1.0  
**Last Updated**: February 25, 2025  
**Owner**: Chief Technology Officer  
**Approved by**: Board of Directors

## 1. Purpose and Scope

### 1.1 Purpose

This Secure Development Policy establishes the requirements for integrating security throughout the software development lifecycle at Enablis. It ensures that security is a foundational element of our development practices, supporting our commitment to technical excellence while protecting our clients' systems and data.

### 1.2 Scope

This policy applies to:

- All software development activities conducted by Enablis
- All employees, contractors, and temporary staff involved in development activities
- All development environments, tools, and processes
- Client applications and systems developed or maintained by Enablis
- Third-party code and components integrated into Enablis projects

## 2. Secure Development Principles

Enablis applies these core principles to our development approach:

### 2.1 Security by Design

Security is integrated from the beginning of the development lifecycle rather than added later, making it a foundational element of our technical solutions.

### 2.2 Defense in Depth

Multiple layers of security controls are implemented to ensure that the failure of a single control does not compromise the entire system.

### 2.3 Least Privilege

Applications and systems are designed to operate with the minimum privileges necessary to fulfill their functions, reducing the potential impact of compromises.

### 2.4 Secure Defaults

Security settings are configured for maximum security by default, requiring conscious decisions to reduce security rather than to enhance it.

### 2.5 Fail Secure

Systems are designed to maintain security in the event of failures, defaulting to a secure state rather than an insecure one when errors occur.

### 2.6 Continuous Improvement

Security practices evolve with emerging threats and technologies, incorporating lessons learned and new best practices.

## 3. Secure Development Lifecycle

### 3.1 Requirements Phase

#### 3.1.1 Security Requirements

- Security requirements must be defined during the initial requirements gathering
- Compliance requirements must be identified and documented
- Threat modeling should be performed for applications with sensitive functionality
- Security requirements must be traceable throughout the development lifecycle

#### 3.1.2 Risk Assessment

- Security risks must be assessed during the planning phase
- Risk assessment should inform security control requirements
- High-risk applications require more rigorous security controls
- Client-specific risk considerations must be documented

### 3.2 Design Phase

#### 3.2.1 Secure Architecture

- Application architecture must incorporate security best practices
- Security patterns appropriate to the application type should be applied
- Defense in depth must be incorporated into the design
- Attack surface should be minimized through conscious design decisions

#### 3.2.2 Threat Modeling

- Threat modeling should be conducted for applications handling sensitive data
- Potential threats must be identified and documented
- Mitigation strategies must be defined for identified threats
- Threat models should be updated when significant architectural changes occur

### 3.3 Development Phase

#### 3.3.1 Secure Coding Standards

- Developers must follow established secure coding standards
- Language-specific security guidelines must be applied
- Code must be written to prevent common vulnerabilities
- Security considerations must be included in code reviews

#### 3.3.2 Code Reviews

- Security-focused code reviews must be conducted
- Peer reviews should include security considerations
- High-risk code components require additional review
- Security issues identified during review must be addressed before release

### 3.4 Testing Phase

#### 3.4.1 Security Testing

- Security testing must be integrated into the testing process
- Automated security testing tools should be utilized where appropriate
- Vulnerability scanning must be performed before release
- Penetration testing should be conducted for high-risk applications

#### 3.4.2 Test Coverage

- Security test cases must verify security requirements
- Negative testing should be included to verify error handling
- Authentication and authorization controls must be thoroughly tested
- Data validation controls must be verified

### 3.5 Deployment Phase

#### 3.5.1 Secure Deployment

- Deployment processes must maintain system and data security
- Production credentials must be properly secured
- Deployment automation should include security verification
- Deployment approval must include security sign-off

#### 3.5.2 Production Validation

- Security configurations must be verified in production
- Production security testing should be conducted where appropriate
- Security issues identified in production must be prioritized for remediation
- Security monitoring must be enabled upon deployment

### 3.6 Maintenance Phase

#### 3.6.1 Security Updates

- Security patches must be applied in a timely manner
- Vulnerability management must be ongoing
- Regular security assessments should be conducted
- Security improvements should be incorporated into maintenance releases

#### 3.6.2 Incident Response

- Security incidents must be addressed according to the Incident Management Policy
- Root causes of security vulnerabilities must be analyzed
- Lessons learned must be incorporated into development practices
- Vulnerability patterns should inform security testing improvements

## 4. Secure Coding Practices

### 4.1 Authentication and Authorization

#### 4.1.1 Authentication Requirements

- Strong authentication mechanisms must be implemented
- Multi-factor authentication should be supported for sensitive functions
- Secure credential storage must be implemented
- Account lockout protections should be implemented

#### 4.1.2 Authorization Controls

- Authorization checks must be implemented at all access points
- Role-based access control should be used where appropriate
- Authorization controls must be tested thoroughly
- Least privilege principles must be applied to authorization design

### 4.2 Data Validation and Encoding

#### 4.2.1 Input Validation

- All user inputs must be validated
- Server-side validation must be implemented
- Input validation should use allowlist approaches where possible
- Validation failures must be handled securely

#### 4.2.2 Output Encoding

- Data must be appropriately encoded for its output context
- HTML, JavaScript, SQL, and other contexts require specific encoding
- User-supplied data must never be interpreted as code
- Encoding libraries should be used rather than custom implementations

### 4.3 Data Protection

#### 4.3.1 Sensitive Data Handling

- Sensitive data must be identified and documented
- Sensitive data must be encrypted during storage and transmission
- Data retention periods must be enforced
- Sensitive data should be minimized in logs and error messages

#### 4.3.2 Cryptographic Controls

- Approved cryptographic algorithms and libraries must be used
- Cryptographic implementations must follow best practices
- Cryptographic keys must be properly managed
- Cryptographic controls must be tested thoroughly

### 4.4 Error Handling and Logging

#### 4.4.1 Error Handling

- Error handling must not expose sensitive information
- Errors must be handled gracefully
- Error messages to users should be generic
- Detailed error information should be logged securely

#### 4.4.2 Logging

- Security-relevant events must be logged
- Logs must include appropriate detail for security analysis
- Logs must be protected from unauthorized access or modification
- Sensitive data must be protected in logs

### 4.5 API Security

#### 4.5.1 API Design

- APIs must implement proper authentication and authorization
- API endpoints must validate inputs
- API responses must not expose sensitive information
- API documentation should include security considerations

#### 4.5.2 API Implementation

- API rate limiting should be implemented
- API security headers should be used
- API error responses should be security-conscious
- API security should be tested thoroughly

## 5. Secure Development Environments

### 5.1 Environment Security

#### 5.1.1 Development Environment

- Development environments must be secured appropriately
- Development environments should be isolated from production
- Developer access should follow least privilege principles
- Development credentials must not be used in production

#### 5.1.2 Testing Environment

- Test environments should mirror production security controls
- Test data must be appropriately protected
- Test environments should be regularly refreshed
- Test environment access must be controlled

### 5.2 Source Code Management

#### 5.2.1 Source Code Protection

- Source code repositories must be secured
- Access to source code must be controlled
- Source code changes must be reviewed
- Critical code components should have additional review requirements

#### 5.2.2 Secrets Management

- Credentials must not be stored in source code
- Secure secrets management solutions should be used
- Repository scanning should detect secrets in code
- Historical repository data should be cleansed of secrets

### 5.3 Continuous Integration/Continuous Deployment

#### 5.3.1 CI/CD Security

- CI/CD pipelines must include security testing
- Build environments must be secured
- Deployment automation must maintain security
- Pipeline credentials must be protected

#### 5.3.2 Security Automation

- Security testing should be automated where possible
- Security scans should block deployments for critical issues
- Automated security testing results must be reviewed
- Security automation should improve over time

## 6. Third-Party Code and Components

### 6.1 Component Management

#### 6.1.1 Component Selection

- Third-party components must be evaluated for security
- Components with known vulnerabilities must not be used
- Component sources must be verified
- Open source components must have appropriate licenses

#### 6.1.2 Component Inventory

- An inventory of third-party components must be maintained
- Component versions must be tracked
- Component updates must be evaluated and applied
- Component vulnerabilities must be monitored

### 6.2 Vulnerability Management

#### 6.2.1 Vulnerability Monitoring

- Vulnerability databases must be monitored for component issues
- Automated tools should be used to detect vulnerable components
- Vulnerability alerts must be evaluated promptly
- High-risk vulnerabilities must be addressed quickly

#### 6.2.2 Remediation

- Vulnerable components must be updated or replaced
- Mitigating controls should be implemented when updates are not available
- Vulnerability remediation must be tested
- Vulnerability remediation should be prioritized by risk

## 7. Secure Development Tools

### 7.1 Security Testing Tools

#### 7.1.1 Static Application Security Testing (SAST)

- SAST tools should be integrated into development processes
- SAST results must be reviewed and addressed
- False positives should be documented
- SAST coverage should be periodically reviewed

#### 7.1.2 Dynamic Application Security Testing (DAST)

- DAST should be performed before production deployment
- DAST tools should be configured for application-specific testing
- DAST results must be reviewed and addressed
- Critical DAST findings must be resolved before deployment

#### 7.1.3 Software Composition Analysis (SCA)

- SCA tools should scan for vulnerable components
- SCA should be integrated into development processes
- SCA results must inform component updates
- SCA coverage should include all project dependencies

### 7.2 Security Development Tools

#### 7.2.1 IDE Security Extensions

- Security extensions for IDEs should be used where available
- Security linting should be enabled
- Real-time security feedback should be leveraged
- Developer security tools should be kept updated

#### 7.2.2 Pre-commit Hooks

- Pre-commit hooks should include security checks
- Secrets detection should be implemented
- Code formatting should enforce security practices
- Pre-commit security checks should evolve over time

## 8. Cloud-Native Development Security

### 8.1 Cloud Security Design

#### 8.1.1 Cloud Architecture

- Cloud architectures must follow security best practices
- Infrastructure as Code must include security controls
- Cloud security benchmarks should be followed
- Cloud security posture should be regularly assessed

#### 8.1.2 Serverless Security

- Serverless function permissions must follow least privilege
- Serverless timeout and memory limits should be configured
- API Gateway security controls must be implemented
- Serverless code dependencies must be monitored for vulnerabilities

### 8.2 Container Security

#### 8.2.1 Container Build Security

- Container images must be built from trusted base images
- Container images should be minimal
- Container image scanning must be implemented
- Container build processes must be secured

#### 8.2.2 Container Runtime Security

- Container orchestration security controls must be implemented
- Container network controls should be restrictive
- Container privileges should be limited
- Container environments should be regularly patched

## 9. MACH Architecture Security

### 9.1 Microservices Security

#### 9.1.1 Service Design

- Microservices must be designed with security boundaries
- Service-to-service authentication must be implemented
- Service authorization should use fine-grained controls
- Service communication should be encrypted

#### 9.1.2 Service Isolation

- Services should be isolated from each other
- Service compromise should not affect other services
- Service dependencies should be minimized
- Service environments should be consistent

### 9.2 API-First Security

#### 9.2.1 API Gateway Security

- API gateways must implement security controls
- API authentication must be robust
- API traffic should be monitored
- API documentation should address security

#### 9.2.2 API Management

- API versioning should consider security improvements
- API deprecation should address security concerns
- API access should be controlled centrally
- API security standards should be consistent

### 9.3 Cloud-Native Security

#### 9.3.1 Cloud Provider Security

- Cloud provider security features should be leveraged
- Cloud security posture management should be implemented
- Cloud service configurations must be secured
- Cloud security should be regularly assessed

#### 9.3.2 Multi-Cloud Security

- Security controls must be consistent across cloud providers
- Identity and access should be centrally managed
- Security monitoring should span all environments
- Security standards should apply to all cloud services

### 9.4 Headless Architecture Security

#### 9.4.1 Frontend Security

- Frontend applications must implement appropriate security controls
- Client-side security best practices must be followed
- API connections must be secured
- Frontend vulnerabilities must be addressed

#### 9.4.2 Backend Security

- Headless services must be properly secured
- Service authentication must be robust
- Content delivery must be secured
- Backend services must be protected from direct access

## 10. Security Testing and Verification

### 10.1 Testing Approaches

#### 10.1.1 Security Unit Testing

- Security functionality should have unit test coverage
- Security unit tests should verify both positive and negative cases
- Security unit tests should be automated
- Security unit tests should be maintained over time

#### 10.1.2 Security Integration Testing

- Integration testing should verify security between components
- Authentication and authorization should be tested across boundaries
- Data protection should be verified through integration points
- Security integration tests should be automated where possible

#### 10.1.3 Security Acceptance Testing

- Security acceptance criteria must be defined
- Security acceptance testing must verify security requirements
- Security acceptance testing should include manual testing
- Security acceptance testing results must be documented

### 10.2 Vulnerability Assessment

#### 10.2.1 Internal Assessment

- Regular vulnerability assessments must be conducted
- Vulnerability assessment tools should be used
- Vulnerability assessment findings must be addressed
- Vulnerability assessment coverage must be comprehensive

#### 10.2.2 External Assessment

- Periodic external security assessments should be performed
- Penetration testing should be conducted for high-risk applications
- External assessment findings must be prioritized
- External assessment recommendations should be implemented

## 11. Client Project Security

### 11.1 Client Security Requirements

#### 11.1.1 Requirement Analysis

- Client security requirements must be documented
- Compliance requirements must be identified
- Security responsibilities must be clarified
- Security exceptions must be approved and documented

#### 11.1.2 Security Implementation

- Client security requirements must be mapped to controls
- Client-specific security testing should be performed
- Client security approvals should be obtained
- Client security documentation should be maintained

### 11.2 Client-Specific Controls

#### 11.2.1 Customized Security

- Client-specific security controls should be implemented as required
- Deviations from standard security practices must be documented
- Client-specific security requirements should be validated
- Client security expectations should be aligned with implementations

#### 11.2.2 Client Security Validation

- Client security validation should be performed
- Client security acceptance should be documented
- Client security concerns must be addressed
- Client security handover should be comprehensive

## 12. Training and Awareness

### 12.1 Developer Security Training

#### 12.1.1 Core Training

- Developers must receive secure coding training
- Training should be relevant to technologies used
- Security training should be updated regularly
- Security training completion should be tracked

#### 12.1.2 Ongoing Education

- Security knowledge sharing should be encouraged
- Security updates should be communicated to developers
- Security champions should be identified and supported
- Security self-education should be promoted

### 12.2 Security Resources

#### 12.2.1 Documentation

- Secure development guidelines should be maintained
- Security controls should be documented
- Security lessons learned should be shared
- Security resources should be accessible to all developers

#### 12.2.2 Knowledge Base

- Common security issues should be documented
- Security solutions should be shared
- Security patterns should be established
- Security knowledge base should be maintained

## 13. Secure Development Metrics

### 13.1 Security Defect Metrics

#### 13.1.1 Defect Tracking

- Security defects must be tracked
- Security defect trends should be analyzed
- Security defect categories should be identified
- Security defect resolution times should be measured

#### 13.1.2 Security Debt

- Security technical debt should be tracked
- Security debt reduction should be prioritized
- Security debt should inform improvement initiatives
- Security debt metrics should be reported

### 13.2 Process Metrics

#### 13.2.1 Security Activity Metrics

- Security testing coverage should be measured
- Security review participation should be tracked
- Security training completion should be monitored
- Security tool usage should be assessed

#### 13.2.2 Improvement Metrics

- Security improvement initiatives should be measured
- Security maturity should be assessed
- Security process adherence should be evaluated
- Security culture should be assessed

## 14. Exceptions

Exceptions to this policy may be granted only after a documented risk assessment and formal approval by the Development Manager or CTO. All exceptions must be:

- Documented using the Security Exception Request Form (ISMS-FORM-05)
- Time-limited with a defined expiration date
- Reviewed periodically for continued necessity
- Accompanied by compensating controls where appropriate

## 15. Responsibilities

### 15.1 Developers

- Implement secure coding practices
- Participate in security code reviews
- Address identified security issues
- Maintain security knowledge

### 15.2 Development Team Leads

- Ensure security is addressed in development
- Review code for security issues
- Promote security best practices
- Support security improvements

### 15.3 Development Manager

- Maintain this policy
- Ensure security is integrated into development processes
- Provide resources for security activities
- Report on secure development metrics

### 15.4 Security Manager

- Provide security guidance to development teams
- Review security testing results
- Support security incident response
- Promote security awareness

## 16. Policy Review

This policy will be reviewed annually or when significant changes occur to ensure it remains aligned with business requirements, technology changes, and security best practices.

## 17. Related Documents

- [Information Security Management Policy]({{ site.baseurl }}/policies/isms-pol-01/)
- [Data Protection & Classification Policy]({{ site.baseurl }}/policies/isms-pol-02/)
- [Incident Management Policy]({{ site.baseurl }}/policies/isms-pol-04/)
- [Secure Client Engagement Procedure]({{ site.baseurl }}/procedures/isms-proc-02/)
- ISMS-GUIDE-03: Secure Development Handbook
- ISMS-FORM-05: Security Exception Request Form

---

_By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Secure Development Policy._
