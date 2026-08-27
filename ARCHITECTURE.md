# Solution Design

## Overview

The recommended solution follows a defense-in-depth approach by implementing multiple security controls across identity management, network security, data protection, and monitoring. The objective is to reduce the attack surface, prevent unauthorized access, protect sensitive data, and improve visibility into security-related activities within the AWS environment.

## Before Remediation

The AWS environment contained several security weaknesses that increased the risk of unauthorized access, data exposure, and potential compromise of cloud resources.

- IAM user without Multi-Factor Authentication (MFA)
- Excessive IAM permissions assigned to users
- Open SSH access (Port 22) exposed to the internet
- Publicly accessible S3 bucket
- Missing encryption controls
- Limited monitoring and logging capabilities

## After Remediation

The recommended secure environment includes the following improvements:

- MFA enabled for all privileged users
- Least-privilege access applied to IAM users and roles
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

### Before Remediation


                Internet
                    |
                    v
            EC2 Instance
                    |
                    v
      Security Group (SSH Open)
          Port 22 = 0.0.0.0/0
                    |
                    v
      IAM User: test-user-1
      - No MFA Enabled
      - AdministratorAccess
                    |
                    v
              S3 Bucket
      - Publicly Accessible
      - Weak Security Controls


### After Remediation

                Internet
                    |
                    v
            EC2 Instance
                    |
                    v
      Hardened Security Group
      - Restricted SSH Access
      - Trusted IP Addresses Only
                    |
                    v
      IAM User: test-user-1
      - MFA Enabled
      - Least-Privilege Access
                    |
                    v
              S3 Bucket
      - Block Public Access Enabled
      - Encryption Enabled
                    |
                    v
      Monitoring & Logging
      - AWS CloudTrail
      - AWS CloudWatch
      - Prowler Assessments


The architecture illustrates the AWS environment before and after remediation, highlighting the security improvements recommended to strengthen access control, network security, data protection, and monitoring.
