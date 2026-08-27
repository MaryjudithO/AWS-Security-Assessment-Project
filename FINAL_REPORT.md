# AWS Security Assessment Report

## Executive Summary

This report presents the results of a security assessment conducted on the Amazon Web Services (AWS) environment of Northbridge Retail Co. The objective was to identify security vulnerabilities, evaluate associated business risks, and recommend remediation measures to improve the organization's cloud security posture.

The assessment focused on identity and access management, network security, data protection, encryption controls, and security monitoring. Automated validation was performed using Prowler to assess compliance and identify security gaps.

Several security weaknesses were identified, including missing Multi-Factor Authentication (MFA), excessive IAM permissions, publicly accessible resources, open administrative ports, and weak security configurations. Recommendations have been provided to address these findings and strengthen the overall security posture of the environment.

## Business Scenario

Northbridge Retail Co. recently migrated its business applications and resources to AWS. As the organization expanded its cloud presence, management became concerned about potential security misconfigurations that could expose sensitive business resources to unauthorized access and data breaches.

A security assessment was requested to identify and evaluate security weaknesses within the AWS environment before an upcoming compliance review.

The assessment focused on the following areas:

- Open ports
- Publicly accessible resources
- IAM security risks
- Missing Multi-Factor Authentication (MFA)
- Missing encryption controls
- Security Group weaknesses


## Assessment Methodology

### Identity Management Review

The Identity and Access Management (IAM) configuration was reviewed to identify excessive permissions, insecure user configurations, and accounts without Multi-Factor Authentication.

### Network Security Review

Security Groups and EC2 configurations were evaluated to identify unnecessary internet exposure and open administrative ports.

### Data Security Review

Amazon S3 bucket permissions and encryption settings were reviewed to identify publicly accessible data and missing encryption controls.

### Automated Validation

Prowler was used to perform an automated security assessment against AWS security best practices and compliance requirements.

## Findings

### Finding 1: Missing Multi-Factor Authentication (MFA)

**Observation:**  
Privileged IAM users were configured without MFA.

**Risk:**  
Unauthorized users who obtain credentials may gain access to AWS resources.

**Severity:** High

**Recommendation:**  
Enable MFA for all IAM users, especially privileged accounts.


### Finding 2: Excessive IAM Permissions

**Observation:**  
An IAM user was assigned AdministratorAccess permissions.

**Risk:**  
Compromised credentials could result in full control of cloud resources.

**Severity:** High

**Recommendation:**  
Implement the principle of least privilege.



### Finding 3: Open Administrative Port (SSH)

**Observation:**  
Port 22 (SSH) was accessible from 0.0.0.0/0.

**Risk:**  
Attackers may attempt unauthorized access through brute-force attacks.

**Severity:** Medium

**Recommendation:**  
Restrict SSH access to trusted IP addresses only.



### Finding 4: Publicly Accessible S3 Bucket

**Observation:**  
An S3 bucket allowed public access.

**Risk:**  
Sensitive information may be exposed to unauthorized parties.

**Severity:** Critical

**Recommendation:**  
Enable Block Public Access and review bucket policies.



### Finding 5: Missing Encryption Controls

**Observation:**  
Data storage resources were not configured with encryption.

**Risk:**  
Sensitive information may be exposed if storage resources are compromised.

**Severity:** High

**Recommendation:**  
Enable server-side encryption for all applicable storage services.



### Finding 6: Security Group Weaknesses

**Observation:**  
Security Group rules were overly permissive.

**Risk:**  
Unnecessary network exposure increases the attack surface.

**Severity:** Medium

**Recommendation:**  
Review and restrict inbound and outbound traffic rules.



## Risk Analysis

| Finding | Risk Level |
|----------|-----------|
| Missing MFA | High |
| Excessive IAM Permissions | High |
| Open SSH Port | Medium |
| Public S3 Bucket | Critical |
| Missing Encryption | High |
| Security Group Weaknesses | Medium |



## Security Recommendations

### Immediate Actions (0-7 Days)

- Enable MFA on all privileged accounts
- Remove public access from S3 buckets
- Restrict SSH access

### Short-Term Actions (1-4 Weeks)

- Review IAM permissions
- Implement least-privilege access
- Enable encryption for sensitive data

### Long-Term Actions (1-3 Months)

- Conduct regular security assessments
- Implement continuous monitoring
- Perform periodic compliance reviews



## Conclusion

The AWS security assessment identified several configuration weaknesses that could increase the likelihood of unauthorized access, data exposure, and compliance issues. The findings demonstrate the importance of implementing AWS security best practices, including strong identity management, secure network configurations, encryption, and continuous monitoring.

Implementing the recommended remediation measures will significantly improve the security posture of the AWS environment and reduce overall business risk.


