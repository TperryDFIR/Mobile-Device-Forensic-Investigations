
# iOS Forensic Investigation: Findings and Limitations

## Investigation Summary

This investigation examined an iPhone X full file system report using Cellebrite Reader, focusing on SmartLife-related artifacts and their potential value in reconstructing mobile and IoT activity.

The examination identified application metadata, registration-related emails, network records, and SQLite database artifacts.

## Key Findings

### 1. SmartLife Application Identified

The examined iPhone X report contained SmartLife application metadata, including version 5.5.4, application identifier `com.tuya.smartlife`, and listed HomeKit, Bluetooth, and Camera permissions.

The recorded purchase date was August 27, 2021, at 8:10:16 PM UTC.

These artifacts support application identification and timeline development but do not independently establish when the application was installed or last used on the examined device.

### 2. Multiple Artifact Sources Supported Correlation

The examination identified SmartLife-related wireless-network records, including:

- `SmartLife-0D13`
- `SmartLife-1D90`
- `SmartLife-061D`

The worksheet also recorded associated BSSID and timestamp information.

These artifacts provide potential leads for correlating the iPhone X evidence with IoT equipment. However, the presence of a wireless-network record does not independently establish that the iPhone connected to the network, that a particular IoT device was operated, or that a specific individual performed an action.

### 3. Email Records Provided Timeline Context

Five emails containing `smartlife` were identified. The worksheet describes these as registration-verification emails associated with different applications.

The email timestamps provide investigative leads for comparing application-registration events with other recorded activity.

### 4. Wireless Network Records Provided IoT Context

SmartLife-related wireless-network names were identified in the report.

These records may help an examiner investigate connections between the mobile device and IoT equipment, but a recorded network entry alone does not establish who operated a device.

### 5. SQLite Records Provided Additional Detail

The SQLite database examination identified SmartLife's `Cache.db` and Wyze's `observations.db` within the iPhone X forensic evidence.

The Wyze database examination included the `OperatingDates` and `Observed Domains` tables.

An `amazonaws.com` record contained a `lastSeen` value that was interpreted using DCode with the Unix: Millisecond Value format.

The completed examination worksheet recorded the decoded timestamp as January 30, 2024, at 20:50:05 UTC.

These database artifacts provide additional investigative context and potential timeline reference points. However, the records do not independently establish which application generated a particular network event or whether an IoT device was operated.

## Examination Limitations

- The investigation was conducted using an existing Cellebrite Reader report. The original mobile-device acquisition was not performed as part of this documented examination.
- Search-result counts represent matches returned by the tool, not a count of distinct user actions.
- Application metadata and verification emails do not independently prove who installed or operated an application.
- Network records do not independently establish physical presence or device ownership.
- Timestamp interpretation depends on the stored format and applicable time zone.
- The examination was limited to the artifacts and questions addressed in the lab worksheet.

## Conclusion

The iPhone X report contained multiple categories of SmartLife-related evidence that could be examined together to develop an investigative timeline.

The case demonstrates a repeatable approach to mobile forensic analysis: identify relevant artifacts, examine their underlying records, correlate findings across sources, and document the limits of the conclusions.

## Evidence Handling and Privacy

This public case study excludes raw mobile extraction data, account credentials, private communications, and unredacted personal information.

## Supporting Evidence and Documentation

The following reports and screenshots support the findings documented in this case study:

- [Evidence and Scope](Evidence-and-Scope.md)
- [Examination Methodology](Examination-Methodology.md)
- [Detailed Artifact Findings](Artifact-Findings.md)
- [SmartLife Installed Application](Screenshots/01-SmartLife-Installed-Application.png)
- [SmartLife Case-Wide Search](Screenshots/02-SmartLife-Case-Wide-Search.png)
- [SmartLife Database Search](Screenshots/03-SmartLife-Database-Search.png)
- [Wyze Observations Database](Screenshots/04-Observations-Database.png)
