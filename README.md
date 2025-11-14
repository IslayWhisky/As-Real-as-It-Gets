## README: Observation Data and Analysis Results
This repository is published to ensure the reproducibility and transparency of the research paper:
"As Real as It Gets: Long-Term Observations of Vulnerable IoT Devices Continuously Exposed to the Internet".
This repository contains the primary datasets collected and analyzed during June 2023 to January 2024 using 12 phsical IoT devices.

## Repository Structure
This repository is primarily structured with top-level summary files for quick threat intelligence reference and the main data directory containing the detailed daily observation records.
```
.
├── README.md                 <-- This file
├── cncserverlist             <-- List of C&C Servers
├── downloadserverlist        <-- List of Malware Download Servers
├── loaderlist                <-- List of Loaders
├── malwarelist               <-- List of IoT Malware Binaries and Scripts
├── observationlist           <-- List of Observation Periods
└── data/                     <-- All categories of daily observation data
    ├── session/              <-- E.g., Session-level data
    │   ├── .json_YYYYMMDD    <-- Daily data with prefix/suffix pattern
    │   └── ...
    ├── steps/                <-- E.g., Step-level data
    │   ├── .json_YYYYMMDD    
    │   └── ...
    ├── step1_login/   <-- E.g., Success login attempts
    │   ├── .json_YYYYMMDD    
    │   └── ...
    ├── ...                   <-- (Other specific step directories)
    └── step5_cnc/            <-- E.g., Communication with C2 servers
        ├── .json_YYYYMMDD   
        └── ...
```

## Details of Key Files and Directories
1. Summary Files (Top Level)
   
These files provide aggregated lists for rapid threat intelligence lookup and are located in the repository's root directory.

| Filename | Content | Format/Schema |
| :--- | :--- | :--- |
| `cncserverlist` | A list of observed **Command and Control (C2)** server endpoints. | `IP address/domain name:port` |
| `downloadserverlist` | A list of observed **Malware Download Server** IP addresses. | `IP address` |
| `loaderlist` | A list of file hashes or details for **Loader** malware components. | `IP address` (Source/Observed location) |
| `malwarelist`| A list of **IoT Malware Binaries and Scripts** identified by their **SHA256 hash**. | `SHA256 hash` |
| `observationlist`| Details regarding the **observation periods**. | `case ID, device, start day, end day, # of days` |

2. The data Directory
   
The data directory contains the detailed daily records collected from the long-term observation experiment.
 It is structured into multiple subdirectories representing different stages or types of observed activity.

| Directory | Description | Data Filename Convention |
| :--- | :--- | :--- |
| `session/` | Data aggregated at the **session level**. | `.json_YYYYMMDD` |
| `steps/` | Device compromise result at the **six common steps**. | `.json_YYYYMMDD` |
| `step1_logins/`| Specific data related to **login success**. | `.json_YYYYMMDD` |
| `step2_download/` | Specific data related to **download attempt**. | `.json_YYYYMMDD` |
| `step3_delivery/` | Specific data related to **malware delivery**. | `.json_YYYYMMDD` |
| `step4_execution/` | Specific data related to **process execution**. | `.json_YYYYMMDD` |
| `step5_cnc/` | Specific data related to **cnc connection**. | `.json_YYYYMMDD` |

## Notes
This repository does not directly contain malicious executable files (malware binaries). Instead, we provide associated hash values (e.g., in malwarelist) to ensure research reproducibility while eliminating direct security risks associated with distributing live malware.

The IP address information included in this repository was collected strictly for the purpose of identifying attacker infrastructure (C2 and download servers). 
It does not contain any local network information or Personally Identifiable Information (PII).

Upon acceptance, the full dataset (including malware binaries) will be released and made available for request via our project website to any interested researcher.
