# Enablis Approved Software List

**Document ID**: DOC-14  
**Version**: 1.0  
**Last Updated**: February 24, 2025  
**Owner**: IT Operations Manager  
**Approved by**: Chief Technology Officer

## 1. Introduction

### 1.1 Purpose

This Approved Software List identifies software applications and tools that have been evaluated and approved for use within Enablis. It ensures that software used across the organization meets our security, compatibility, and licensing requirements while supporting our technical excellence and business objectives.

### 1.2 Scope

This document applies to:

- All software installed on Enablis-owned devices
- All cloud services and SaaS applications used for Enablis business
- Development tools and platforms used for client projects
- All employees, contractors, and temporary staff using software for Enablis business

### 1.3 Software Approval Process

New software requests must follow the Software Request and Approval Procedure (DOC-37). The approval process considers:

- Security requirements and risk assessment
- Business need and use case
- Compatibility with existing systems
- Licensing and cost implications
- Support and maintenance requirements
- Alignment with technical strategy

## 2. Operating Systems

### 2.1 Desktop and Laptop Operating Systems

| Software       | Version(s)            | Use Case                                  | Security Requirements                                               | Notes                                     |
| -------------- | --------------------- | ----------------------------------------- | ------------------------------------------------------------------- | ----------------------------------------- |
| Windows 11 Pro | 23H2 or later         | Standard corporate OS for Windows devices | Auto-updates enabled, BitLocker encryption, Windows Defender active | Default OS for corporate laptops          |
| macOS          | Ventura (13) or later | Development and design work               | FileVault encryption, auto-updates enabled                          | Approved for engineering and design teams |
| Ubuntu LTS     | 22.04 or later        | Development work                          | Disk encryption, auto-updates enabled                               | Approved for engineering teams            |

### 2.2 Server Operating Systems

| Software          | Version(s)     | Use Case                             | Security Requirements                    | Notes                                 |
| ----------------- | -------------- | ------------------------------------ | ---------------------------------------- | ------------------------------------- |
| Windows Server    | 2022           | Corporate services, Active Directory | Regular patching, hardened configuration | Internal infrastructure only          |
| Ubuntu Server LTS | 22.04 or later | Application hosting, development     | Regular patching, minimal installation   | Preferred for containerized workloads |
| Amazon Linux      | 2023           | AWS cloud deployments                | Regular patching, IMDSv2 required        | Preferred for AWS EC2 instances       |

### 2.3 Mobile Operating Systems

| Software | Version(s)    | Use Case       | Security Requirements              | Notes                         |
| -------- | ------------- | -------------- | ---------------------------------- | ----------------------------- |
| iOS      | 17.x or later | Mobile devices | MDM enrollment, passcode required  | Company-provided iPhones      |
| Android  | 14.0 or later | Mobile devices | MDM enrollment, encryption enabled | Approved Samsung devices only |

## 3. Productivity and Communication Tools

### 3.1 Office and Productivity

| Software          | Version(s)          | Use Case                                | Security Requirements             | Notes                                     |
| ----------------- | ------------------- | --------------------------------------- | --------------------------------- | ----------------------------------------- |
| Microsoft 365     | E3/E5 subscriptions | Document creation, email, collaboration | MFA enabled, ATP enabled          | Standard corporate platform               |
| Google Workspace  | Business Plus       | Collaboration with specific clients     | MFA enabled, data loss prevention | Limited approval for client collaboration |
| Adobe Acrobat Pro | DC (subscription)   | PDF creation and editing                | Auto-updates enabled              | As required for specific roles            |
| Notion            | Enterprise plan     | Documentation and knowledge management  | SSO integration required          | Company knowledge base                    |

### 3.2 Communication and Collaboration

| Software        | Version(s)          | Use Case                                | Security Requirements                       | Notes                                    |
| --------------- | ------------------- | --------------------------------------- | ------------------------------------------- | ---------------------------------------- |
| Microsoft Teams | Current             | Internal communication, client meetings | MFA enabled, conditional access             | Primary communication platform           |
| Slack           | Enterprise Grid     | Client collaboration where required     | SSO integration, channel retention policies | Approved for specific client engagements |
| Zoom            | Enterprise          | Video conferencing                      | Encryption enabled, waiting rooms required  | Approved for external meetings           |
| Miro            | Business/Enterprise | Collaborative whiteboarding             | SSO integration                             | Approved for workshops and planning      |

### 3.3 Password Management

| Software  | Version(s) | Use Case                     | Security Requirements                   | Notes                                      |
| --------- | ---------- | ---------------------------- | --------------------------------------- | ------------------------------------------ |
| 1Password | Business   | Secure password management   | MFA required, minimum password strength | Corporate standard                         |
| LastPass  | Enterprise | Legacy client environments   | MFA required                            | Approved for specific legacy clients only  |
| Bitwarden | Enterprise | Alternative password manager | MFA required                            | Approved where client requirements dictate |

## 4. Development Tools and Platforms

### 4.1 Integrated Development Environments (IDEs)

| Software           | Version(s)    | Use Case                      | Security Requirements                            | Notes                           |
| ------------------ | ------------- | ----------------------------- | ------------------------------------------------ | ------------------------------- |
| Visual Studio Code | Latest stable | General development           | Approved extensions only, settings sync disabled | Primary IDE                     |
| JetBrains Suite    | Latest stable | Language-specific development | License management, settings sync disabled       | Approved for engineering team   |
| Visual Studio      | 2022          | .NET development              | Regular updates                                  | Approved for .NET projects      |
| Xcode              | Latest stable | iOS/macOS development         | App Store version only                           | Approved for mobile development |

### 4.2 Version Control and CI/CD

| Software     | Version(s)           | Use Case                  | Security Requirements             | Notes                                  |
| ------------ | -------------------- | ------------------------- | --------------------------------- | -------------------------------------- |
| Git          | Latest stable        | Version control           | Signed commits recommended        | Required for all development           |
| GitHub       | Cloud service        | Code repository, CI/CD    | MFA required, branch protection   | Primary code repository                |
| GitLab       | Cloud or self-hosted | Code repository, CI/CD    | MFA required, branch protection   | Approved for specific clients          |
| Azure DevOps | Cloud service        | CI/CD, project management | MFA required                      | Approved for Microsoft-focused clients |
| Jenkins      | Latest LTS           | CI/CD                     | Isolated network, regular updates | Legacy systems only                    |

### 4.3 Containerization and Orchestration

| Software   | Version(s)    | Use Case                      | Security Requirements          | Notes                               |
| ---------- | ------------- | ----------------------------- | ------------------------------ | ----------------------------------- |
| Docker     | Latest stable | Containerization              | Regular updates, content trust | Development and production          |
| Kubernetes | Latest stable | Container orchestration       | Security context constraints   | Production environments             |
| Helm       | Latest stable | Kubernetes package management | Repo signing                   | Approved for Kubernetes deployments |
| Terraform  | Latest stable | Infrastructure as Code        | State file encryption          | Primary IaC tool                    |

### 4.4 Development Languages and Frameworks

| Software | Version(s)        | Use Case                     | Security Requirements                     | Notes                                  |
| -------- | ----------------- | ---------------------------- | ----------------------------------------- | -------------------------------------- |
| Node.js  | LTS versions only | JavaScript runtime           | Regular updates                           | Approved for web development           |
| Python   | 3.10 or later     | Backend, data processing, AI | Virtual environments, dependency scanning | Primary language for data projects     |
| Go       | 1.21 or later     | Backend services             | Dependency scanning                       | Preferred for microservices            |
| Java     | 17 LTS or later   | Enterprise applications      | Regular updates                           | Approved for enterprise clients        |
| .NET     | 6.0 LTS or later  | Microsoft stack development  | Regular updates                           | Approved for Microsoft-focused clients |
| React    | Latest stable     | Frontend development         | Dependency scanning                       | Primary frontend framework             |
| Flutter  | Latest stable     | Cross-platform mobile        | Dependency scanning                       | Preferred for mobile applications      |

## 5. Security Tools

### 5.1 Endpoint Security

| Software                        | Version(s) | Use Case            | Security Requirements  | Notes                       |
| ------------------------------- | ---------- | ------------------- | ---------------------- | --------------------------- |
| Microsoft Defender for Endpoint | Current    | Endpoint protection | Centralized management | Primary endpoint protection |
| Crowdstrike Falcon              | Current    | Endpoint protection | Centralized management | Approved alternative        |
| Jamf                            | Current    | macOS management    | Centralized management | For macOS devices           |

### 5.2 Network Security

| Software         | Version(s)    | Use Case              | Security Requirements | Notes                           |
| ---------------- | ------------- | --------------------- | --------------------- | ------------------------------- |
| Cisco AnyConnect | Latest stable | VPN client            | MFA integration       | Corporate VPN solution          |
| WireGuard        | Latest stable | VPN alternative       | Proper key management | Approved for specific use cases |
| Tailscale        | Current       | Zero trust networking | MFA integration       | Approved for development teams  |

### 5.3 Security Testing and Monitoring

| Software   | Version(s)    | Use Case                         | Security Requirements  | Notes                                 |
| ---------- | ------------- | -------------------------------- | ---------------------- | ------------------------------------- |
| Snyk       | Enterprise    | Dependency scanning              | Integration with CI/CD | Required for all projects             |
| SonarQube  | Latest LTS    | Code quality and security        | Integration with CI/CD | Required for all projects             |
| OWASP ZAP  | Latest stable | Web application security testing | Controlled usage       | Security team and approved developers |
| Burp Suite | Professional  | Web application security testing | Licensed usage only    | Security team only                    |

## 6. Cloud Platforms and Services

### 6.1 Cloud Providers

| Software              | Version(s) | Use Case                    | Security Requirements           | Notes                           |
| --------------------- | ---------- | --------------------------- | ------------------------------- | ------------------------------- |
| Amazon Web Services   | N/A        | Primary cloud provider      | Security hub enabled, GuardDuty | Strategic platform              |
| Microsoft Azure       | N/A        | Microsoft-centric workloads | Security center enabled         | Approved for Microsoft clients  |
| Google Cloud Platform | N/A        | Data and AI workloads       | Security command center enabled | Approved for specific use cases |

### 6.2 Cloud Security and Management

| Software        | Version(s) | Use Case                | Security Requirements | Notes                                  |
| --------------- | ---------- | ----------------------- | --------------------- | -------------------------------------- |
| AWS CloudTrail  | Current    | AWS activity monitoring | Centralized logging   | Required for all AWS accounts          |
| Azure Monitor   | Current    | Azure monitoring        | Centralized logging   | Required for all Azure subscriptions   |
| Terraform Cloud | Enterprise | IaC management          | SSO integration       | Approved for infrastructure management |

### 6.3 Database Platforms

| Software   | Version(s)    | Use Case                | Security Requirements                 | Notes                           |
| ---------- | ------------- | ----------------------- | ------------------------------------- | ------------------------------- |
| PostgreSQL | 15.x or later | Relational database     | Encryption at rest, network isolation | Preferred relational database   |
| MySQL      | 8.0 or later  | Relational database     | Encryption at rest, network isolation | Approved for specific use cases |
| MongoDB    | 6.0 or later  | Document database       | Encryption at rest, network isolation | Approved for specific use cases |
| Redis      | 7.0 or later  | Caching, message broker | Authentication, network isolation     | Approved for caching needs      |
| Snowflake  | N/A           | Data warehousing        | Encryption, MFA for admin             | Approved for analytics projects |

## 7. Data Analysis and AI Tools

### 7.1 Data Processing and Analysis

| Software     | Version(s)    | Use Case                    | Security Requirements         | Notes                                     |
| ------------ | ------------- | --------------------------- | ----------------------------- | ----------------------------------------- |
| Jupyter      | Latest stable | Data analysis, prototyping  | Secure configuration          | Approved for data teams                   |
| Apache Spark | Latest stable | Large-scale data processing | Secure configuration          | Approved for data engineering             |
| Power BI     | Latest        | Business intelligence       | Data classification awareness | Approved for analytics                    |
| Tableau      | Latest        | Data visualization          | Data classification awareness | Approved for client-specific requirements |

### 7.2 AI and Machine Learning

| Software             | Version(s)    | Use Case             | Security Requirements               | Notes                                |
| -------------------- | ------------- | -------------------- | ----------------------------------- | ------------------------------------ |
| TensorFlow           | Latest stable | Machine learning     | Data protection controls            | Approved for ML projects             |
| PyTorch              | Latest stable | Machine learning     | Data protection controls            | Approved for ML projects             |
| Hugging Face         | Latest stable | NLP models and tools | Controlled data exposure            | Approved for ML projects             |
| Azure OpenAI Service | Current       | AI integration       | Content filtering, usage monitoring | Approved for enterprise AI use cases |

## 8. Client-Specific Software

### 8.1 Client Environment Requirements

Client-specific software requirements must be documented in project documentation. All client-required software must still undergo security review before approval, with exceptions noted and risk-assessed.

### 8.2 Common Client-Required Software

| Software        | Version(s)      | Use Case                          | Security Requirements | Notes                    |
| --------------- | --------------- | --------------------------------- | --------------------- | ------------------------ |
| Atlassian Suite | Cloud or latest | Project management, documentation | MFA required          | Used by multiple clients |
| Salesforce      | Various         | CRM integration                   | MFA required          | Client integrations      |
| SAP             | Various         | ERP integration                   | Secure connectivity   | Client integrations      |
| ServiceNow      | Various         | ITSM integration                  | Secure connectivity   | Client integrations      |

## 9. Personal Device Software Requirements

For staff using personal devices under the BYOD policy, the following minimum software requirements apply:

| Category                 | Required Software                 | Notes                                     |
| ------------------------ | --------------------------------- | ----------------------------------------- |
| Endpoint Protection      | Approved antivirus/EDR solution   | Must meet minimum corporate standards     |
| Disk Encryption          | OS-native or approved third-party | Full disk encryption required             |
| VPN Client               | Corporate standard VPN client     | Required for corporate network access     |
| Mobile Device Management | Corporate MDM solution            | Required for email/data access            |
| Password Manager         | Corporate standard solution       | Required for secure credential management |

## 10. Software Retirement

The following software is being phased out and should not be used for new projects:

| Software          | Replacement                | Retirement Date | Notes               |
| ----------------- | -------------------------- | --------------- | ------------------- |
| Internet Explorer | Microsoft Edge             | Retired         | No longer supported |
| Angular.js        | React or Angular           | June 2025       | End of support      |
| CentOS 7          | Ubuntu LTS or Amazon Linux | June 2025       | End of support      |
| jQuery            | Native JavaScript          | December 2025   | Strategic decision  |
| Apache Ant        | Maven or Gradle            | December 2025   | Strategic decision  |

## 11. Exception Process

Exceptions to this Approved Software List may be requested through the Software Request and Approval Procedure (DOC-37). Exceptions require:

- Clear business justification
- Security risk assessment
- Approval from the IT Operations Manager or CTO
- Time limitation with review date
- Documentation of any compensating controls

## 12. Compliance Monitoring

Compliance with this Approved Software List will be monitored through:

- Regular automated software inventory scans
- Periodic manual audits
- Cloud service usage reviews
- Developer environment assessments
- Vulnerability scanning that identifies unapproved software

## 13. Related Documents

- POL-01: Information Security Policy
- POL-02: Acceptable Use Policy
- POL-12: Change Management Policy
- POL-13: Cryptographic Controls Policy
- DOC-37: Software Request and Approval Procedure
- DOC-38: Software License Management Procedure
- FORM-05: Software Approval Request Form

---

_By working for Enablis, you acknowledge that you have read, understood, and agree to comply with this Approved Software List._
