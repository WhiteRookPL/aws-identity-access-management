# Differences between Cloud Providers

## AWS (*our reference*)

- AWS *Identity Access Management*.
  - Supports *users*, *groups*, *roles*, *policies* and *instance profiles*.
  - No auditing by default (available by separate service - *AWS CloudTrail*).
  - Does not replace *AD* or *LDAP*.

## Azure

- Azure *Active Directory*.
  - Full power (and problems) of *Active Directory*.
    - Supports the same things as AWS IAM when it comes to granularity.
  - Easier federation with *LDAP* or *AD*.
  - Built-in audit trail (instead of separate service - *AWS CloudTrail*).

## Google Cloud

- Google Cloud *Identity* and *Access Management* (*Cloud IAM*).
  - Supports the same things as AWS IAM when it comes to granularity.
  - Built-in audit trail (instead of separate service - *AWS CloudTrail*).
  - Does not replace *AD* or *LDAP*.

## References

- https://docs.microsoft.com/en-us/azure/active-directory/active-directory-whatis
- https://cloud.google.com/iam
- https://aws.amazon.com/iam