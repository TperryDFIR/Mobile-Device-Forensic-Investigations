# Android IoT Forensic Investigation

## Investigation Overview

This case study documents the examination of Android and IoT-related
forensic evidence as part of a mobile device forensics portfolio.

The investigation focuses on identifying relevant device, application,
network, and database artifacts; correlating findings across available
evidence sources; and documenting the limitations of the examination.

## Investigation Objectives

- Identify the available Android and IoT evidence sources.
- Document the forensic tools and examination methods used.
- Examine relevant application and device artifacts.
- Correlate findings across available evidence sources.
- Develop evidence-supported investigative conclusions.
- Protect sensitive information in public documentation.

## Key Findings

The Galaxy S8 Physical evidence examination identified several Android and IoT-related artifacts:

| Artifact | Evidence-Supported Finding |
|---|---|
| ezDevice application | Application-related artifacts were identified in the examined evidence. |
| Case-wide search | A search for `ezdevice` returned 144 results across multiple artifact categories. |
| Cookie record | An `NID` cookie associated with `.google.com` contained source and timestamp information useful for correlation. The cookie value is redacted in public documentation. |
| Network usage | A wireless network-usage record showed activity on June 6, 2024, from 06:00 to 08:00 UTC, with 1,391 bytes received and 834 bytes sent. |
| RKStorage database | Serialized application data included account-configuration fields and an ezOutlet2 device record. Sensitive identifiers and credential values are redacted. |
| ezOutlet2 network settings | Stored configuration fields included automatic DNS, DHCP, gateway, DNS servers, hostname, IP address, subnet mask, and HTTP port. |
| Timestamp analysis | DCode was used to decode a Unix millisecond timestamp for comparison with other forensic artifacts. |

These findings document artifacts present in the examined dataset. Individual records do not, by themselves, establish who operated a device, whether a login succeeded, or whether a network connection occurred at a particular timestamp.

See [Artifact Findings](Artifact-Findings.md) for screenshots, detailed observations, and forensic significance.

## Case Documentation

| Report | Description |
|---|---|
| [Evidence and Scope](Evidence-and-Scope.md) | Galaxy S8 evidence source, examination scope, and limitations |
| [Examination Methodology](Examination-Methodology.md) | Cellebrite Reader examination procedures |
| [Artifact Findings](Artifact-Findings.md) | Android and IoT application, cookie, network, database, and timestamp findings |

