# Create IAM policies with Terraform

IAM identities (users, groups, or roles) must be assigned explicit permissions to access AWS resources.
The associated IAM policy determines the privileges available to an IAM identity.
Policies are JSON documents that define explicit allow/deny privileges to specific resources or resource groups.
I create an IAM user and an S3 bucket. I map permissions for that S3 bucket with an IAM policy. I attach that policy to the new user.
An IAM policy resource is the starting point for creating an IAM policy in Terraform.
The main.tf file contains an IAM policy resource, an S3 bucket, and a new IAM user.
The name in my policy is a random_pet string to avoid duplicate policy names.
The iam_policy resource and iam_policy_document data source used together will create a policy. I create a policy attachment for my policy to apply to my users.
