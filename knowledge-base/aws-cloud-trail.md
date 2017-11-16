# AWS CloudTrail

<p align="center">
  <img src="https://github.com/WhiteRookPL/aws-identity-access-management/raw/master/knowledge-base/assets/cloud-trail.png" />
</p>

## Description

**AWS CloudTrail** is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. With CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. CloudTrail provides event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command line tools, and other AWS services. This event history simplifies security analysis, resource change tracking, and troubleshooting.

## Notes

- Service that is tracking events (and effectively - also changes) across your AWS account and saves those events to log files.
- Logs are stored on S3 and you are able to access them, download, encrypt with AWS KMS.
- You can troubleshoot operational and security incidents over the past 90 days in the CloudTrail console by viewing Event history.


## References

https://aws.amazon.com/cloudtrail/pricing/