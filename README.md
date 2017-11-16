# *AWS Identity Access Management* - Workshop

## Editions

- [NatywnaChmura.pl (13.01.2018, Gliwice)](http://natywnachmura.pl)

## Motivation

Our main goal is to introduce and explain *AWS IAM* in a simple and approachable way, with showing real world examples and best practices. We cover also identity management automation process, organizations and hierarchical structure, consolidated billing and differences with other cloud providers (*Azure*, *Google Cloud*).

## Tools

Repository contains tools that are setup inside a `virtualenv`. If you are interested in details, please have a look inside `Makefile`.

If you want to use *MFA* together with this setup, you need to provide additional configuration to your `~/.aws/credentials` file:

```
[default-long-term]
aws_access_key_id = ...
aws_secret_access_key = ...
mfa_serial = arn:aws:iam::<ACCOUNT_ID>:mfa/<IAM_USER>

```

## License

[Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)](LICENSE.md)
