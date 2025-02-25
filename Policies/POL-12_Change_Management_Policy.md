# Enablis Change Management Policy

**Document ID**: POL-12  
**Version**: 1.0  
**Last Updated**: February 24, 2025  
**Owner**: IT Operations Manager  
**Approved by**: Chief Technology Officer  

## 1. Purpose and Scope

### 1.1 Purpose
This Change Management Policy establishes the framework for managing changes to Enablis systems, infrastructure, applications, and processes in a controlled, efficient manner. It ensures that changes support business objectives while minimizing risk, disruption, and unintended consequences to our operations and client services.

### 1.2 Scope
This policy applies to:
- All changes to information systems, network infrastructure, and applications owned or managed by Enablis
- All changes to client systems managed by Enablis
- All employees, contractors, and temporary staff involved in implementing changes
- All environments including development, testing, staging, and production
- All locations from which changes are implemented, including remote environments

## 2. Change Management Principles

### 2.1 Balance Control with Agility
Change management processes should provide appropriate control without unnecessarily impeding innovation or delivery timelines. The level of control should be proportionate to the risk and impact of the change.

### 2.2 Informed Decision Making
Change decisions should be based on complete information about risks, benefits, resource requirements, and business impacts. Stakeholders should have visibility into planned changes that may affect them.

### 2.3 Segregation of Duties
Where practical, changes should be separated into those who request, approve, develop, test, and implement to maintain appropriate checks and balances.

### 2.4 Continuous Improvement
Change management processes should be regularly reviewed and refined based on feedback and outcomes to improve effectiveness and efficiency.

### 2.5 Technical Excellence
Changes should maintain or improve technical quality and adhere to established architectural principles, security standards, and best practices.

## 3. Change Types and Classification

### 3.1 Change Types

#### 3.1.1 Standard Change
Pre-approved, routine changes with established procedures, known risks, and predictable outcomes. Examples include:
- Scheduled patches with established testing procedures
- User account management following established processes
- Minor configuration adjustments within defined parameters

#### 3.1.2 Normal Change
Changes that require risk assessment and formal approval before implementation. Examples include:
- System upgrades or major version changes
- New software deployments
- Network configuration changes
- Infrastructure modifications

#### 3.1.3 Emergency Change
Changes that must be implemented urgently to resolve critical issues such as:
- Security vulnerabilities requiring immediate patching
- System outages affecting business operations
- Performance issues severely impacting service delivery
- Issues directly affecting client services

### 3.2 Change Impact Classification

Changes shall be classified according to their potential impact:

| Impact Level | Description | Examples |
|--------------|-------------|----------|
| High | Affects critical systems or multiple users/clients | - Core infrastructure changes<br>- Major application upgrades<br>- Changes affecting multiple client environments |
| Medium | Affects individual systems or limited user groups | - Single application updates<br>- Departmental system changes<br>- Individual client environment changes |
| Low | Minimal or isolated impact | - Minor configuration changes<br>- Individual workstation updates<br>- Non-critical system adjustments |

### 3.3 Change Risk Assessment

Risk assessment should consider:
- Potential for service disruption
- Security implications
- Data integrity impacts
- Compliance considerations
- Recovery complexity if issues occur
- Resource dependencies

## 4. Change Management Roles and Responsibilities

### 4.1 Change Initiator
- Identifies need for change
- Documents change requirements
- Submits change requests
- Provides additional information as needed

### 4.2 Change Manager
- Coordinates the change management process
- Facilitates Change Advisory Board meetings
- Ensures changes are properly documented and communicated
- Reports on change management metrics
- Identifies process improvements

### 4.3 Change Advisory Board (CAB)
- Reviews and approves normal changes
- Assesses risks and impacts
- Evaluates resource requirements
- Recommends implementation strategies
- Reviews post-implementation results

### 4.4 Emergency Change Advisory Board (ECAB)
- Expedites review and approval of emergency changes
- Available outside normal business hours when needed
- Includes key technical and business decision makers

### 4.5 Technical Implementers
- Develop and execute technical aspects of changes
- Test changes before implementation
- Document technical details of changes
- Implement approved changes
- Participate in post-implementation reviews

## 5. Change Management Process

### 5.1 Request and Documentation
All changes must be formally requested and documented with:
- Clear description and justification
- Systems and services affected
- Expected benefits and outcomes
- Estimated resource requirements
- Proposed implementation timing
- Rollback or contingency plans
- Testing requirements

### 5.2 Assessment and Planning
Changes must be assessed for:
- Technical feasibility
- Potential risks and impacts
- Resource requirements
- Dependencies on other systems or changes
- Testing approach
- Implementation schedule

### 5.3 Approval Process

#### 5.3.1 Standard Change Approval
- Reviewed against standard change criteria
- Approved by designated authority for the change type
- Documented in change management system

#### 5.3.2 Normal Change Approval
- Reviewed by Change Advisory Board
- Approval based on risk, impact, and business value
- Scheduled in the forward schedule of changes

#### 5.3.3 Emergency Change Approval
- Expedited review by Emergency CAB or designated approvers
- Minimum required documentation to enable quick decision
- Post-implementation documentation completed retrospectively

### 5.4 Testing Requirements
Changes must be tested before implementation to verify:
- Functionality works as intended
- No adverse effects on dependent systems
- Performance meets requirements
- Security is maintained or enhanced
- Recovery procedures are effective

### 5.5 Implementation Planning
Implementation plans must include:
- Detailed implementation steps
- Resource assignments and responsibilities
- Communication plan for affected stakeholders
- Scheduled maintenance window if required
- Validation criteria for success
- Rollback procedures

### 5.6 Post-Implementation Review
After implementation, changes must be reviewed to:
- Confirm successful implementation
- Document any issues encountered
- Validate that objectives were met
- Identify lessons learned
- Update documentation and knowledge base
- Close the change record

## 6. Change Windows and Scheduling

### 6.1 Standard Change Windows
- Regular maintenance windows should be established for routine changes
- Change windows should be communicated to all stakeholders
- Changes should be scheduled to minimize business impact

### 6.2 Blackout Periods
- Periods where changes are restricted should be identified
- Critical business periods should be protected from non-essential changes
- Client-specific blackout periods should be respected

### 6.3 Change Calendar
- A forward schedule of changes should be maintained
- Potential conflicts should be identified and resolved
- Dependencies between changes should be managed

## 7. Client Environment Changes

### 7.1 Client-Specific Requirements
- Client change management requirements must be documented
- Client approval processes must be followed when required
- Client communication plans must be established

### 7.2 Service Level Agreements
- Changes must comply with client SLAs
- Change windows must align with agreed service parameters
- Change notifications must meet contractual requirements

### 7.3 Client Communication
- Clients must be notified of changes according to agreed timeframes
- Communication should include purpose, timing, impact, and contact information
- Post-change confirmation should be provided when appropriate

## 8. Emergency Change Management

### 8.1 Emergency Process
- Streamlined process for urgent changes
- Minimum required approvals clearly defined
- 24/7 access to emergency approvers
- Prioritization over non-emergency changes

### 8.2 Post-Emergency Documentation
- Complete documentation must be created retrospectively
- Normal change process must be followed post-implementation
- Root cause analysis should be conducted when appropriate

### 8.3 Emergency Communication
- Communication templates should be prepared in advance
- Escalation paths should be clearly defined
- Status updates should be provided at regular intervals

## 9. Change Management Tools and Documentation

### 9.1 Change Management System
- All changes must be recorded in the approved change management system
- The system must maintain the status and history of all changes
- Access to the system must be controlled based on roles
- The system should support reporting and metrics

### 9.2 Documentation Requirements
- Change requests, approvals, and implementations must be documented
- Technical details must be captured for knowledge retention
- System and configuration documentation must be updated following changes
- Change records must be retained according to retention requirements

### 9.3 Knowledge Management
- Lessons learned should be captured and shared
- Common issues and solutions should be documented
- Technical documentation should be kept current
- Change patterns should be analyzed for process improvement

## 10. Release Management

### 10.1 Release Planning
- Related changes should be grouped into coordinated releases when appropriate
- Release schedules should be communicated in advance
- Release dependencies should be identified and managed
- Resource requirements should be planned accordingly

### 10.2 Release Testing
- Releases should be tested as an integrated unit
- Performance and security testing should be included
- User acceptance testing should be conducted when appropriate
- Test environments should mirror production where possible

### 10.3 Release Deployment
- Deployment plans should detail the sequence of changes
- Rollback points should be identified
- Verification steps should be defined
- Post-deployment support should be arranged

## 11. Change Management for Development Projects

### 11.1 Development Lifecycle Integration
- Change management should be integrated with the development lifecycle
- Project transition to operations should include change management planning
- Development teams should understand change requirements

### 11.2 DevOps Considerations
- Automated deployment pipelines should incorporate change controls
- Continuous integration/continuous deployment (CI/CD) should maintain appropriate approvals
- Change management should support rather than impede agile practices

### 11.3 Infrastructure as Code
- Infrastructure as Code changes should follow change management processes
- Version control systems should be integrated with change management
- Infrastructure code should be tested before deployment

## 12. Training and Awareness

### 12.1 Staff Training
- All relevant staff should receive change management training
- Role-specific training should be provided
- Training materials should be updated when processes change

### 12.2 Process Awareness
- Change management processes should be clearly communicated
- Benefits of proper change management should be emphasized
- Regular reminders and updates should be provided

## 13. Monitoring and Compliance

### 13.1 Metrics and Reporting
Key metrics should be tracked:
- Volume of changes by type and category
- Success/failure rates of changes
- Change-related incidents
- Emergency change frequency
- Process compliance

### 13.2 Audit and Review
- Regular audits of change management processes should be conducted
- Compliance with this policy should be verified
- Process effectiveness should be assessed
- Improvement opportunities should be identified

## 14. Exceptions

Exceptions to this policy may be granted only after a documented risk assessment and formal approval by the IT Operations Manager or CTO. All exceptions must be:
- Documented with a clear business justification
- Time-limited with a defined expiration date
- Reviewed periodically for continued necessity

## 15. Policy Compliance

### 15.1 Verification
Compliance with this policy will be verified through:
- Change management system audits
- Process reviews
- Post-implementation checks
- Regular reporting

### 15.2 Consequences of Non-Compliance
Failures to comply with this policy may result in:
- Additional oversight or controls
- Process remediation
- Training requirements
- Disciplinary action in accordance with HR policies

## 16. Policy Review

This policy will be reviewed annually or when significant changes occur to ensure it remains aligned with business requirements, technological developments, and best practices.

## 17. Related Documents

- POL-01: Information Security Policy
- POL-08: Incident Management Policy
- DOC-09: Business Continuity Plan
- DOC-28: Change Request Template
- DOC-29: Change Management Procedure
- DOC-30: Emergency Change Procedure

---

*By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Change Management Policy.*