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
