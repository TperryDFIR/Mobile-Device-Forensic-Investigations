# Examination Methodology

## Examination Overview

The Android IoT examination used Cellebrite Reader to review
artifacts from the supplied Galaxy S8 Physical forensic dataset.

The objective was to identify Android applications associated with
IoT activity and document relevant application metadata and
permissions.

## Tool and Evidence Source

| Item | Description |
|---|---|
| Forensic examination tool | Cellebrite Reader |
| Dataset | Galaxy S8 Physical |
| Device | Samsung Galaxy S8 |
| Primary examination area | Installed Applications |
| Initial application of interest | ezDevice |

## Examination Procedure

### 1. Open the Android Forensic Report

The supplied Galaxy S8 Physical Reader dataset was opened using
`CellebriteReader.exe`.

The examination was conducted within the available Reader report.
The original physical extraction process was not performed as part
of this documented examination.

### 2. Examine Installed Applications

Within Cellebrite Reader, the examiner navigated to:

`Analyzed Data → Installed Applications`

The installed-application records were reviewed to locate the
application named `ezDevice`.

### 3. Record Application Metadata

The `ezDevice` application record was examined for its identifying
information.

The Lab 8 worksheet records the following findings:

| Field | Recorded result |
|---|---|
| Application | ezDevice |
| Version | 4.0.0a |
| Purchase date | April 17, 2023, 6:05:36 PM (UTC+0) |
| Identifier | Com.ezdevice |
| Permissions | Bluetooth/Network |

### 4. Interpret the Findings

Application metadata can help establish which software was
represented in the examined forensic report.

The listed Bluetooth and network permissions identify capabilities
associated with the application. They do not independently prove
that the application used those capabilities or that a particular
IoT device was operated.

## Timestamp Considerations

The lab instructions note that Cellebrite Reader timestamps may
require time-zone review. Recorded timestamps should be presented
with their displayed time-zone information and should not be
silently converted.

## Examination Limitations

This methodology documents review of the supplied Galaxy S8
forensic report. It does not establish who installed or used an
application, whether an associated IoT device was connected, or
whether any specific device command was issued.

Additional conclusions require supporting artifacts from the
available dataset.
