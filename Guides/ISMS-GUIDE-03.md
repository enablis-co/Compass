---
layout: page
title: "Secure Development Handbook"
permalink: /guides/isms-guide-03/
---

**Document ID**: ISMS-GUIDE-03  
**Version**: 1.0  
**Last Updated**: February 27, 2025  
**Owner**: Chief Technology Officer  
**Approved by**: Board of Directors

## 1. Introduction

### 1.1 Purpose

This handbook provides practical guidance for building secure applications and systems at Enablis. It offers principles and approaches to help developers integrate security throughout the software development lifecycle.

### 1.2 Security by Design Philosophy

At Enablis, we believe in building security in from the start, not bolting it on later. This means:

- Considering security requirements during initial design
- Including security activities in each development phase
- Making security a natural part of development
- Automating security checks where possible

## 2. Secure Design Principles

### 2.1 Core Security Principles

#### Defense in Depth

Implement multiple security controls so that if one fails, others will still provide protection.

#### Least Privilege

Grant the minimum access necessary to perform a function.

#### Secure Defaults

Make the default configuration secure, requiring explicit actions to reduce security.

#### Fail Secure

When a system fails or encounters an error, it should default to a secure state.

### 2.2 Threat Modeling

#### Simplified Threat Modeling Approach

1. **Identify assets**: What are you protecting?
2. **Create a system diagram**: How does data flow through the system?
3. **Identify threats**: What could go wrong?
4. **Mitigate risks**: How will you address the threats?
5. **Validate**: Did you miss anything?

Use the STRIDE framework to identify threats:

- **S**poofing
- **T**ampering
- **R**epudiation
- **I**nformation disclosure
- **D**enial of service
- **E**levation of privilege

#### MACH Architecture Considerations

When working with MACH architecture (Microservices, API-first, Cloud-native, Headless), consider:

**Microservices Security:**

- Service-to-service authentication
- API gateway security
- Service boundary protection

**API Security:**

- API authentication and authorization
- Input validation and output encoding
- Rate limiting and throttling

**Cloud-Native Security:**

- Container security
- Serverless function security
- Infrastructure as code security

**Headless Security:**

- Frontend/backend separation security
- Cross-site scripting protection
- Authentication token handling

## 3. Secure Coding Practices

### 3.1 Input Validation

- Validate all input regardless of source
- Use allowlist validation rather than blocklist
- Validate data type, length, format, and range
- Apply validation server-side (client-side is for UX only)
- Use structured data validation libraries when possible

### 3.2 Authentication and Authorization

#### Authentication Best Practices

- Use multi-factor authentication where possible
- Implement secure password handling
- Use time-limited authentication tokens
- Implement secure session management

#### Authorization Patterns

- Implement role-based access control (RBAC)
- Centralize authorization logic
- Validate authorization at each request
- Implement least privilege by default

### 3.3 Data Protection

#### Encryption Best Practices

- Use modern, standard encryption algorithms
- Don't implement custom encryption
- Use appropriate key management
- Implement encryption at rest and in transit

#### Sensitive Data Handling

- Identify and classify sensitive data
- Minimize sensitive data collection and storage
- Implement appropriate access controls
- Apply data masking for display

### 3.4 Error Handling and Logging

#### Secure Error Handling

- Never expose sensitive information in error messages
- Implement different error handling for development and production
- Use generic error messages for users
- Log detailed errors for debugging

#### Secure Logging

- Never log sensitive data (passwords, tokens, PII)
- Implement appropriate log levels
- Structure logs for better analysis
- Secure log storage and transmission

### 3.5 API Security

#### RESTful API Security

- Implement proper authentication and authorization
- Use HTTPS for all API endpoints
- Apply rate limiting and throttling
- Validate all input and sanitize output

#### GraphQL Security

- Implement depth and complexity limits
- Apply query whitelisting for production
- Use persisted queries when possible
- Implement proper authorization at field level

## 4. Common Vulnerability Prevention

### 4.1 Injection Prevention

#### SQL Injection

Prevention techniques:

- Use parameterized queries or prepared statements
- Implement ORM libraries with proper escaping
- Apply input validation
- Apply least privilege database accounts

#### NoSQL Injection

Prevention techniques:

- Use parameterized queries
- Apply input validation and sanitization
- Avoid using string operations to build queries
- Use typed operators instead of interpolated strings

#### Command Injection

Prevention techniques:

- Avoid executing system commands when possible
- Use libraries/APIs instead of shell commands
- Apply strict input validation
- Use parameterized commands with arguments

### 4.2 Cross-Site Scripting (XSS) Prevention

Prevention techniques:

- Implement context-appropriate output encoding
- Use Content Security Policy (CSP)
- Apply input validation
- Use modern frameworks that automatically escape output

### 4.3 Cross-Site Request Forgery (CSRF) Prevention

Prevention techniques:

- Implement anti-CSRF tokens
- Use SameSite cookie attribute
- Verify origin and referrer headers
- Require re-authentication for sensitive operations

### 4.4 Security Headers and Configurations

- Implement appropriate security headers
- Apply secure cookie settings
- Configure proper CORS policies
- Use HTTPS with secure TLS configuration

## 5. Security Testing

### 5.1 Testing Approaches

- Integrate security testing into CI/CD pipeline
- Perform automated SAST, DAST, and SCA
- Conduct regular manual security testing
- Include security in code reviews

### 5.2 Automated Security Testing

- Static Application Security Testing (SAST)
- Dynamic Application Security Testing (DAST)
- Software Composition Analysis (SCA)
- Container security scanning

## 6. Secure DevOps Practices

### 6.1 Security in CI/CD

- Automate security checks in build and deployment pipelines
- Establish security gates with appropriate thresholds
- Manage secrets securely in CI/CD processes
- Implement secure artifact management

### 6.2 Infrastructure as Code Security

- Use template security scanning
- Implement least privilege principles in infrastructure
- Apply network security controls
- Secure cloud service configurations

## 7. Security Response

### 7.1 Vulnerability Management

- Establish a vulnerability reporting process
- Define vulnerability assessment criteria
- Implement a patch management process
- Conduct regular security assessments

### 7.2 Incident Response

- Prepare an incident response plan
- Define security incident criteria
- Establish an incident response team
- Document and learn from incidents

## 8. Resources

### 8.1 Security Tools

- SAST: SonarQube, ESLint Security
- DAST: OWASP ZAP, Burp Suite
- SCA: Snyk, OWASP Dependency Check
- Secret scanning: GitLeaks, TruffleHog

### 8.2 Security References

- OWASP Top 10
- NIST Secure Software Development Framework
- OWASP Application Security Verification Standard
