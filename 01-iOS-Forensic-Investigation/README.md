# iOS Forensic Investigation

## Investigation Overview

This case study documents the examination of an existing iPhone X full file system forensic report using Cellebrite Reader.

The investigation focuses on SmartLife application artifacts, registration-related emails, wireless-network records, application databases, and timestamp analysis. Findings are supported by documented examination procedures and selected forensic screenshots.

The examination was performed using an existing forensic report; the original device acquisition was not performed as part of this documented investigation.

## Key Evidence Examined

This investigation examined an existing iPhone X full file system report using Cellebrite Reader. The analysis focused on SmartLife and related mobile and IoT artifacts.

The documented findings include:

- SmartLife application metadata and listed permissions
- A case-wide search returning 1,213 SmartLife-related results
- Registration-verification email artifacts
- Application and network-usage records
- SmartLife-related wireless-network records
- SQLite database artifacts associated with SmartLife and Wyze
- Timestamp interpretation using DCode

These findings provide leads for timeline reconstruction and cross-artifact correlation. Individual records do not independently prove device operation or identify the person responsible for an action.

## Detailed Findings

[View the iOS Artifact Findings](Artifact-Findings.md)

## Investigation Objectives

- Identify the available iOS evidence and its source.
- Document the forensic tools and examination methods used.
- Examine relevant device, application, and user-activity artifacts.
- Correlate findings across available evidence sources.
- Record the limitations of the examination.
- Present findings without exposing sensitive personal information.

## Case Documentation

| Report | Description |
|---|---|
| [Evidence and Scope](Evidence-and-Scope.md) | iPhone X evidence source, examination scope, and limitations |
| [Examination Methodology](Examination-Methodology.md) | Cellebrite Reader examination procedures |
| [Artifact Findings](Artifact-Findings.md) | SmartLife application, email, network, database, and timestamp findings |
| [Findings and Limitations](Findings-and-Limitations.md) | Investigative conclusions and examination limitations |

## Featured Evidence Screenshots

The following screenshots document selected findings from the iPhone X evidence examination using Cellebrite Reader.

| Figure | Evidence Demonstrated |
|---|---|
| [1. SmartLife Installed Application](Screenshots/01-SmartLife-Installed-Application.png) | Installed-application metadata and permissions |
| [2. SmartLife Case-Wide Search](Screenshots/02-SmartLife-Case-Wide-Search.png) | 1,213 SmartLife-related search results |
| [3. SmartLife Database Search](Screenshots/03-SmartLife-Database-Search.png) | SmartLife `Cache.db` examination |
| [4. Wyze Observations Database](Screenshots/04-Observations-Database.png) | Examination of `observations.db` and its `OperatingDates` table |

For the analysis and interpretation of these screenshots, see the
[Artifact Findings report](Artifact-Findings.md).

## Investigative Conclusion

The examination identified installed-application metadata, registration-related
emails, network records, and SQLite database artifacts that may support timeline
reconstruction and cross-source correlation. The findings are limited to the
available iPhone X evidence and do not independently establish user attribution
or operation of a particular IoT device.

## Evidence Handling and Privacy

Original forensic evidence, extracted personal information, account credentials, and unredacted private communications are excluded from this public repository.

This portfolio contains investigation documentation and selected supporting screenshots only.
