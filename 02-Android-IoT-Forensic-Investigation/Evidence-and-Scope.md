# Evidence and Scope

## Case Overview

This case study documents an examination of Android IoT-related
artifacts from a Samsung Galaxy S8 forensic dataset.

The examination was conducted as part of Lab 8: iOS & Android IoT
Evidence, with supporting Android forensic work documented in
Lab 7: Android Forensics and Artifacts.

## Evidence Source

| Field | Description |
|---|---|
| Device | Samsung Galaxy S8 |
| Dataset | Galaxy S8 Physical |
| Examination tool | Cellebrite Reader |
| Evidence type | Existing Android forensic extraction/report |
| Investigation focus | Android application and IoT-related artifacts |

The provided dataset was examined using Cellebrite Reader. This
portfolio documents examination of the available forensic evidence;
it does not claim that the examiner personally performed the
original physical acquisition.

## Examination Scope

The Android IoT examination focuses on:

- Identifying installed applications relevant to IoT activity.
- Examining application metadata, including version and identifier.
- Reviewing application permissions.
- Examining additional Android artifacts identified in the
  assigned forensic exercises.
- Correlating relevant findings where supported by the evidence.
- Documenting investigative limitations.

## Initial Application of Interest

The Lab 8 Android IoT examination identifies `ezDevice` as an
application of interest in the Galaxy S8 dataset.

The recorded application metadata includes:

| Field | Recorded finding |
|---|---|
| Application | ezDevice |
| Version | 4.0.0a |
| Identifier | Com.ezdevice |
| Permissions | Bluetooth/Network |

These entries establish an initial examination target. Application
presence and permissions alone do not prove that a particular IoT
device was connected to or operated from the phone.

## Evidence Handling and Limitations

The examination is based on the supplied forensic dataset and the
artifacts accessible through Cellebrite Reader. Findings will be
reported according to what the available evidence supports.

Original extraction files, credentials, private communications,
and unredacted personal information will not be published in
this public portfolio.
