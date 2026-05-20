# Release and Maintenance

Definition: Evaluating the security of the release process and maintenance management level, reflecting the project's release quality and continuous maintenance capability.

# Assessment Model

**Release Quality**

| Metric | URL | Threshold | Weight |
| ------ | --- | --------- | ------ |
| SBOM Check | [/api/v3/release_quality/sbom_in_release](https://oss-compass.org/dataHub#api_v3_release_quality_sbom_in_release) | 1 | 0.25 |
| Binary Artifact Included | [/api/v3/release_quality/security_binary_artifact](https://oss-compass.org/dataHub#api_v3_release_quality_security_binary_artifact) | 1 | 0.25 |
| Package Signature | [/api/v3/release_quality/security_package_sign](https://oss-compass.org/dataHub#api_v3_release_quality_security_package_sign) | 1 | 0.25 |
| Release Notes | [/api/v3/release_quality/lifecycle_release_note](https://oss-compass.org/dataHub#api_v3_release_quality_lifecycle_release_note) | 1 | 0.25 |

**Maintenance Management**

| Metric | URL | Threshold | Weight |
| ------ | --- | --------- | ------ |
| Lifecycle Statement | [/api/v3/maintenance_management/lifecycle_statement](https://oss-compass.org/dataHub#api_v3_maintenance_management_lifecycle_statement) | 1 | 0.50 |
| Average Vulnerability Fix Time | [/api/v3/maintenance_management/avg_vulnerability_fix_time](https://oss-compass.org/dataHub#api_v3_maintenance_management_avg_vulnerability_fix_time) | 30 days | 0.50 |

# Metrics in Assessment Model

## Release Quality

The release quality model focuses on the security and standardization of the release process, ensuring the integrity and trustworthiness of release versions.

### SBOM Check

- Definition: Whether the release version includes a Software Bill of Materials (SBOM).
- Weight: 25%
- Threshold: 1 (Included)

SBOM (Software Bill of Materials) is a software bill of materials that records all components and dependencies contained in the software. Including SBOM can help users understand the composition of the software and identify potential security risks. This metric reflects the project's supply chain transparency.

### Binary Artifact Included

- Definition: Whether the release version includes binary artifacts.
- Weight: 25%
- Threshold: 1 (Included)

Binary artifacts are software packages that users use directly. Including binary artifacts can facilitate user installation and use, lowering the barrier to use. This metric reflects the project's user friendliness.

### Package Signature

- Definition: Whether the release version has been digitally signed.
- Weight: 25%
- Threshold: 1 (Signed)

Package signature is an important measure to ensure software integrity and authenticity. Through digital signatures, the source and integrity of software packages can be verified, preventing software packages from being tampered with. This metric reflects the project's security maturity.

### Release Notes

- Definition: Whether the release version includes release notes.
- Weight: 25%
- Threshold: 1 (Included)

Release Notes record version changes, new features, fixed issues, and other information. Complete Release Notes can help users understand version changes and make upgrade decisions. This metric reflects the project's documentation completeness.

## Maintenance Management

The maintenance management model focuses on the project's maintenance status and response capability, ensuring that the project receives continuous maintenance.

### Lifecycle Statement

- Definition: Whether the project declares its lifecycle status.
- Weight: 50%
- Threshold: 1 (Declared)

Lifecycle statement informs users of the project's current status (such as active, maintenance, archived, etc.). A clear lifecycle statement can help users understand the project's maintenance status and make usage decisions. This metric reflects the project's transparency and user care.

### Average Vulnerability Fix Time

- Definition: The average time for the project to fix security vulnerabilities.
- Weight: 50%
- Threshold: 30 days

Average vulnerability fix time is an important indicator of the project's security response capability. A shorter fix time can reduce the time users are exposed to security risks, protecting user security. This metric reflects the project's security maintenance capability.

# Assessment Model Algorithm

## Weight

The weights of each metric are equally distributed.

### Release Quality

4 metrics are equally distributed, with each metric having a weight of 25%.

### Maintenance Management

2 metrics are equally distributed, with each metric having a weight of 50%.

## Threshold

The thresholds we selected are based on big data observations of different types of open source projects.
