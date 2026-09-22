
# iOS Forensic Investigation: Artifact Findings

## Investigation Overview

This case study documents artifacts identified in an iPhone X full file system report using Cellebrite Reader. The examination focused on the SmartLife application and associated application, email, network, and database records.

The findings below are based on the completed Lab 8.1 iOS IoT Evidence examination.

## 1. Installed Application Artifacts

Cellebrite Reader identified the following SmartLife application information:

| Artifact | Finding |
|---|---|
| Application | SmartLife |
| Version | 5.5.4 |
| Application identifier | `com.tuya.smartlife` |
| Recorded purchase date | August 27, 2021, 8:10:16 PM UTC |
| Listed permissions | HomeKit, Bluetooth, and Camera |

**Forensic significance:** Application metadata can help establish which software was present in the examined device report and identify related artifacts for further examination. The recorded purchase date should not automatically be treated as proof of first use.

## 2. Case-Wide Artifact Search

A case-wide search for `smartlife` returned **1,213 results**.

The worksheet identified these result categories:

- Aggregated Application Usage
- Application Usage Log
- Emails
- Installed Applications
- Log Entries
- Wireless Networks

**Forensic significance:** Searching across artifact categories provides a way to correlate application records with communications, usage data, and network information.

## 3. Email Artifacts

The search identified **five emails** containing `smartlife`.

The completed worksheet describes these as registration-verification emails associated with different applications.

| Email | Recorded timestamp (UTC) |
|---|---|
| 1 | May 25, 2021, 3:08:13 AM |
| 2 | April 3, 2022, 7:33:19 PM |
| 3 | August 27, 2021, 8:11:29 PM |
| 4 | February 1, 2024, 10:07:27 PM |
| 5 | February 1, 2024, 10:29:46 PM |

**Forensic significance:** Verification emails may help establish an application-registration timeline. Their presence alone does not establish that a particular individual completed each registration.

## 4. Application and Network Log Artifacts

The worksheet records the following information from the first numerically listed log entry:

| Field | Finding |
|---|---|
| Timestamp | July 9, 2024, 6:30:01 PM UTC |
| Source | `iphoneNetworkDataUsage` |
| WAN In | 8,218 |
| WAN Out | 3,514 |

**Forensic significance:** Network-usage records can provide additional context about application-related activity. These values should not be interpreted as the contents of transmitted communications.

## 5. Wireless Network Artifacts

The examination identified wireless-network records containing SmartLife-related network names, including:

- `SmartLife-0D13`
- `SmartLife-1D90`
- `SmartLife-061D`

The worksheet also records associated BSSID and timestamp information.

**Forensic significance:** Wireless-network artifacts may support investigation of device connectivity and relationships with nearby IoT equipment. A saved or recorded network entry does not, by itself, prove that a particular person operated an IoT device.

## 6. SQLite Database Examination

Searching the database artifacts for `smartlife` returned **five databases**.

The examination included `observations.db` and its:

- `Operating Dates` table
- `Observed Domains` table

The `Observed Domains` examination included a `lastSeen` value for `amazonaws.com`. Using DCode with the **Unix: Millisecond Value** format, the worksheet records the decoded timestamp as:

**January 30, 2024, 20:50:05 UTC**

A separate search for `feit` returned **two databases**.

**Forensic significance:** Database records can provide application-specific context that may not be visible in Cellebrite Reader’s higher-level artifact categories. Decoding stored timestamps helps place records into a consistent investigative timeline.

## 7. Findings and Limitations

The iPhone X report contained SmartLife application metadata, verification emails, network-related records, and database artifacts. Together, these provide multiple sources for examining SmartLife-related activity.

This case study documents findings from an existing Cellebrite Reader report. It does not claim that the examiner personally performed the original device acquisition.

The recorded timestamps should be interpreted with attention to their displayed time zone. The lab instructions specifically caution that some timestamps may not convert automatically.

No raw mobile extraction, private communications, account credentials, or unredacted personal information are included in this public portfolio.
