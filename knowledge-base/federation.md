# Identity Federation

# Definitions

- **Federation** in short words is a way of combining / joining list of users with list of users from another service.
- **Identity Broker** is a service that allows to take an identity from point *A* and join it (federate it) to point *B*.
- **Identity Store** is a service that stores the data about users (e.g. *AD*, *Google*, *FB*).
- **Identities** describes users of the system.
- **AssumeRole** is a mechanism used by *AWS* in order to take provided authenticated user from external source and associate it with *IAM role* that gives permissions to the cloud resources. In that scenario you are not storing users inside *IAM*.

## Identity Management

### Classic Federation

It is a mechanism that allows to separate identity provider from *AWS*. Often used together with enterprise identity brokers like *LDAP* or *Active Directory*, but supports out of the box any *SAML* compatible identity broker. If your broker does not support *SAML 2.0*, you are still able to leverage federation, but you need to provide additional implementation on your own.

### Web Identity Federation (*OpenID*)

It is identical mechanism to the *federation* explained above, but it uses different identity storage and protocol. Those capabilities are provided by external, 3rd party company - e.g. *Facebook*, *Google* or *Github*. All those providers implements *OpenID* that is used in that case. Flow and mechanism looks identically, the only difference lies in different identity store being hit.

### Cross Account Access

You are also able to federate two different *AWS* accounts and use identities stored inside one account *IAM* service to authenticate in second account.

# Flow

1. User authenticates against identity store via broker.
2. Identity broker authenticates with store first, then it hits *AWS Security Token Service*.
3. *AWS STS* generates temporary access tokens that allows for access to the resources (`AssumeRole`).
4. Tokens are returned to the user client application and from now on user is able to access *AWS* resources, accordingly to the role.

## References

- https://aws.amazon.com/identity/federation