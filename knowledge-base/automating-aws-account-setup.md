# Automating AWS account setup and provisioning

## AWS CloudFormation

<p align="center">
  <img src="https://github.com/WhiteRookPL/aws-identity-access-management/raw/master/knowledge-base/assets/cloud-formation.png" />
</p>

### Description

**AWS CloudFormation** provides a common language for you to describe and provision all the infrastructure resources in your cloud environment. CloudFormation allows you to use a simple text file to model and provision, in an automated and secure manner, all the resources needed for your applications across all regions and accounts. This file serves as the single source of truth for your cloud environment.

### References

- https://aws.amazon.com/cloudformation

## AWS CLI

<p align="center">
  <img src="https://github.com/WhiteRookPL/aws-identity-access-management/raw/master/knowledge-base/assets/cli.png" />
</p>

### Useful Commands

```
~ $ aws iam get-account-password-policy
~ $ aws iam generate-credential-report
~ $ aws iam get-credential-report | jq '.Content' -r | base64 -D
~ $ aws iam list-access-keys --user-name <USERNAME> --query 'AccessKeyMetadata[?Status==`Active`]'
~ $ aws iam list-access-keys --user-name <USERNAME> --query 'AccessKeyMetadata[].AccessKeyId' | jq -r '.[]'
~ $ aws cloudtrail describe-trails
~ $ aws cloudtrail get-trail-status --name my-trail
```

### References

- https://aws.amazon.com/cli/