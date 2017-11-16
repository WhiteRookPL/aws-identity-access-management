# Tips and Tricks

There are various tips and tricks when it comes to securing your *AWS* account, we have collected them for you in the following points:

- Enforce security settings for Identity and Access Management (IAM) accounts.
  - Have proper *IAM* policies in place.
  - Enforce *MFA* and longer passwords via *IAM*.
  - Generate frequently credential reports and discuss the most resistant users.
- Rotate your AWS keys.
  - Have proper *IAM* policies in place.
- Do not commit AWS access keys or credentials!
  - Extract all your keys from *IAM* via `aws-cli` and then use `grep`.
  - Leverage *Amazon Macie* if you can.
  - Use *IAM Instance Profiles* instead of hard-coding keys inside *EC2* instances.
- Keep your security groups minimal.
  - Enable *AWS Trusted Advisor*.
  - Limit *SG* to only necessary *IP* ranges and ports.
- Use a private *VPC*.
  - Leverage internal *ELBs* in order to narrow down connectivity between services.
- Use *AWS Trusted advisor*.
  - Enable that service, even if you apply only to the basic plan.
    - If 100 USD per month is too much.
- Enable *AWS CloudTrail*.
  - If you have limited money, track only most important events (*IAM*, *Billing*, *CloudWatch*).
  - Leverage *SNS* to notify when new update is available.
  - Invest in *Amazon Macie* or automated tool customized to your needs.
- Update your *Amazon Machine Images* (*AMI*).
  - Apply security patches regularly.
  - Follow the hardening guide: https://aws.amazon.com/articles/public-ami-publishing-hardening-and-clean-up-requirements
  - Do not bake *IAM* access keys inside *AMI*.
- Choose your rights carefully.
  - Apply always rule of the least privilege.
- Monitor billing.
  - Setup billing alarms.
  - Create budgets and limit your spent money.
- Leverage AWS Security whitepapers.
  - https://d0.awsstatic.com/whitepapers/compliance/AWS_Auditing_Security_Checklist.pdf
  - https://d0.awsstatic.com/whitepapers/Security/AWS_Security_Best_Practices.pdf