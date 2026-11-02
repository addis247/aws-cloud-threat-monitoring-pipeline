# GuardDuty Finding Analysis: SSH Brute Force Detection

## Finding Summary
* **Finding type:** `UnauthorizedAccess:EC2/SSHBruteForce`
* **Finding source:** `AWS-generated sample finding`
* **Severity:** `7.4 (High)`
* **AWS Region:** `us-east-1`
* **Affected resource type:** `EC2 Instance (i-0a1b2c3d4e5f6g7h8)`
* **Status:** `Investigated`

## Analyst Summary
Amazon GuardDuty generated a high-severity finding indicating that an external IP address was performing brute-force SSH authentication attempts against an EC2 instance in the lab VPC. 

The finding was automatically captured by the EventBridge severity rule ($\ge 7.0$) and routed through the SNS notification pipeline for immediate analyst review.

## Validation
The analyst reviewed:
* **Finding type:** High-severity SSH brute-force activity pattern.
* **Finding severity:** Score of 7.4, crossing the automated notification threshold.
* **Affected resource:** Isolated lab EC2 instance.
* **Finding description:** Multiple failed login attempts originating from a suspicious external source IP.
* **First-seen and last-seen timestamp:** Logged within a 10-minute observation window.
* **Recommended actions:** Verified via AWS documentation as an AWS-generated sample security event.

## Supporting Evidence
The analyst reviewed the following available evidence:
* GuardDuty finding details and raw JSON payload.
* Associated CloudTrail management events for the affected instance.
* VPC security group inbound rules restricting port 22 access.

## Assessment
* **Potential impact:** `High (Unauthorized administrative access attempt if credentials are weak)`
* **Investigation result:** `Confirmed automated test finding / zero compromise verified`
* **False-positive or test determination:** `Controlled lab test (AWS sample finding triggered to validate EventBridge-to-SNS pipeline)`

## Recommended Actions
* Validate whether the activity was authorized or a simulated test.
* Review related CloudTrail events to confirm no state changes occurred.
* Verify security group restrictions on remote management ports.
* Document findings and escalate unresolved suspicious behavior.

## Final Disposition
* **Disposition:** `Resolved - Verified Automated Alert Pipeline Functional`

## Portfolio Notice
This analysis has been sanitized. All account IDs, email addresses, ARNs, resource names, IP addresses, and other identifying information have been removed or replaced.
