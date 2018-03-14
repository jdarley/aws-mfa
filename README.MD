Script to generate AWS STS tokens for MFA enabled accounts
---

1. Create an AWS profile named bootstrap-{env} with the key and secret for the account secured by MFA
2. Create a bash script named {env}-config in your ~/.aws/ folder containing an environment variable for the AWS_ACCOUNT_ID and AWS_IAM_USERNAME corresponding to the profile in question
3. Place aws-mfa in your ~/bin folder

Run aws_mfa {mfa_code} to sign into the "default" profile
Run aws_mfa {profile} {mfa_code} to sign into the named profile
