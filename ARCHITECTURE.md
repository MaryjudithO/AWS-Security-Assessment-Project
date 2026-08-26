# Solution Design

## Overview

The recommended solution follows a defense-in-depth approach by implementing multiple security controls across identity management, network security, data protection, and monitoring services.

The goal is to reduce the attack surface, prevent unauthorized access, protect sensitive data, and improve visibility into security-related activities within the AWS environment.

## Before Assessment

The AWS environment contained several security weaknesses:

- IAM user without Multi-Factor Authentication (MFA)
- Excessive IAM permissions
- Open SSH access (Port 22) exposed to the internet
- Publicly accessible S3 bucket
- Missing encryption controls
- Limited monitoring and logging capabilities

These weaknesses increased the risk of unauthorized access, data exposure, and potential compromise of cloud resources.

## After Remediation

The recommended secure environment includes:

- MFA enabled for all privileged users
- Least privilege access applied to IAM users and roles
- Restricted Security Group rules allowing access only from trusted IP addresses
- Private and secured S3 buckets with Block Public Access enabled
- Encryption enabled for data at rest and in transit
- Enhanced monitoring through AWS CloudTrail and CloudWatch
- Regular security assessments using Prowler

## Security Improvements

The proposed security controls provide the following benefits:

- Stronger authentication and access control
- Reduced risk of credential compromise
- Protection of sensitive information
- Reduced network exposure
- Improved visibility into security events
- Better alignment with AWS security best practices

## Architecture Diagram

The architecture diagram illustrating the AWS environment before and after remediation is included in the project deliverables and supporting evidence.
