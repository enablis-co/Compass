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

This policy establishes the high-level requirements for secure software development at Enablis. It applies to all software development activities, employees, contractors, and third parties involved in development.

## 2. Core Principles

- Security by Design: Security must be integrated from the start
- Defense in Depth: Multiple layers of security controls are required
- Least Privilege: Systems must operate with minimum necessary privileges
- Secure Defaults: Security settings must be secure by default
- Fail Secure: Systems must maintain security during failures
- Continuous Improvement: Security practices must evolve with threats

## 3. Key Requirements

### 3.1 Secure Development Lifecycle

- Security requirements must be defined during planning
- Threat modeling must be performed for sensitive applications
- Secure architecture and design patterns must be applied
- Code must follow secure coding standards
- Security testing must be performed before release
- Production deployments must include security validation
- Security patches must be applied promptly

### 3.2 Security Controls

- Strong authentication and authorization controls are required
- All user input must be validated and outputs encoded
- Sensitive data must be encrypted in transit and at rest
- Errors must be handled securely without exposing details
- Security events must be logged appropriately
- APIs must implement comprehensive security controls

### 3.3 Development Environment

- Development environments must be secured and isolated
- Source code must be protected with access controls
- Secrets must not be stored in code repositories
- CI/CD pipelines must include security testing
- Third-party components must be security-vetted

### 3.4 Cloud and MACH Security

- Cloud services must follow security best practices
- Microservices must maintain security boundaries
- API gateways must enforce security controls
- Container security must be implemented

## 4. Responsibilities

- Developers: Implement secure coding practices
- Team Leads: Ensure security in development processes
- Development Manager: Maintain policy and provide resources
- Security Manager: Provide guidance and review security

## 5. Exceptions

Exceptions require documented risk assessment and CTO approval using ISMS-FORM-05.

## 6. Related Documents

- [Information Security Management Policy]({{ site.baseurl }}/policies/isms-pol-01/)
- [Data Protection & Classification Policy]({{ site.baseurl }}/policies/isms-pol-02/)
- [Incident Management Policy]({{ site.baseurl }}/policies/isms-pol-04/)
- [Secure Client Engagement Procedure]({{ site.baseurl }}/procedures/isms-proc-02/)
- ISMS-GUIDE-03: Secure Development Handbook
- ISMS-FORM-05: Security Exception Request Form

---

_By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Secure Development Policy._
