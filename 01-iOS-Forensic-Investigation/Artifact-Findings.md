
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

**Forensic significance:** The SmartLife application record identifies the application name, version, bundle identifier, recorded purchase date, and listed permissions within the iPhone X evidence dataset. These details may support application identification and timeline development. The recorded purchase date does not independently establish when the application was installed on the examined device or when it was last used.

## Supporting Forensic Screenshots

The following screenshots document the iPhone X portion of the completed iOS and Android IoT evidence lab, using Cellebrite Reader to examine SmartLife application artifacts.
### Figure 1: SmartLife Installed Application

![SmartLife installed application](Screenshots/01-SmartLife-Installed-Application.png)

**Figure 1.** Cellebrite Reader examination of the SmartLife application installed on the iPhone X evidence dataset.

### Figure 2: SmartLife Case-Wide Search

![SmartLife case-wide search](Screenshots/02-SmartLife-Case-Wide-Search.png)

**Figure 2.** Case-wide search identifying 1,213 results associated with SmartLife, providing leads for further examination of application and device activity.

### Figure 3: SmartLife Database Identification

![SmartLife database search](Screenshots/03-SmartLife-Database-Search.png)

**Figure 3.** Cellebrite Reader examination of the Smart Life application's `Cache.db` database within the iPhone X file-system extraction, showing database metadata and accessible tables for further artifact analysis.

**Forensic significance:** The identification of `Cache.db` provides a database-level lead for examining SmartLife application data. Its metadata and table structure can guide further analysis, but the presence of the database alone does not establish that a particular IoT device was operated or that a specific user action occurred.

### Figure 4: Observations Database Examination

![Observations database](Screenshots/04-Observations-Database.png)

**Figure 4.** Cellebrite Reader examination of the Wyze application's `observations.db` database, showing the `OperatingDates` table and associated date records recovered from the iPhone X evidence dataset.

**Forensic significance:** The `observations.db` artifact demonstrates that the iPhone X evidence contains database records associated with another smart-home application, Wyze. The visible `OperatingDates` table provides potential leads for further examination and cross-application correlation. The presence of these records alone does not establish that a particular smart-home device was operated on the listed dates.

## 2. Case-Wide Artifact Search

A case-wide search for `smartlife` returned **1,213 results**.

The worksheet identified these result categories:

- Aggregated Application Usage
- Application Usage Log
- Emails
- Installed Applications
- Log Entries
- Wireless Networks

**Forensic significance:** The 1,213 results represent case-wide search matches for `smartlife`, not 1,213 confirmed application launches or smart-home device interactions. Searching across artifact categories provides investigative leads that may be correlated with application records, communications, usage data, and network information.

## 3. Email Artifacts

The search identified **five emails** containing `smartlife`.

The completed worksheet describes these as registration-verification emails associated with different applications.

The emails are presented in the order recorded in the completed worksheet rather than chronological order.

| Email | Recorded Timestamp (UTC) |
|---|---|
| 1 | May 25, 2021, 3:08:13 AM |
| 2 | April 3, 2022, 7:33:19 PM |
| 3 | August 27, 2021, 8:11:29 PM |
| 4 | February 1, 2024, 10:07:27 PM |
| 5 | February 1, 2024, 10:29:46 PM |

**Forensic significance:** Verification emails may help establish a timeline of application-registration activity. The recorded email timestamps provide temporal reference points but do not necessarily establish when an account was created, when a message was read, or whether a registration was completed. The presence of these emails alone does not establish that a particular individual completed each registration.

## 4. Application and Network Log Artifacts

The worksheet records the following information from the first numerically listed log entry:

| Field | Finding |
|---|---|
| Timestamp | July 9, 2024, 6:30:01 PM UTC |
| Source | `iphoneNetworkDataUsage` |
| WAN In | 8,218 |
| WAN Out | 3,514 |

**Forensic significance:** The `iphoneNetworkDataUsage` record provides a timestamped network-usage artifact that may support further examination of device or application activity. The WAN In and WAN Out values should be interpreted according to the units and context established by the source artifact. These values do not reveal the contents of communications or, by themselves, prove that SmartLife transmitted data at the recorded time.

## 5. Wireless Network Artifacts

The examination identified wireless-network records containing SmartLife-related network names, including:

- `SmartLife-0D13`
- `SmartLife-1D90`
- `SmartLife-061D`

The worksheet also records associated BSSID and timestamp information.

**Forensic significance:** The SmartLife-related wireless-network records provide potential leads for correlating the iPhone X evidence with nearby IoT equipment. Associated BSSID and timestamp information may help distinguish network entries and place them in an investigative timeline. However, the presence of a wireless-network record does not, by itself, establish that the iPhone connected to the network, that a specific IoT device was operated, or that a particular individual performed an action. Those conclusions would require corroborating artifacts.

## 6. SQLite Database Examination

Searching the database artifacts for `smartlife` returned **five databases**.

The examination included `observations.db` and its:

- `OperatingDates` table
- `Observed Domains` table

The `Observed Domains` examination included a `lastSeen` value for `amazonaws.com`. Using DCode with the **Unix: Millisecond Value** format, the worksheet records the decoded timestamp as:

**January 30, 2024, 20:50:05 UTC**

A separate search for `feit` returned **two databases**.

**Forensic significance:** The database examination demonstrates how application-specific SQLite records can provide investigative context beyond Cellebrite Reader's higher-level artifact categories. The `observations.db` examination identified records associated with Wyze, while separate searches identified SmartLife- and Feit-related database results. Decoding the `lastSeen` value for `amazonaws.com` provided a timestamp that may assist with timeline development. However, a domain record or decoded timestamp does not independently establish which application generated the activity, who performed it, or whether a particular IoT device was operated.

## 7. Findings and Limitations

The iPhone X report contained SmartLife application metadata, verification emails, network-related records, and database artifacts. Together, these provide multiple sources for examining SmartLife-related activity.

This case study documents findings from an existing Cellebrite Reader report. It does not claim that the examiner personally performed the original device acquisition.

The recorded timestamps should be interpreted with attention to their displayed time zone. The lab instructions specifically caution that some timestamps may not convert automatically.

No raw mobile extraction, private communications, account credentials, or unredacted personal information are included in this public portfolio.

**Investigative conclusion:** The examination identified multiple artifact categories that could support further investigation of mobile application and IoT-related activity, including installed-application metadata, registration-related emails, wireless-network records, network-usage logs, and SQLite database entries. These artifacts provide opportunities for timeline reconstruction and cross-source correlation. The findings should be interpreted within the limits of the available extraction and should not be treated as independent proof of device operation, user attribution, or the contents of network communications.
