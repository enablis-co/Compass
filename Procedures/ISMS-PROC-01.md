---
layout: page
title: "Risk Assessment Procedure"
permalink: /procedures/isms-proc-01/
---

**Document ID**: ISMS-PROC-01  
**Version**: 1.0  
**Last Updated**: February 25, 2025  
**Owner**: Chief Technology Officer  
**Approved by**: Board of Directors

## 1. Purpose and Scope

### 1.1 Purpose

This Risk Assessment Procedure establishes a practical, consistent approach for identifying, analyzing, and evaluating information security risks at Enablis. It enables informed decision-making about risk treatment while maintaining operational efficiency.

### 1.2 Scope

This procedure applies to:

- All information security risk assessments conducted at Enablis
- Risk assessments for internal operations and client projects
- All personnel involved in risk assessment activities
- All information assets owned or managed by Enablis

## 2. Definitions

| Term           | Definition                                                                                    |
| -------------- | --------------------------------------------------------------------------------------------- |
| Risk           | The effect of uncertainty on objectives, expressed in terms of likelihood and impact          |
| Threat         | A potential cause of an unwanted incident that may result in harm to a system or organization |
| Vulnerability  | A weakness that can be exploited by one or more threats                                       |
| Risk Owner     | The person or entity with the accountability and authority to manage a risk                   |
| Risk Treatment | The process to modify risk through avoidance, reduction, transfer, or acceptance              |
| Residual Risk  | The risk remaining after risk treatment                                                       |

## 3. Roles and Responsibilities

### 3.1 Security Manager

- Oversees the risk assessment process
- Provides guidance on risk assessment methodology
- Reviews completed risk assessments
- Reports significant risks to senior management

### 3.2 Risk Assessor

- Conducts risk assessment activities
- Documents identified risks
- Collaborates with stakeholders during the assessment
- Provides recommendations for risk treatment

### 3.3 Risk Owners

- Provide input on risk identification and analysis
- Approve risk treatment plans for their areas of responsibility
- Implement risk treatments
- Monitor ongoing risk status

### 3.4 Chief Technology Officer

- Reviews significant risks
- Approves risk acceptance for high risks
- Allocates resources for risk treatment
- Ensures integration of risk management with business strategy

## 4. Risk Assessment Process

### 4.1 Risk Assessment Planning

#### 4.1.1 Assessment Scope

Define the scope of the risk assessment, including:

- Systems, applications, or processes to be assessed
- Locations and organizational units
- Time period for the assessment
- Dependencies and interfaces

#### 4.1.2 Assessment Team

Identify the personnel who will conduct the assessment, considering:

- Required technical expertise
- Knowledge of the systems or processes
- Independence from the area being assessed
- Availability during the assessment period

#### 4.1.3 Assessment Schedule

Establish a timeline for assessment activities, including:

- Kickoff meeting
- Information gathering
- Analysis
- Validation
- Reporting
- Review

### 4.2 Risk Identification

#### 4.2.1 Information Gathering

Collect relevant information through:

- Stakeholder interviews
- Document reviews
- System configuration analysis
- Previous assessment results
- Vulnerability scans and penetration test results
- Incident history

#### 4.2.2 Threat Identification

Identify relevant threat sources and types, including:

- External threats (hackers, competitors, natural disasters)
- Internal threats (employees, contractors)
- Technical threats (malware, system failures)
- Process threats (human error, inadequate procedures)

#### 4.2.3 Vulnerability Identification

Identify vulnerabilities that could be exploited, including:

- Technical vulnerabilities (unpatched systems, misconfigurations)
- Process vulnerabilities (lack of verification, unclear responsibilities)
- People vulnerabilities (lack of awareness, insufficient training)
- Physical vulnerabilities (inadequate physical security)

#### 4.2.4 Asset Identification

Identify and value assets within the assessment scope, including:

- Information assets (data, intellectual property)
- System assets (hardware, software, services)
- People assets (key personnel, specialized skills)
- Reputational assets (brand value, client trust)

### 4.3 Risk Analysis

#### 4.3.1 Likelihood Assessment

Evaluate the likelihood of risks materializing using the following scale:

| Level              | Description                                 | Criteria                     |
| ------------------ | ------------------------------------------- | ---------------------------- |
| 1 - Rare           | May occur only in exceptional circumstances | Less than once every 5 years |
| 2 - Unlikely       | Could occur at some time                    | Once every 2-5 years         |
| 3 - Possible       | Might occur at some time                    | Once every 1-2 years         |
| 4 - Likely         | Will probably occur in most circumstances   | Several times per year       |
| 5 - Almost Certain | Expected to occur in most circumstances     | Monthly or more frequently   |

When assessing likelihood, consider:

- Historical occurrence
- Threat motivation and capability
- Vulnerability exploitability
- Existing controls

#### 4.3.2 Impact Assessment

Evaluate the potential impact if risks materialize using the following scale:

| Level             | Description                                    | Criteria                                                                                                                                       |
| ----------------- | ---------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| 1 - Insignificant | Minimal impact with no disruption              | - No financial loss<br>- No operational disruption<br>- No compliance impact<br>- No reputational damage                                       |
| 2 - Minor         | Minor impact with limited disruption           | - Financial loss < $10,000<br>- Brief operational disruption<br>- Minor compliance issues<br>- Limited reputational damage                     |
| 3 - Moderate      | Moderate impact with noticeable disruption     | - Financial loss $10,000-$50,000<br>- Partial operational disruption<br>- Reportable compliance issues<br>- Local reputational damage          |
| 4 - Major         | Significant impact with substantial disruption | - Financial loss $50,000-$250,000<br>- Major operational disruption<br>- Significant compliance violations<br>- Widespread reputational damage |
| 5 - Severe        | Critical impact with severe disruption         | - Financial loss > $250,000<br>- Critical operational failure<br>- Severe compliance violations<br>- Major long-term reputational damage       |

When assessing impact, consider effects on:

- Confidentiality, integrity, and availability of information
- Financial position
- Operational capability
- Legal and regulatory compliance
- Reputation and client relationships

#### 4.3.3 Risk Level Determination

Calculate the risk level by multiplying the likelihood and impact scores:

| Risk Score | Risk Level | Description                                                  |
| ---------- | ---------- | ------------------------------------------------------------ |
| 1-4        | Low        | Acceptable risk; manage by routine procedures                |
| 5-10       | Medium     | Attention needed; specific monitoring or procedures required |
| 11-19      | High       | Significant risk; senior management attention needed         |
| 20-25      | Critical   | Unacceptable risk; immediate action required                 |

### 4.4 Risk Evaluation

#### 4.4.1 Risk Prioritization

Prioritize risks based on:

- Risk level (Critical, High, Medium, Low)
- Alignment with business objectives
- Implementation feasibility of risk treatments
- Resource requirements for mitigation

#### 4.4.2 Risk Acceptance Criteria

Apply the following risk acceptance criteria:

| Risk Level | Approval Required | Review Frequency      |
| ---------- | ----------------- | --------------------- |
| Low        | Risk Assessor     | Annually              |
| Medium     | Security Manager  | Semi-annually         |
| High       | CTO               | Quarterly             |
| Critical   | CEO               | Monthly until reduced |

#### 4.4.3 Risk Response Strategy

Determine the appropriate risk response strategy:

- **Avoid**: Eliminate the risk by removing the risk source
- **Mitigate**: Reduce likelihood or impact through controls
- **Transfer**: Share the risk with another party (e.g., insurance)
- **Accept**: Retain the risk with informed decision-making

### 4.5 Risk Treatment

#### 4.5.1 Treatment Planning

For risks requiring treatment, document:

- Selected risk treatment options
- Required controls to be implemented
- Resource requirements
- Responsibilities and timelines
- Performance measures
- Constraints and dependencies

#### 4.5.2 Residual Risk

After planning treatment:

- Estimate the residual risk level
- Evaluate if residual risk meets acceptance criteria
- Determine if additional treatments are needed
- Document acceptance of residual risk

### 4.6 Risk Documentation and Reporting

#### 4.6.1 Risk Register

Maintain a risk register containing:

- Risk ID and description
- Affected assets
- Threat and vulnerability information
- Inherent risk level (likelihood and impact)
- Existing controls
- Planned treatments
- Residual risk level
- Risk owner
- Status and review dates

#### 4.6.2 Risk Assessment Report

Prepare a risk assessment report including:

- Executive summary
- Assessment scope and objectives
- Methodology used
- Key findings and significant risks
- Risk treatment recommendations
- Conclusions and next steps

## 5. Project Risk Assessments

### 5.1 Initiation Phase Assessment

#### 5.1.1 Preliminary Assessment

Conduct a high-level assessment during project initiation to:

- Identify major risk categories relevant to the project
- Determine if a detailed assessment is required
- Identify client-specific security requirements
- Incorporate security considerations into project planning

#### 5.1.2 Client Requirements Analysis

When assessing client projects:

- Review client security policies and requirements
- Identify compliance obligations
- Determine client risk acceptance criteria
- Document client-specific risk considerations

### 5.2 Development Risk Assessment

#### 5.2.1 Design Phase Assessment

Assess risks during the design phase focusing on:

- Architecture and design security
- Technology selection risks
- Integration points and dependencies
- Security control design

#### 5.2.2 Implementation Phase Assessment

Assess risks during implementation focusing on:

- Secure coding and configuration
- Test environment security
- Third-party component risks
- Development process security

### 5.3 Deployment Risk Assessment

#### 5.3.1 Pre-Deployment Assessment

Before deployment, assess:

- Production environment security
- Deployment process security
- Operational support readiness
- Security testing completion and results

#### 5.3.2 Post-Deployment Validation

After deployment, validate:

- Implemented security controls
- Operational security procedures
- Monitoring and incident response capabilities
- Compliance with requirements

## 6. Simplified Risk Assessment

### 6.1 Rapid Risk Assessment

For lower-risk scenarios or time-sensitive situations:

#### 6.1.1 Rapid Assessment Process

1. Identify key assets and threats
2. Evaluate risks using simplified High/Medium/Low ratings
3. Determine immediate actions required
4. Document basic findings
5. Schedule comprehensive assessment if needed

#### 6.1.2 Rapid Assessment Template

Use the Rapid Risk Assessment Template (ISMS-FORM-06) for simplified assessments, capturing:

- Core assets and functionality
- Key threats and vulnerabilities
- Risk levels
- Immediate actions
- Approval for continued operation

### 6.2 Change Risk Assessment

#### 6.2.1 Change Risk Evaluation

For system or process changes:

1. Identify security implications of the change
2. Assess potential impact on existing security controls
3. Determine if additional controls are needed
4. Document findings in the change management system

#### 6.2.2 Change Approval

Risk assessment results must be considered in change approval decisions, with:

- Low-risk changes approved by the change manager
- Medium-risk changes requiring security review
- High-risk changes requiring CTO approval

## 7. Risk Monitoring and Review

### 7.1 Risk Review Schedule

Review risks according to:

- Scheduled intervals based on risk level
- After significant changes to systems or processes
- Following security incidents
- When new threats or vulnerabilities emerge

### 7.2 Key Risk Indicators

Monitor key risk indicators such as:

- Vulnerability scan results
- Security incident frequency
- Control effectiveness metrics
- Compliance status
- External threat intelligence

### 7.3 Risk Status Updates

Update the risk register with:

- Changes to risk levels
- Treatment implementation status
- Emerging risks
- Closed or accepted risks
- Treatment effectiveness

## 8. Tools and Templates

### 8.1 Risk Assessment Matrix

Use the Risk Assessment Matrix (ISMS-FORM-01) to document and calculate risk levels based on likelihood and impact.

### 8.2 Risk Register

Maintain risks in the Risk Register (ISMS-FORM-07), updated throughout the risk management process.

### 8.3 Risk Treatment Plan

Document risk treatments in the Risk Treatment Plan (ISMS-FORM-08), including actions, owners, and timelines.

## 9. Procedure Review

This procedure will be reviewed annually or when significant changes occur to ensure it remains effective and aligned with business requirements.

## 10. Related Documents

- ISMS-POL-01: Information Security Management Policy
- ISMS-FORM-01: Risk Assessment Matrix
- ISMS-FORM-06: Rapid Risk Assessment Template
- ISMS-FORM-07: Risk Register
- ISMS-FORM-08: Risk Treatment Plan

---

_By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Risk Assessment Procedure._
