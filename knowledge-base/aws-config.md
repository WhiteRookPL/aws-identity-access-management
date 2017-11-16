## AWS Config

<p align="center">
  <img src="https://github.com/WhiteRookPL/aws-identity-access-management/raw/master/knowledge-base/assets/config.png" />
</p>

## Description

*AWS Config* is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources. Config continuously monitors and records your AWS resource configurations and allows you to automate the evaluation of recorded configurations against desired configurations. With Config, you can review changes in configurations and relationships between AWS resources, dive into detailed resource configuration histories, and determine your overall compliance against the configurations specified in your internal guidelines. This enables you to simplify compliance auditing, security analysis, change management, and operational troubleshooting.

It allows for enforcing various stuff e.g. policies and life-cycles for S3 buckets across your *AWS* account etc.

## Features

### Change Management

When your resources are created, updated, or deleted, *AWS Config* streams these configuration changes to Amazon Simple Notification Service (SNS), so that you are notified of all the configuration changes. *AWS Config* represents relationships between resources so that you can assess how a change to one resource may impact other resources.

### Continuous Audit and Compliance

*AWS Config* is designed to help you assess compliance with your internal policies and regulatory standards by providing you visibility into the configuration of your AWS resources, and evaluating resource configuration changes against your desired configurations.

### Security Analysis

Data from *AWS Config* enables you to continuously monitor the configurations of your resources and evaluate these configurations for potential security weaknesses. Changes to your resource configurations can trigger Amazon Simple Notification Service (SNS) notifications, which can be sent to your security team to review and take action. After a potential security event, Config enables you to review the configuration history of your resources and examine your security posture.

## References

- https://docs.aws.amazon.com/config/latest/developerguide/resource-config-reference.html#s3-attributes