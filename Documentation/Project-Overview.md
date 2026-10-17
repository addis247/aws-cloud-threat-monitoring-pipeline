# Project Overview

## Business Scenario

A small organization requires centralized visibility into AWS administrative activity and a method for notifying its security analyst when Amazon GuardDuty identifies a high-severity security finding.

The organization wants to reduce unnecessary alert noise while retaining human oversight for investigation and response decisions.

## Project Objective

The objective was to create an AWS security-monitoring workflow that:

1. Secures administrative access.
2. Establishes a segmented network environment.
3. Records configured AWS management events.
4. Enables continuous threat detection.
5. Prioritizes high-severity security findings.
6. Delivers prioritized findings to an analyst.
7. Supports repeatable investigation and escalation.
8. Monitors unexpected cloud-service charges.

## Technical Scope

The project included:

- AWS root-account MFA
- Dedicated administrative identity
- Custom VPC
- Public and private subnets
- AWS CloudTrail
- Amazon S3
- Amazon GuardDuty
- Amazon EventBridge
- Amazon SNS
- AWS Budgets

## Out of Scope

The project did not include:

- Production workloads
- Customer or regulated data
- Multi-account AWS Organizations
- Automated resource isolation
- Automated credential suspension
- Automated malware remediation
- Production-grade business continuity
- Enterprise ticketing-system integration

## Project Outcome

The lab demonstrated a security-monitoring workflow in which selected high-severity GuardDuty findings were routed through EventBridge to an SNS email subscription for analyst review.

Human authorization remained required for any containment or remediation activity.
