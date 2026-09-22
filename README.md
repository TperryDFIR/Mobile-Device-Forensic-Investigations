# Mobile Device Forensic Investigations

## Project Overview

This portfolio documents hands-on forensic examinations of existing iOS and Android mobile device evidence, focusing on application artifacts, SQLite databases, network records, IoT-related activity, and forensic timeline analysis.

The investigations demonstrate how mobile device evidence can be examined, interpreted, correlated, and documented using Cellebrite Reader, DCode, and repeatable forensic examination procedures.

The documented examinations used provided forensic datasets. Original device acquisition was not performed as part of these case studies.

## Investigation Objectives

* Examine mobile device evidence using appropriate forensic tools and methods.
* Compare mobile extraction methods and the artifacts they provide.
* Identify and interpret application and operating system artifacts.
* Examine SQLite databases to recover and correlate relevant records.
* Analyze Android and iOS evidence in the context of investigative questions.
* Document findings, limitations, and evidence-handling procedures.

## Tools and Technologies

| Tool or Technology | Investigative Purpose |
|---|---|
| Cellebrite Reader | Examine mobile forensic reports and identify application, device, network, and database artifacts |
| DCode | Interpret encoded timestamps for forensic timeline analysis |
| SQLite databases | Examine application-specific records and stored artifacts |
| iOS forensic artifacts | Investigate iPhone application, email, network, and database evidence |
| Android forensic artifacts | Investigate application, cookie, network, database, and IoT-related evidence |

## Investigation Documentation

| Investigation | Evidence Examined | Case Study |
|---|---|---|
| iOS Forensic Investigation | iPhone X SmartLife application, registration emails, wireless-network records, SQLite databases, and timestamp artifacts | [View iOS Investigation](01-iOS-Forensic-Investigation/README.md) |
| Android and IoT Forensic Investigation | Galaxy S8 ezDevice application, cookie, network, database, IoT device, and timestamp artifacts | [View Android Investigation](02-Android-IoT-Forensic-Investigation/README.md) |

### Android and IoT Case Study

### iOS Forensic Investigation

The iOS investigation includes:

- Examination of an existing iPhone X full file system forensic report
- SmartLife installed-application metadata and permissions
- Case-wide search identifying 1,213 SmartLife-related results
- Registration-related email and wireless-network artifacts
- SmartLife and Wyze SQLite database examination
- DCode timestamp interpretation
- Supporting Cellebrite Reader screenshots and documented examination limitations

[Read the iOS Artifact Findings](01-iOS-Forensic-Investigation/Artifact-Findings.md)

### Android and IoT Forensic Investigation

The Android investigation includes:

- Examination of an existing Samsung Galaxy S8 forensic dataset
- ezDevice application identification and artifact searches
- Cookie and application-related database examination
- Network-usage artifact analysis
- ezOutlet2 IoT device and network configuration records
- DCode timestamp interpretation
- Redacted screenshots supporting documented forensic findings

[Read the Android Artifact Findings](02-Android-IoT-Forensic-Investigation/Artifact-Findings.md)

## Forensic Methodology

Each case study documents the investigative objective, evidence source, tools used, examination process, relevant findings, and limitations. Supporting screenshots demonstrate procedures and substantiate documented findings where appropriate.

## Evidence Handling and Privacy

This public repository is intended to demonstrate forensic methodology and technical skills. Raw forensic images, extraction packages, credentials, personal communications, and sensitive identifying information will not be published.

## Portfolio

**Examiner:** Terrance Perry  
**Specialization:** Digital Forensics and Incident Response  

**Related Project:** [Windows NTFS Forensic Investigation](https://github.com/TperryDFIR/Windows-NTFS-Forensic-Investigation)
