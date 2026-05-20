# Source Code Management

Definition: Evaluating the security management level of source code, reflecting the project's legal compliance and security protection capability.

# Assessment Model

**Legal Compliance**

| Metric | URL | Threshold | Weight |
| ------ | --- | --------- | ------ |
| License Header and Copyright Statement | [/api/v3/legal_compliance/compliance_copyright_statement](https://oss-compass.org/dataHub#api_v3_legal_compliance_compliance_copyright_statement) | 1 | 0.25 |
| License Inclusion (OSI) | [/api/v3/legal_compliance/compliance_license](https://oss-compass.org/dataHub#api_v3_legal_compliance_compliance_license) | 1 | 0.25 |
| License Compatibility | [/api/v3/legal_compliance/compliance_license_compatibility](https://oss-compass.org/dataHub#api_v3_legal_compliance_compliance_license_compatibility) | 1 | 0.25 |
| License and Copyright Statement Anti-Tamper | [/api/v3/legal_compliance/compliance_copyright_anti_tamper](https://oss-compass.org/dataHub#api_v3_legal_compliance_compliance_copyright_anti_tamper) | 1 | 0.25 |

**Security Management**

| Metric | URL | Threshold | Weight |
| ------ | --- | --------- | ------ |
| Vulnerability Response and Disclosure | [/api/v3/security_management/vulnerability_disclosure](https://oss-compass.org/dataHub#api_v3_security_management_vulnerability_disclosure) | 1 | 0.50 |
| Public Unfixed Vulnerabilities | [/api/v3/security_management/security_vulnerability](https://oss-compass.org/dataHub#api_v3_security_management_security_vulnerability) | 1 | 0.50 |

# Metrics in Assessment Model

## Legal Compliance

The legal compliance model focuses on the project's legal compliance, ensuring that the project meets standards in intellectual property and licensing.

### License Header and Copyright Statement

- Definition: Whether the project includes license headers and copyright statements in source code files.
- Weight: 25%
- Threshold: 1 (Compliant)

License headers and copyright statements are important measures for protecting intellectual property. Including license headers in source code files can clarify the usage rights of the code and protect the rights of contributors. This metric reflects the project's emphasis on intellectual property protection.

### License Inclusion (OSI)

- Definition: Whether the project includes an OSI (Open Source Initiative) recognized open source license.
- Weight: 25%
- Threshold: 1 (Compliant)

OSI recognized open source licenses are standard configurations for open source projects. Using OSI recognized licenses can ensure the open source nature of the project and avoid legal risks. This metric reflects the project's open source compliance and legal risks.

### License Compatibility

- Definition: Whether the licenses used by the project are compatible with each other.
- Weight: 25%
- Threshold: 1 (Compatible)

License compatibility is an important aspect of open source project compliance. Incompatible license combinations may lead to legal disputes and usage restrictions. This metric reflects the project's license management level and legal risks.

### License and Copyright Statement Anti-Tamper

- Definition: Whether the project takes measures to prevent license and copyright statements from being tampered with.
- Weight: 25%
- Threshold: 1 (Compliant)

License and copyright statement anti-tamper is an important measure for protecting project intellectual property. Preventing tampering through technical means can ensure the validity of licenses and copyright statements. This metric reflects the project's security protection capability.

## Security Management

The security management model focuses on the project's security vulnerability management, ensuring that the project can timely discover and fix security vulnerabilities.

### Vulnerability Response and Disclosure

- Definition: Whether the project has a complete vulnerability response and disclosure mechanism.
- Weight: 50%
- Threshold: 1 (Compliant)

Vulnerability response and disclosure mechanisms are important components of open source project security management. A complete mechanism can ensure that security vulnerabilities receive timely response and handling, protecting user security. This metric reflects the project's security management maturity.

### Public Unfixed Vulnerabilities

- Definition: Whether the project has public unfixed security vulnerabilities.
- Weight: 50%
- Threshold: 1 (None)

Public unfixed vulnerabilities are important indicators of project security risks. Unfixed vulnerabilities may be maliciously exploited, threatening user security. This metric reflects the project's security risks and maintenance quality.

# Assessment Model Algorithm

## Weight

The weights of each metric are equally distributed.

### Legal Compliance

4 metrics are equally distributed, with each metric having a weight of 25%.

### Security Management

2 metrics are equally distributed, with each metric having a weight of 50%.

## Threshold

The thresholds we selected are based on big data observations of different types of open source projects.
