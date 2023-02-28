# IAM
## Users, Groups and Principles
- Identity and Access Management - Global Service
- Root account created by default, shouldn't be used or shared (just used to setup your account)
- create users in IAM which represent people within an organization (which can be grouped together if it makes sense to do so e.g. developers, operations etc...)
- groups can only contain users (i.e. no nesting groups)
- users can be part of multiple groups
- users or groups can be assigned a JSON document called a policy
- policies describe what users are allowed to do (least privilege principle), they define user permissions

## Policies
- Group policies: every user in the group will inherit a group's policies e.g. developers, auditors, operations
- Inline policies: policy attached to individual user(s)

Policy Structure
- Version: policy language version, always include "2012-10-17"
- Id: identifier for policy (optional)
- Statement: list of one or more statements (required)
  - Sid: identifier for statement (optional)
  - Effect: whether the statement allows or denies access (Allow, Deny)
  - Principal: account/user/role to which this policy applies
  - Action: list of actions allowed/denied by this policy
  - Resource: list of resources the actions apply to
  - Condition: when this policy is in effect (optional)
```json
{
    "Version": "2012-10-17",
    "Id": "S3-Account-Permissions",
    "Statement": [
        {
            "Sid":"1",
            "Effect": "Allow",
            "Principal": {
                "AWS":["arn:aws:iam::123456789012:root"]
            },
            "Action": [
                "s3:GetObject",
                "s3:PutObject"
            ],
            "Resource": ["arn:aws:s3:::mybucket/*"]
        }
    ]
}
```

## MFA
Password Policy
- minimum password length
- require specific character types
  - lower case
  - upper case
  - numbers
  - non-alphanumerics
- allow all IAM users to change their own passwords
- require users to change their passwords periodically (expiration)
- prevent password re-use

POSSIBLE EXAM QUESTION: Multi-Factor Authentication (MFA)
- users have acces to change configurations or delete resources in your AWS account
- protect Root accounts and IAM users
- MFA = password (you know) + security device (you own)
- MFA Device options in AWS
  - Virtual MFA Device: support multiple tokens on a single device
    - Google Authenticator (mobile only)
    - Authy (multi-device)
  - Universal 2nd Factor (U2F) Security Key: support multiple root and IAM users using a signle security key e.g. YubiKey by Yubico (3rd party)
  - Hardware Key Fob MFA Device e,g, Gemalto (3rd party)
  - Hardware Key Fob MFA Device for AWS GovCloud (US) e.g. SurePassID (3rd party)