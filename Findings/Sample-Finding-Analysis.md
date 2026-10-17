# GuardDuty Finding Analysis

## Finding Summary

**Finding type:** [INSERT SANITIZED FINDING TYPE]

**Finding source:** [AWS-generated sample / controlled lab test / unexpected activity]

**Severity:** [INSERT SEVERITY]

**AWS Region:** [INSERT REGION]

**Affected resource type:** [INSERT RESOURCE TYPE]

**Status:** Investigated

## Analyst Summary

Amazon GuardDuty generated a finding indicating potentially suspicious activity affecting an AWS resource in the lab environment.

The finding was selected by the EventBridge severity rule and routed through the SNS notification pipeline for analyst review.

## Validation

The analyst reviewed:

- Finding type
- Finding severity
- Affected resource
- AWS Region
- Finding description
- First-seen and last-seen information
- Recommended response guidance

## Supporting Evidence

The analyst reviewed the following available evidence:

- GuardDuty finding details
- Relevant CloudTrail activity
- IAM identity information
- Source information
- Resource configuration
- Associated security controls

## Assessment

**Potential impact:** [INSERT LOW, MEDIUM, OR HIGH]

**Investigation result:** [INSERT RESULT]

**False-positive or test determination:** [INSERT DETERMINATION]

## Recommended Actions

- Validate whether the activity was authorized.
- Review related CloudTrail events.
- Review the affected identity or resource configuration.
- Restrict access if unauthorized activity is confirmed.
- Rotate or revoke credentials if compromise is suspected.
- Document findings and escalate unresolved activity.

## Final Disposition

[INSERT FINAL DISPOSITION]

## Portfolio Notice

This analysis has been sanitized. All account IDs, email addresses, ARNs, resource names, IP addresses, and other identifying information have been removed or replaced.
