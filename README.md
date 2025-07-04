# Aws_Practicals
This repository explains the major concepts and services in AWS cloud platform 

AWS IAM Explained Simply

** What is IAM?**
AWS Identity and Access Management (IAM) is like the security guard of your AWS account. It controls:

WHO can access your cloud resources (users & roles)

WHAT they can do (permissions via policies)

HOW they can access them (temporary or permanent access)

Key IAM Concepts
 Users : Represents a person or application that needs AWS access
Each gets unique credentials (password + access keys)

Follows the Principle of Least Privilege (only give necessary permissions)

 Groups : A way to organize users (e.g., "Developers", "Admins")
Assign permissions once to the group → all members inherit them

 Policies: JSON documents that define permissions (like rulebooks)
Example: "Allow read-only access to S3 but block deletions"

Roles: Temporary permissions for AWS services (EC2, Lambda, etc.)
Safer than hardcoding credentials (e.g., "Let this EC2 instance access S3")

IAM Best Practices
Enable MFA – Add an extra layer of security beyond passwords

Use Roles for Services – Never store credentials in code/configs

Audit Permissions – Regularly review who has access to what

Example Scenario
"You want to let a developer deploy EC2 instances only in Mumbai (ap-south-1):"

Create an IAM User for them
Attach a Custom Policy restricting EC2 to Mumbai
Add them to the "Dev-Team" Group for shared permissions

Next Steps: 
Try creating your first IAM user:
aws iam create-user --user-name test-user
Explore the AWS IAM Documentation for deeper learning!

![image](https://github.com/user-attachments/assets/0e79a65c-1b4f-4ad1-8bc2-cbbb127de784)

IAM is your first line of defense in AWS – configure it wisely! 
#########################################################################################################################################################################################

AWS AMI (Amazon Machine Image) Overview
An AMI (Amazon Machine Image) is a pre-configured virtual machine image used to launch EC2 instances. It contains:

OS (Amazon Linux, Ubuntu, Windows, etc.)

Software (pre-installed apps, configurations)

Permissions (launch controls via IAM roles)

Key Features
✅ Fast Deployment: Launch identical instances in seconds.
✅ Customization: Create your own AMIs from existing instances.
✅ Region-Specific: AMIs must be copied across regions.
✅ Backup/Restore: Create AMIs from EBS snapshots.

![image](https://github.com/user-attachments/assets/83faea33-74b3-4b07-9fb9-248567dbd234)

