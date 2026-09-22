# iPhone X Forensic Examination Methodology

## Examination Objective

The objective of this examination was to identify and analyze relevant artifacts within a provided iPhone X full-file-system forensic dataset.

## Evidence and Tool

| Item | Description |
|---|---|
| Evidence | iPhone X Full File System dataset |
| Primary examination tool | Cellebrite Reader |
| Timestamp interpretation tool | DCode |
| Examination type | Analysis of a provided forensic extraction |

## Examination Workflow

1. Opened the provided iPhone X full file system forensic report in Cellebrite Reader.
2. Reviewed the available artifact categories and identified the SmartLife application under installed applications.
3. Recorded the SmartLife application version, application identifier, purchase date, and listed permissions.
4. Performed a case-wide search for `smartlife` and reviewed the resulting artifact categories.
5. Examined registration-related email records and their recorded timestamps.
6. Reviewed application and network-usage log entries, including the `iphoneNetworkDataUsage` artifact.
7. Examined SmartLife-related wireless-network records and their associated network identifiers.
8. Reviewed SQLite database artifacts, including SmartLife's `Cache.db` and Wyze's `observations.db`.
9. Examined the `OperatingDates` and `Observed Domains` database tables.
10. Used DCode to interpret a Unix millisecond timestamp associated with the `amazonaws.com` domain record.
11. Documented relevant observations and selected supporting screenshots for the public forensic portfolio.

## Timestamp Considerations

Timestamps were interpreted with attention to their displayed time zones and source artifacts.

The examination included a `lastSeen` timestamp associated with an `amazonaws.com` record in the `Observed Domains` table. DCode was used with the Unix: Millisecond Value format to interpret the recorded timestamp.

The completed examination worksheet records the decoded timestamp as January 30, 2024, 20:50:05 UTC.

Timestamp interpretation was limited to the information available in the provided forensic report. A timestamp alone does not establish which individual performed an action or whether a particular IoT device was operated.

## Reporting Approach

The investigation documents artifacts directly observed in the provided forensic report and distinguishes those observations from their potential forensic significance.

Findings are organized by artifact category and supported by examination notes, recorded values, and selected Cellebrite Reader screenshots.

The public portfolio excludes the original forensic extraction, account credentials, private communications, and unredacted personal information.

The investigation does not claim that the examiner performed the original physical acquisition of the iPhone X.

## Examination Limitations

This case study examines an existing forensic extraction. It does not claim that a new physical acquisition of the iPhone X was performed.
