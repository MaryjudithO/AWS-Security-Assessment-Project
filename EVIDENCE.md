# Evidence Collected

## AWS Console Screenshots

The following screenshots were collected as evidence during the AWS security assessment:

- IAM Users Configuration
- Multi-Factor Authentication (MFA) Status
- IAM Policy Assignments
- Security Group Rules
- Amazon S3 Bucket Configuration
- Amazon EC2 Instance Configuration
- S3 Encryption Settings
- AWS Monitoring and Logging Configuration

## Prowler Assessment Evidence

Evidence collected from the Prowler security assessment includes:

- Prowler Installation
- Prowler Scan Execution
- Security Findings Report
- Compliance Assessment Results
- Failed Security Controls
- Generated HTML, CSV, and JSON Reports
- Risk Validation Results

## Architecture Evidence

The following architecture diagrams were developed as part of the assessment:

### Before Remediation
- IAM User without MFA
- AdministratorAccess assigned to test-user-1
- SSH (Port 22) open to 0.0.0.0/0
- Publicly Accessible S3 Bucket
- Weak Security Group Configuration

### After Remediation
- MFA Enabled
- Least-Privilege Access Controls Implemented
- SSH Restricted to Trusted IP Addresses
- Private S3 Bucket Configuration
- Encryption Enabled
- Enhanced Monitoring and Logging

## Supporting Documentation

- AWS Cloud Security Assessment Report
- Risk Analysis Matrix
- Security Recommendations
- Remediation Plan
- Prowler Assessment Results
- GitHub Project Repository
