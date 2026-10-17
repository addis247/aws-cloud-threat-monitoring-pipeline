# Security Controls Implemented

## Identity and Access Management

- Enabled multi-factor authentication for the AWS root account.
- Avoided using the root account for routine administrative work.
- Created the `admin-dev` identity for lab administration.
- Used identity-based permissions for AWS service configuration.
- Separated routine configuration activity from root-account activity.

## Network Security

- Created a custom VPC using the `10.0.0.0/16` CIDR range.
- Configured public and private subnets.
- Applied network controls to regulate allowed traffic.
- Maintained the environment as an isolated educational lab.

## Audit Logging

- Created the `cyber-lab-main-trail` CloudTrail trail.
- Configured the trail for multi-region management events.
- Delivered CloudTrail records to an Amazon S3 bucket.
- Centralized management-event records for investigation and compliance support.

## Threat Detection

- Enabled Amazon GuardDuty.
- Enabled selected GuardDuty protection features.
- Reviewed finding severity and affected resources.
- Used GuardDuty findings as security-investigation inputs.

## Event Filtering

- Created the `cyber-lab-guardduty-high-severity` EventBridge rule.
- Configured the rule on the default event bus.
- Filtered GuardDuty findings with severity values of 7 or higher.
- Reduced notification noise by prioritizing higher-severity findings.

## Analyst Notification

- Created the `cyber-lab-alert-topic` SNS topic.
- Configured an email subscription.
- Confirmed the SNS subscription.
- Routed matching EventBridge events to the SNS topic.

## Cost Governance

- Created a Zero-Spend Budget Alert.
- Set the notification threshold to $0.01.
- Used the alert to identify unexpected lab charges.
- Monitored GuardDuty trial status and usage-based services.

## Limitations

- The SNS notification does not automatically remediate a finding.
- The budget alert does not stop services or guarantee zero cost.
- Centralized S3 logging is not described as immutable unless additional integrity or retention protections are verified.
- A dedicated administrator identity is not described as least privilege unless the assigned permissions were restricted to the minimum actions required.
