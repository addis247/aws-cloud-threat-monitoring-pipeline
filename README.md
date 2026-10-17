# AWS Cloud Threat Monitoring and Alerting Pipeline

## Project Overview

This project demonstrates the design and implementation of an automated AWS security monitoring and alerting pipeline.

The environment uses AWS identity, logging, threat-detection, event-routing, and notification services to identify high-severity security findings and notify a security analyst for investigation.

The project was created as a hands-on cloud security portfolio lab and does not contain production, proprietary, or customer data.

---

## Project Objectives

- Strengthen administrative access and identity security
- Establish centralized AWS API activity logging
- Detect suspicious cloud activity using Amazon GuardDuty
- Filter high-severity findings using Amazon EventBridge
- Route prioritized security alerts through Amazon SNS
- Document a repeatable investigation and escalation workflow
- Demonstrate cost-conscious cloud security implementation

---

## Architecture

```text
AWS Account Activity
        |
        +--------------------+
        |                    |
        v                    v
AWS CloudTrail        Amazon GuardDuty
        |                    |
        v                    v
Amazon S3             Security Finding
                             |
                             v
                    Amazon EventBridge
                    Severity Filter >= 7
                             |
                             v
                       Amazon SNS
                             |
                             v
                  Security Analyst Email
```

**Important clarification:** CloudTrail sends audit logs to S3, while GuardDuty findings are published separately to EventBridge. The EventBridge rule does not scan the S3 bucket.

---

## AWS Services Used

- AWS Identity and Access Management
- Amazon Virtual Private Cloud
- AWS CloudTrail
- Amazon Simple Storage Service
- Amazon GuardDuty
- Amazon EventBridge
- Amazon Simple Notification Service
- AWS Budgets

---

## Project Phases

### 1. Identity and Perimeter Security

- Secured administrative access
- Created a dedicated IAM identity for lab administration
- Applied role-appropriate IAM permissions
- Configured VPC and security-group controls
- Established account budget monitoring

### 2. Threat Detection

- Enabled Amazon GuardDuty
- Reviewed generated or sample security findings
- Evaluated finding type, severity, affected resource, and recommended response
- Documented the analyst investigation process

### 3. Audit Logging

- Enabled AWS CloudTrail management-event logging
- Configured centralized log delivery to Amazon S3
- Applied encryption and restricted access to stored audit logs
- Used CloudTrail records to review account and administrative activity

### 4. Automated Alert Routing

- Created an Amazon EventBridge rule for GuardDuty findings
- Applied an event pattern for severity values of 7 or higher
- Routed matching events to an Amazon SNS topic
- Configured an email subscription for analyst notification
- Tested and documented the alert-delivery process

---

## Security Controls Demonstrated

- Administrative account protection
- Identity and access management
- Least-privilege access principles
- Centralized audit logging
- Encrypted log storage
- Continuous threat detection
- Severity-based event filtering
- Automated security notification
- Incident documentation and escalation
- Cloud budget monitoring

---

## Deliverables

- Architecture diagram
- Sanitized EventBridge event pattern
- Sanitized IAM policy
- Cloud security control summary
- Sample GuardDuty finding analysis
- Incident-response workflow
- Implementation screenshots

---

## Skills Demonstrated

- AWS Cloud Security
- Cloud Threat Detection
- Security Monitoring
- Identity and Access Management
- Audit Logging
- Event-Driven Security Automation
- Incident Investigation
- Alert Prioritization
- Security Documentation
- Cost Governance

---

## Security and Privacy Notice

All account IDs, resource identifiers, email addresses, bucket names, user names, access keys, and other sensitive values have been removed or replaced with placeholders.

No production systems, real customer information, confidential data, or active credentials are included in this repository.

---

## Portfolio Disclaimer

This repository documents a personal educational lab created for cybersecurity training and professional portfolio development. The environment and results should not be interpreted as a production security implementation or evidence of a real-world cyberattack.

