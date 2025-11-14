README: Observation Data and Analysis Results

This repository is published to ensure the reproducibility and transparency of the research paper:
"As Real as It Gets: Long-Term Observations of Vulnerable IoT Devices Continuously Exposed to the Internet".
This repository contains the primary datasets collected and analyzed during June 2023 to January 2024 using 12 phsical IoT devices.

Repository Structure
This repository is primarily structured with top-level summary files for quick reference and the main data directory containing the daily observation records.
.
├── README.md                 <-- This file
├── cncserverlist             <-- List of C&C Servers (IP address/domain name: port)
├── downloadserverlist        <-- List of Malware Download Servers (IP address)
├── loaderlist                <-- List of Loaders (IP address)
├── malwarelist               <-- List of IoT Malware Binaries and Scripts (SHA256 hash)
├── observationperiodlist     <-- List of observation periods (case ID, device, start day, end day, # of days)
└── data/                     <-- All categories of daily observation data
    ├── session/
    │   ├── .json_YYYYMMDD
    │   └── ...
    ├── steps/
    │   ├── .json_YYYYMMDD
    │   └── ...
    ├── step1_loginsuccess/
    │   ├── .json_YYYYMMDD
    │   └── ...
    ├── ...
    └── step5_cnc/
        ├── YYYY-MM-DD.json
        └── ...

Malware Binary Disclosure
This repository does not directly contain malicious executable files (malware binaries). Instead, we provide associated hash values (e.g., in malwarelist) to ensure research reproducibility while eliminating direct security risks associated with distributing live malware.

IP Address Disclosure
The IP address information included in this repository was collected strictly for the purpose of identifying attacker infrastructure (C2 and download servers). 
It does not contain any local network information or Personally Identifiable Information (PII).

Data directory
The data directory contains the detailed daily records collected from the long-term observation experiment.
The data/ directory is organized into seven subdirectories, each corresponding to a specific data collection category.
Each subdirectory contains data files partitioned by day in JSON format where files follow the format *.json_YYYYMMDD.
All files are in JSON format. Please refer to the first file in any given category for the exact data schema.

Contact Information
Upon acceptance, the full dataset (including malware binaries) will be released and made available for request via our project website to any interested researcher.
