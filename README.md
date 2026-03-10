# AWS IAM Roles & Policies Lab


![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![AWS](https://img.shields.io/badge/AWS-IAM-orange)


## Project Structure
- README.md  
- screenshots/  


## Overview
This lab helped me understand how IAM roles, policies, and temporary permissions work in AWS. The goal was to see how users can safely get elevated access when they need it, and how that access can be removed when no longer required.


## What I did
- Created IAM users with different permission levels  
- Assigned policies and tested access restrictions  
- Created IAM roles and configured trust relationships  
- Generated temporary credentials through AWS STS  
- Verified how permissions change depending on the user or role  
- Removed access once tasks were completed

  

## IAM Flow Diagram
Below is a simple diagram showing how the user, group, role, and policies interact in this lab:


![IAM Flow Diagram](https://github.com/Chi-buike/aws-iam-lab/blob/main/screenshots/iam-flow-diagram.png?raw=true)


## Creating the policies
I created two simple custom policies:
a read‑only policy
a CRUD policy

I attached them to the correct roles and updated each role’s trust relationship so only one specific user could assume it.


## Testing the roles
When I logged in as the regular user:
assuming the read‑only role allowed me to view EC2 instances
assuming the CRUD role allowed actions like terminating an instance

This showed how temporary elevated permissions work in practice.


## Revoking sessions
I tested revoking an active session. After the admin revoked the CRUD session, the standard user instantly lost access once the console was refreshed. This showed how AWS can cut off temporary credentials immediately.


## Using the CLI
To finish the lab, I used Session Manager to connect to an EC2 instance and worked with the AWS CLI. I checked my identity, tested permissions, created policies, attached roles, and assumed a role from the CLI.

## Conclusion
This lab helped me practice IAM concepts like policies, roles, session revocation, and role assumption using both the console and CLI.


## What I learned
This lab gave me practical experience with:
creating IAM policies
attaching and trusting IAM roles
assuming temporary roles
revoking access sessions
and using both the console and CLI to manage permissions

## Screenshots
All screenshots from the lab are available in the **/screenshots** folder.

## How I ran this lab
This lab was completed using AWS Skills Builder. All resources were provided by the lab environment.
