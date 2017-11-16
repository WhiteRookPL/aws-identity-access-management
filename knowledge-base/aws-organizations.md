# AWS Organizations

<p align="center">
  <img src="https://github.com/WhiteRookPL/aws-identity-access-management/raw/master/knowledge-base/assets/organizations.png" />
</p>

## Description

**AWS Organizations** offers policy-based management for multiple AWS accounts. With Organizations, you can create groups of accounts and then apply policies to those groups. Organizations enables you to centrally manage policies across multiple accounts, without requiring custom scripts and manual processes. You are able to create default policy that narrows down security for a created account.

## Automation

```
for I in `seq -f"%03g" 1 22`; do
  aws organizations create-account --email "account_$I@email.account.com"
                                   --account-name "account$I"
                                   --iam-user-access-to-billing "ALLOW"
  sleep 2
done
```

## Limits

Limit by default:

- 20 accounts for main organization.
- 1000 organization units.
- At most 1-2 days of wait for increasing limit.

## References

- https://aws.amazon.com/blogs/security/how-to-use-aws-organizations-to-automate-end-to-end-account-creation/
- http://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_accounts_remove.html#leave-without-all-info