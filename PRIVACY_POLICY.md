# Privacy Policy for Cymatune LT

**Effective Date:** December 4, 2025  
**Developer:** SandTuskers  
**Contact:** [Your Contact Email]

## Overview

Cymatune LT is a security-focused mobile application designed to detect potentially suspicious cellular network behavior, including IMSI catchers and fake cell towers. This privacy policy explains how we handle your data.

## Data Collection and Usage

### Data We Collect

Cymatune LT collects and processes the following data **locally on your device only**:

1. **Cellular Network Information**
   - Cell tower IDs (CID, LAC, MCC, MNC)
   - Signal strength measurements (RSRP, RSRQ, SINR)
   - Network type (GSM, UMTS, LTE, 5G NR)
   - Connection state and timing information

2. **Location Data**
   - GPS coordinates for tower triangulation
   - Used exclusively to detect geographic anomalies in tower positioning
   - **Never transmitted off your device**

3. **SMS Metadata (Optional)**
   - Detection of silent SMS (Type 0) messages
   - SMS timing and patterns for paging storm detection
   - **Message content is never accessed or stored**
   - This permission is optional and can be denied
1.  **Cellular Network Information**
    -   Cell tower IDs (CID, LAC, MCC, MNC)
    -   Signal strength measurements (RSRP, RSRQ, SINR)
    -   Network type (GSM, UMTS, LTE, 5G NR)
    -   Connection state and timing information

2.  **Location Data**
    -   GPS coordinates for tower triangulation
    -   Used exclusively to detect geographic anomalies in tower positioning
    -   **Never transmitted off your device**

3.  **SMS Metadata (Optional)**
    -   Detection of silent SMS (Type 0) messages
    -   SMS timing and patterns for paging storm detection
    -   **Message content is never accessed or stored**
    -   This permission is optional and can be denied

4.  **Phone State Information**
    -   Network registration state
    -   Data connection state
    -   Used for anomaly detection only

### How This Data Is Used

All data processing occurs **entirely on your device**. The app uses this data to:

-   Analyze cellular network behavior for suspicious patterns
-   Calculate trust scores for detected cell towers
-   Provide real-time security alerts
-   Generate historical detection reports

**Important:** We (the developers) never have access to your data. All processing happens locally on your device.

### Data Storage

-   All data is stored **locally** in an **encrypted SQLCipher database** on your device
-   Database encryption uses AES-256 encryption
-   No cloud storage or remote servers are used
-   Data remains on your device and under your control

## Data Sharing

**We do NOT share, transmit, or upload any data to external servers.**

- ❌ No analytics services
- ❌ No advertising networks
- ❌ No third-party data sharing
- ❌ No cloud backups
- ✅ 100% offline operation

## Permissions Explained

### Required Permissions

1. **ACCESS_FINE_LOCATION / ACCESS_COARSE_LOCATION**
   - **Purpose:** Detect geographic anomalies in tower positioning
   - **Usage:** Calculate distances between towers and detect impossible tower movements
   - **Data:** GPS coordinates stored locally, never transmitted

2. **READ_PHONE_STATE**
   - **Purpose:** Access cellular network information
   - **Usage:** Read cell tower IDs, signal strength, and network type
   - **Data:** Network metadata only, no personal information

### Optional Permissions

3. **RECEIVE_SMS / READ_SMS**
   - **Purpose:** Detect silent SMS (Type 0) and paging storms
   - **Usage:** Monitor for IMSI catcher attack patterns
   - **Data:** SMS metadata only (timing, type), **never message content**
   - **Note:** App functions without this permission in degraded mode

4. **POST_NOTIFICATIONS (Android 13+)**
   - **Purpose:** Display security alerts for detected threats
   - **Usage:** Notify you when suspicious towers are detected
   - **Data:** No data collection, display only

5. **FOREGROUND_SERVICE**
   - **Purpose:** Continuous monitoring when app is active
   - **Usage:** Run detection service while you use the app
   - **Data:** No additional data collection

## Data Retention

- Detection data is stored indefinitely on your device
- You can clear all data at any time through the app settings
- Uninstalling the app removes all stored data

## Data Security

We implement industry-standard security measures:

- **AES-256 encryption** for all stored data (SQLCipher)
- **No network transmission** of sensitive data
- **Secure key storage** using Android Keystore
- **Permission-based access** to sensitive APIs

## Your Rights

You have complete control over your data:

- **Access:** View all detected towers in the app
- **Delete:** Clear detection history at any time
- **Export:** Export detection data to CSV (local only)
- **Control:** Revoke permissions at any time through Android settings

## Children's Privacy

Cymatune LT does not knowingly collect data from children under 13. The app is designed for security-conscious adults.

## Changes to This Policy

We may update this privacy policy from time to time. Changes will be reflected in the app and on our GitHub repository:
https://github.com/sandtuskers/CymatuneLT

## Contact Us

For questions about this privacy policy or data handling:

-   **Developer:** SandTuskers
-   **GitHub:** https://github.com/sandtuskers/CymatuneLT
-   **Email:** [Your Contact Email]

## Third-Party Libraries

Cymatune LT uses the following open-source libraries. The application itself is proprietary software.

-   **SQLCipher** - Database encryption (BSD-style license)
-   **AndroidX Libraries** - Android compatibility (Apache 2.0)
-   **Kotlin Coroutines** - Asynchronous programming (Apache 2.0)
-   **Material Components** - UI framework (Apache 2.0)

These libraries do not collect or transmit user data.

---

**Summary:** Cymatune LT is a privacy-first security tool. All data stays on your device, encrypted and under your control. We never transmit, share, or upload your data to any external servers.
