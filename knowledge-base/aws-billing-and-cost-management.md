# AWS Billing and Cost Management

## Consolidated Billing.

It is a mechanism consisting of one paying account, linked to *separate AWS accounts* that are called *linked accounts*. Limit of 20 linked accounts for one paying account for a consolidated billing. It looked that way in the past, currently the only default way is to use *AWS Organizations*.

Paying account will receive monthly billing for all linked accounts (with distinction) and total bill. Each account is independent - cannot access resources of other accounts (unless explicitly specified). *Free tier* is still applied separately for each account.

### Advantages

- One bill per *AWS* account.
- Very easy to track charges and cost allocation.
- Easier to get discounts:
  - E.g. volume pricing discount.
  - *S3* storage sums up and than discounts are applied.