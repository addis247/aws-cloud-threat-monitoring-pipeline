# Incident Investigation Workflow

## Purpose

This workflow documents the analyst steps following receipt of a high-severity GuardDuty notification.

## Workflow

### 1. Receive Alert

The analyst receives an email notification through the confirmed Amazon SNS subscription.

### 2. Validate the Finding

The analyst verifies:

- Finding type
- Severity
- AWS Region
- Affected resource
- First-seen and last-seen information
- Finding description
- Available recommended actions

### 3. Determine Whether the Finding Is a Test

The analyst determines whether the finding is:

- An AWS-generated sample finding
- A controlled lab test
- Unexpected activity requiring further investigation

### 4. Gather Supporting Evidence

The analyst reviews applicable evidence, including:

- GuardDuty finding details
- CloudTrail event history
- IAM identity information
- Source IP information
- Resource configuration
- Relevant security-group activity

### 5. Assess Scope and Impact

The analyst determines:

- Which resources are affected
- Whether credentials may be involved
- Whether unauthorized changes occurred
- Whether suspicious activity is continuing
- The potential operational and security impact

### 6. Recommend Response

Depending on the evidence, the analyst may recommend:

- Closing the finding as a controlled test
- Monitoring for additional activity
- Updating a security group
- Revoking or rotating credentials
- Restricting resource access
- Escalating to account administration
- Preserving evidence for further investigation

### 7. Document and Close

The analyst records:

- Finding summary
- Evidence reviewed
- Investigation conclusion
- Response recommendation
- Final disposition
- Follow-up actions

## Human Oversight

This lab automates finding prioritization and notification. It does not automatically perform containment or remediation. A human analyst validates the evidence and authorizes the response.
