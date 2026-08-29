# Vehicle Forensics: Apple CarPlay Investigation

## Overview

This repository documents my forensic examination of an Apple CarPlay ecosystem recovered during a vehicle investigation.

Modern vehicles generate and store significant amounts of digital evidence through infotainment systems, navigation platforms, telematics services, and connected mobile devices. Apple CarPlay extends the functionality of a vehicle by integrating an iPhone with the vehicle's infotainment system, enabling access to navigation, communications, media, contacts, and voice assistant services.

As a result, Apple CarPlay environments can become valuable sources of forensic evidence capable of revealing user activity, travel patterns, communication history, connected devices, and vehicle interactions.

Using a Full Filesystem Extraction associated with an Apple CarPlay environment, I conducted a structured forensic examination to identify the connected device, reconstruct vehicle activity, analyze communications, investigate Siri interactions, recover historical pairing information, and correlate all recovered evidence into a unified investigative timeline.

This repository serves as both a learning resource and a practical record of my vehicle forensic investigation workflow.

---

## Table of Contents

- Overview
- Investigation Background
- Investigation Objectives
- Evidence Provided
- Forensic Methodology
- Tools Used
- Case Studies
- Repository Structure
- Key Learning Outcomes
- Conclusion

---

# Investigation Background

As part of a vehicle forensic investigation, I was provided with a Full Filesystem Extraction associated with an Apple CarPlay environment.

The purpose of the examination was to determine how the vehicle had been used, identify the connected mobile device, reconstruct user activity, and establish whether any evidence existed that could assist in understanding events relevant to the investigation.

The evidence contained a collection of Apple CarPlay artifacts, configuration files, device metadata, communication records, navigation artifacts, and user interaction data. By examining these artifacts, I aimed to determine not only who was using the system but also how the device interacted with the vehicle environment.

The investigation was designed to answer several key questions:

- Which mobile device was connected to the vehicle?
- Who owned the device?
- What vehicle was associated with the CarPlay environment?
- Which routes were travelled?
- What communications occurred during vehicle usage?
- Was Siri used while driving?
- Were any devices removed or deleted from the system?
- Can all recovered evidence be correlated into a single timeline?

To answer these questions, I performed a structured forensic examination using multiple evidence sources recovered from the Apple CarPlay ecosystem.

---

# Investigation Objectives

The primary objectives of this investigation were to:

- Identify the connected mobile device.
- Determine device ownership.
- Identify the vehicle associated with the CarPlay environment.
- Reconstruct travel routes and location history.
- Examine communication activity.
- Investigate Siri and voice assistant interactions.
- Recover historical and deleted pairing information.
- Correlate evidence across multiple artifact sources.
- Reconstruct a timeline of events.
- Produce findings supported by forensic evidence.

---

# Evidence Provided

### Evidence Type

Apple CarPlay Full Filesystem Extraction

### Source

Apple iPhone connected to a vehicle infotainment system.

### Examination Scope

The evidence contains artifacts associated with:

- Device Identification
- Vehicle Identification
- Apple CarPlay Configuration
- Navigation History
- Route Information
- Location Data
- Communication Activity
- Contacts
- Siri Interactions
- Pairing Records
- User Preferences
- System Configuration Data

---

# Forensic Methodology

To ensure consistency and evidential integrity throughout the investigation, I followed a structured digital forensic methodology.

## Phase 1: Evidence Review

I began by reviewing the Full Filesystem Extraction to understand the available evidence and identify potential Apple CarPlay artifact locations.

## Phase 2: Artifact Identification

I identified relevant forensic artifacts stored within Apple iOS system directories, configuration files, databases, and application data.

Common artifact locations included:

```text
/System
/private
/private/var/mobile
/private/var/mobile/Library
/private/var/mobile/Library/Preferences
```

## Phase 3: Artifact Analysis

I examined Property List (plist) files, databases, configuration records, and application artifacts to recover evidential information relating to device usage, vehicle activity, and user behavior.

## Phase 4: Evidence Correlation

Recovered artifacts were correlated to establish relationships between:

- Device activity
- Vehicle activity
- User activity
- Navigation events
- Communication activity
- Siri interactions

## Phase 5: Timeline Reconstruction

I combined findings from multiple artifact sources to create a chronological reconstruction of events occurring within the Apple CarPlay environment.

## Phase 6: Documentation

All findings were documented and organized into individual case studies to demonstrate the investigative process and support reproducibility.

---

# Tools Used

| Tool | Purpose |
|--------|----------|
| Autopsy 4.22.1 | Primary forensic examination platform |
| SQLite Viewer | Database analysis |
| Manual Artifact Review | Evidence verification and correlation |

---

# Case Studies

To maintain a structured investigation workflow, I divided the examination into multiple case studies. Each case study focuses on a specific investigative objective while contributing to the overall incident reconstruction.

---

## Case Study 01: Device Identification

### Objective

Identify the mobile device connected to the Apple CarPlay environment.

### Key Questions

- What device was connected?
- Who owned the device?
- What iOS version was installed?
- What unique identifiers exist?

---

## Case Study 02: CarPlay Vehicle Profiling

### Objective

Identify the vehicle associated with the Apple CarPlay environment.

### Key Questions

- What vehicle was paired?
- What manufacturer information exists?
- What configuration data was stored?

---

## Case Study 03: Route Reconstruction

### Objective

Reconstruct travel activity using navigation and location artifacts.

### Key Questions

- Where did the vehicle travel?
- What destinations were visited?
- What routes were used?

---

## Case Study 04: Communications Correlation

### Objective

Analyze communications associated with the connected device.

### Key Questions

- Who was contacted?
- What communications occurred?
- When did the communications take place?

---

## Case Study 05: Siri and Voice Interaction

### Objective

Examine voice assistant usage and Siri activity.

### Key Questions

- Was Siri used while driving?
- What commands were issued?
- What user activity can be inferred?

---

## Case Study 06: Deleted Pairing Investigation

### Objective

Identify historical and deleted pairing records.

### Key Questions

- Were devices removed?
- What historical pairings existed?
- Can deleted relationships be reconstructed?

---

## Case Study 07: Final Incident Reconstruction

### Objective

Correlate all recovered evidence into a complete investigative narrative.

### Key Questions

- What sequence of events occurred?
- How do the artifacts relate to one another?
- What conclusions can be supported by the evidence?

---

# Key Learning Outcomes

Through this investigation, I developed practical experience in:

- Vehicle forensic investigations.
- Apple CarPlay artifact analysis.
- Mobile device attribution.
- Navigation and location analysis.
- Communication correlation.
- Siri artifact analysis.
- Historical pairing investigations.
- Timeline reconstruction.
- Evidence correlation across multiple artifact sources.
- Digital forensic documentation and reporting.

---

# Conclusion

Modern vehicle infotainment systems have evolved into valuable sources of digital evidence. Apple CarPlay environments contain artifacts capable of revealing device ownership, navigation activity, communications, voice assistant interactions, and user behavior.

Through systematic examination and evidence correlation, I was able to identify connected devices, reconstruct vehicle-related activity, analyze communications, investigate Siri usage, and develop a structured understanding of events occurring within the vehicle ecosystem.

This repository documents that investigative process through a series of practical vehicle forensic case studies focused on Apple CarPlay artifact analysis and incident reconstruction.

This case was developed by Nana Sei Anyemedu
