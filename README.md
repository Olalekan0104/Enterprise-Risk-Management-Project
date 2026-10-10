# NovaPay Financial Services: Enterprise Risk Management (ERM) Case Study

This project applies **Enterprise Risk Management (ERM)** principles to assess cybersecurity and operational risks at NovaPay Financial Services, a Lagos-based regulated FinTech company. It focuses on identifying and classifying assets, evaluating threats and vulnerabilities, recommending risk treatments and security controls, and calculating financial exposure using Single Loss Expectancy (SLE), Annual Rate of Occurrence (ARO), and Annual Loss Expectancy (ALE).

## Table of Contents

- [Project Overview](#project-overview)
- [Network Topology](#network-topology)
- [Tools and Technologies](#tools-and-technologies)
- [Configuration Steps](#configuration-steps)
- [Results and Findings](#results-and-findings)
- [Author](#author)

## Project Overview

The purpose of this project is to conduct a structured enterprise risk assessment for NovaPay Financial Services, a regulated FinTech organization that processes financial transactions and manages sensitive customer information.

NovaPay has approximately **120 employees, over 500,000 customer wallets, and more than 8,000 registered small-business merchants**. The organization faces potential security and compliance risks associated with weak administrative access controls, inadequate customer login protection, and insufficient third-party vendor assessments.

As a Junior Risk Analyst, the objective was to assess three connected risk scenarios and recommend practical measures to reduce exposure.

**Project objectives:**

- Identify critical business and technology assets.
- Classify information according to sensitivity: Public, Internal, Confidential, and Restricted.
- Identify threats and vulnerabilities affecting customer data, application authentication, and third-party services.
- Assess risk levels and recommend appropriate risk treatment strategies.
- Recommend preventive, detective, and corrective controls.
- Calculate financial exposure using SLE, ARO, and ALE.
- Present risk findings in clear, business-focused language to support management decision-making.

**Business risk appetite:** NovaPay has very low tolerance for risks affecting customer funds, customer data, or its licence to operate. Only Low risks may be accepted without treatment.

## Network Topology

This case study focuses on a logical view of NovaPay's technology environment and its third-party payment relationship rather than a physical network diagram. The assessment covers three interconnected risk areas: the customer database, mobile application login, and PaySecure Ltd, the external payment vendor.

### Logical Environment

```text
                  NovaPay Financial Services
                            |
              +-------------+-------------+
              |             |             |
       Customer Database  Mobile App   PaySecure Ltd
              |             |             |
       Administrative    Customer       Third-Party
           Access         Login        Payment Vendor
              |             |             |
        Shared Passwords  No MFA       No Formal Security
        No Admin MFA      No Rate      Assessment
        Limited Alerting  Limiting     Unclear Data Boundaries
              |             |             |
              +-------------+-------------+
                            |
                    Enterprise Risk
                       Assessment
                            |
             +--------------+--------------+
             |              |              |
        Asset and Data   Threat and     Risk Treatment
        Classification  Vulnerability   and Controls
                         Assessment
                            |
                   Financial Exposure
                     SLE, ARO, ALE
```

### Assets and Risk Areas

| Asset or Component | Identified Weakness | Business Owner | Data Classification |
|---|---|---|---|
| Customer Database | No MFA for administrative accounts, shared passwords, and no alerting for unusual administrative access | Head of IT | Confidential |
| Mobile App Login | No customer MFA, no login rate-limiting, and rising unauthorized-transfer complaints | Head of Product | Public |
| PaySecure Ltd | No formal vendor security assessment and unclear data-sharing boundaries | Head of Compliance | Internal |

**Important note:** The classifications above reflect the original case study. The Mobile App is classified as Public because it is customer-facing, while the Customer Database is classified as Confidential because it contains sensitive customer information. PaySecure's relationship and related information are classified as Internal in the original assessment.

The case study does not provide actual IP addresses, subnet configurations, firewalls, routers, network segmentation details, or specific hardware models. These details are therefore not included in the topology.

## Tools and Technologies

The project uses enterprise risk management concepts, information security controls, and financial risk calculations.

- **Enterprise Risk Management (ERM):** A structured approach to identifying, assessing, treating, and monitoring organizational risks.
- **Asset and Data Classification:** Categorization of information according to sensitivity and required protection.
- **Threat and Vulnerability Assessment:** Identification of potential threats and weaknesses that could expose business assets.
- **Risk Scoring and Analysis:** Assessment of risk severity to support treatment prioritization.
- **Risk Treatment Strategies:** Avoid, Mitigate, Transfer, and Accept.
- **Preventive Controls:** Security measures intended to prevent incidents before they occur.
- **Detective Controls:** Measures designed to identify suspicious activities or control failures.
- **Corrective Controls:** Measures used to address identified weaknesses and restore secure operations.
- **Single Loss Expectancy (SLE):** Calculation of the estimated financial loss from a single incident.
- **Annual Rate of Occurrence (ARO):** Estimate of how frequently a risk event may occur annually.
- **Annual Loss Expectancy (ALE):** Calculation of expected annual financial loss.
- **Microsoft PowerPoint:** Used to prepare the case study presentation.
- **PDF:** Used as the final presentation and submission format.

No specific network configuration tools, monitoring platforms, vulnerability scanners, or security appliances are identified in the source document.

## Configuration Steps

### 1. Review the Business Environment

Reviewed NovaPay's business profile, regulatory context, operational responsibilities, and risk appetite.

Identified the potential consequences of security incidents affecting customer funds, personal information, payment services, and regulatory obligations.

### 2. Identify and Classify Assets

Identified the three primary assets and risk areas:

- **Customer Database:** Classified as Confidential because it contains sensitive customer and banking information.
- **Mobile App:** Classified as Public because it is designed for customer access and use.
- **PaySecure Ltd:** Classified as Internal in the original assessment because of the organization's vendor relationship and data-sharing activities.

The classification exercise established the basis for determining the level of protection required for each asset.

### 3. Identify Threats and Vulnerabilities

Evaluated the threats and weaknesses associated with each scenario.

| Scenario | Identified Threats | Identified Vulnerabilities |
|---|---|---|
| Customer Database | Unauthorized access, repudiation, data loss, and breach of confidentiality | Shared passwords, missing MFA, insufficient access controls, and limited security monitoring |
| Mobile App Login | Unauthorized access, financial loss, and reduced customer trust | Missing customer MFA, lack of login rate-limiting, and insufficient authentication safeguards |
| PaySecure Ltd | Data loss and breach of confidentiality | No formal vendor security assessment, unclear data-sharing boundaries, and insufficient documented compliance and audit processes |

The assessment highlighted the need to strengthen access management, application authentication, monitoring, and third-party risk management.

### 4. Assess Risks and Recommend Treatment

Evaluated the risk scenarios and identified proposed treatment strategies.

| Scenario | Risk Level in Source | Recommended Treatment | Rationale |
|---|---|---|---|
| Customer Database | High, 80% | Mitigate | Strengthen access controls and ensure that only authorized employees with a legitimate business need can access sensitive information. |
| Mobile App Login | High, 100% | Avoid | The original assessment recommends stopping the unsafe exposure immediately by implementing appropriate security safeguards to protect customer funds and maintain customer trust. |
| PaySecure Ltd | High, 100% | Transfer or Avoid | The original assessment recommends pausing data sharing or activities until a formal security assessment is completed and appropriate compliance evidence is provided. |

The percentages are reproduced from the source document and are not independently validated risk scores.

The treatment strategies are defined as follows:

- **Avoid:** Stop the activity causing the risk.
- **Mitigate:** Reduce the likelihood or impact of the risk.
- **Transfer:** Shift some or all of the risk to another party.
- **Accept:** Knowingly accept the risk.

Given NovaPay's low risk appetite, significant risks affecting customer funds, customer information, or its licence to operate should receive priority attention and documented treatment decisions.

### 5. Recommend Security Controls

Identified control categories for each risk scenario.

| Risk Scenario | Control Category 1 | Control Category 2 |
|---|---|---|
| Customer Database | Detective Control | Corrective Control |
| Mobile App Login | Preventive Control | Detective Control |
| PaySecure Ltd | Detective Control | Corrective Control |

The original case study identifies the control categories but does not specify detailed control implementations. Practical recommendations based on the identified weaknesses include:

**Customer Database**

- Implement MFA for all administrative accounts and eliminate shared administrator passwords.
- Apply role-based access control and least privilege, with logging and alerts for unusual administrative activity.
- Establish a corrective process for investigating access violations, revoking inappropriate access, and addressing identified control failures.

**Mobile App Login**

- Implement customer MFA and rate-limiting to reduce unauthorized login attempts.
- Monitor authentication failures and suspicious transfer patterns, with procedures for investigation and response.

**PaySecure Ltd**

- Conduct a formal third-party security assessment and document security responsibilities and data-sharing boundaries.
- Establish remediation requirements and review evidence of corrective actions before resuming or expanding higher-risk data-sharing activities.

These implementation examples are recommendations derived from the case findings, rather than configurations explicitly documented in the original assessment.

### 6. Calculate Financial Exposure Using SLE, ARO, and ALE

Calculated the potential financial exposure associated with a successful Customer Database breach.

**Given values:**

- Asset Value: ₦50,000,000
- Exposure Factor (EF): 60%
- Annual Rate of Occurrence (ARO): 0.5, representing an estimated occurrence once every two years

**Single Loss Expectancy (SLE)**

Formula:

`SLE = Asset Value × Exposure Factor`

Calculation:

`SLE = ₦50,000,000 × 0.60`

**SLE = ₦30,000,000**

The estimated financial loss from one successful breach is ₦30,000,000.

**Annual Loss Expectancy (ALE)**

Formula:

`ALE = SLE × ARO`

Calculation:

`ALE = ₦30,000,000 × 0.5`

**ALE = ₦15,000,000 per year**

The estimated annual financial exposure is ₦15,000,000, based on the assumptions provided in the case study.

### 7. Consolidate Findings for Management

Organized the assessment into a business-focused presentation covering:

- Asset and data classification.
- Threat and vulnerability identification.
- Risk levels and treatment recommendations.
- Recommended control categories and practical security measures.
- Financial exposure calculations.
- Risk priorities requiring management attention.

The original assignment required the completed PowerPoint presentation to be converted to PDF for submission.

## Results and Findings

The assessment identified three significant areas of exposure that could affect NovaPay's confidentiality, financial security, customer trust, and regulatory obligations.

### Key Findings

- **Customer Database Risk:** Missing administrative MFA, shared passwords, and limited monitoring increase the possibility of unauthorized access to sensitive customer information.
- **Mobile App Authentication Risk:** The absence of customer MFA and login rate-limiting creates opportunities for unauthorized access, while rising unauthorized-transfer complaints indicate a need for investigation.
- **Third-Party Vendor Risk:** The absence of a formal PaySecure security assessment and clearly documented data-sharing boundaries limits NovaPay's visibility into the vendor's security posture.
- **Control Improvement Opportunities:** Stronger identity and access management, authentication safeguards, security monitoring, and vendor due diligence are important risk reduction priorities.
- **Financial Exposure:** The calculated SLE is **₦30,000,000**, while the calculated ALE is **₦15,000,000 per year**, using the assumptions supplied in the case study.

### Recommended Priorities

1. **Strengthen administrative access security** by eliminating shared passwords, enforcing MFA, applying least privilege, and monitoring privileged activity.
2. **Improve customer authentication security** by introducing MFA, implementing login rate-limiting, and investigating suspicious transfer activity.
3. **Address third-party security gaps** by completing PaySecure's security assessment, documenting data-sharing responsibilities, and tracking remediation actions.
4. **Monitor risk indicators** such as unusual administrative logins, repeated authentication failures, unauthorized-transfer complaints, and overdue vendor assessment findings.
5. **Review financial exposure regularly** and update risk assessments when incident frequency, asset values, or control effectiveness changes.

The case study demonstrates how ERM connects technical security weaknesses to business impact, risk treatment, and financial exposure. It also shows the importance of presenting findings in clear language that supports informed management decisions.

The source document does not provide actual post-implementation test results, confirmed incident outcomes, or evidence that the recommended controls have been deployed. The findings should therefore be understood as a risk assessment and set of recommendations, not proof that the identified risks have already been resolved.

## Author

**Author:** Saheed Ilesanmi

**Role:** Junior Risk Analyst | Enterprise Risk Management (ERM) | Governance, Risk, and Compliance (GRC)

**LinkedIn:** linkedin.com/in/saheed-i-0008b11bb

**Project Context:** Enterprise Risk Management case study based on NovaPay Financial Services, completed as part of GRC and ERM learning.

