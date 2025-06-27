# Aws_Practicals
This repository explains the major concepts and services in AWS cloud platform 

**AWS IAM (Identity and Access Management) - Quick Overview**

 IAM is AWS’s security service that controls who (users/roles) can access what (AWS resources) and how (policies).

Key Components
Concept	Description	Use Case
Users	Individuals (people/apps) with credentials	Granting developers access to specific services
Groups	Collections of users with shared permissions	Assigning Admin or Dev team permissions
Policies	JSON rules defining permissions	Restricting EC2 creation to a specific region
Roles	Temporary permissions for AWS services	Letting an EC2 instance read from S3
Best Practices
✅ Least Privilege – Grant minimal required access.
✅ MFA – Enforce multi-factor authentication.
✅ Use Roles – Avoid hardcoding credentials in apps.

 Example: Custom Policy to restrict EC2 to Mumbai region.

** Try it yourself:
**

Create a User with S3ReadOnly access.

Build a Custom Policy with region restrictions.

Assign a Role to an EC2 instance.
