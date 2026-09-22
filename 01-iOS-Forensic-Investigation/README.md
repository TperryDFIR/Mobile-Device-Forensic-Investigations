# iOS Forensic Investigation

## Investigation Overview

This case study documents hands-on examination of iOS forensic evidence as part of a mobile device forensics portfolio.

The investigation focuses on identifying, examining, and correlating artifacts that may help reconstruct device activity. Findings will be supported by documented forensic procedures, relevant tool output, and appropriately redacted screenshots.

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
| [Examination Methodology](Examination-Methodology.md) | Forensic tools and procedures used to examine the iOS report |
| [Artifact Findings](Artifact-Findings.md) | SmartLife application, email, network, and SQLite database artifacts |
| [Findings and Limitations](Findings-and-Limitations.md) | Final investigative conclusions and examination limitations |

## Featured Evidence Screenshots

The following screenshots document selected findings from the iPhone X evidence examination using Cellebrite Reader.

| Figure | Evidence demonstrated |
|---|---|
| [1. SmartLife Installed Application](Screenshots/01-SmartLife-Installed-Application.png) | Installed-application metadata |
| [2. SmartLife Case-Wide Search](Screenshots/02-SmartLife-Case-Wide-Search.png) | Search results across artifact categories |
| [3. SmartLife Database Search](Screenshots/03-SmartLife-Database-Search.png) | Identification of application-related SQLite databases |
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
