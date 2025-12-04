## 🛡️ Overview

Cymatune LT is a privacy-focused Android application that detects fake cell towers (IMSI catchers) using a **self-learning approach**. Unlike other solutions, it builds its own local database of towers over time, requiring no external services or cloud connectivity.

### Key Highlights
- ✅ **100% Local** - No cloud sync, no external databases
- ✅ **Self-Learning** - Improves detection accuracy over time
- ✅ **Encrypted Storage** - SQLCipher AES-256 encryption
- ✅ **Native Performance** - C++ signal analysis library
- ✅ **Privacy-First** - No analytics, no tracking, no data sharing

---

## ✨ Features

### Detection Methods
- **Geographic Anomaly Detection** - Flags towers appearing in conflicting locations
- **Signal Pattern Analysis** - Native C++ analysis of RSRP, RSRQ, SINR, and Timing Advance
- **Dynamic Trust Scoring** - 0-100 trust score based on tower behavior and history
- **LAC/CID Pattern Analysis** - Detects suspicious Location Area Code patterns
- **Silent SMS Detection** - Identifies Class 0 surveillance messages

### User Interface
- **Real-Time Monitoring** - Live signal strength and tower information
- **Threat Alerts** - Instant notifications for detected anomalies
- **Historical Logs** - Complete detection event history
- **Trust Score Visualization** - Color-coded threat levels

---

## 🔬 How It Works

Cymatune LT uses a **self-learning approach**:

1. **First Detection:** When a tower is detected, its location is stored locally
2. **Subsequent Detections:** The app compares new observations with historical data
3. **Anomaly Detection:** If a tower appears >10km from its expected location, it's flagged
4. **Trust Building:** Familiar towers gain trust over time; suspicious behavior reduces it

**No External Databases:** Unlike other solutions, Cymatune LT doesn't rely on OpenCelliD, Mozilla Location Service, or any external tower database. Your data never leaves your device.

---

## 📱 Installation

### Requirements
- Android 8.0 (API 26) or higher
- Location permission (for tower positioning)
- Phone state permission (for cell tower information)
- SMS permission (optional, for silent SMS detection)

### Download
- **Beta Testing:** [Join the beta program](https://github.com/yourusername/cymatune-lt/releases)
- **Play Store:** Coming soon



## 📖 Documentation

- **[Complete Documentation](PROJECT_DOCS.md)** - Architecture, algorithms, testing
- **[Research References](ACKNOWLEDGMENTS.md)** - Academic papers and inspirations
- **[Privacy Policy](PRIVACY.md)** - Data handling and permissions

---

## 🧪 Testing Without IMSI Catcher

You can validate detection without specialized hardware:

1. **Geographic Anomaly Test:** Install on emulator (US towers) and use from a different country
2. **Trust Score Test:** Monitor familiar towers over several days
3. **Signal Analysis Test:** Walk around and observe RSRP/RSRQ changes

See [Testing Strategy](PROJECT_DOCS.md#testing-strategy) for details.

---

## 🔒 Privacy & Security

### What We Collect
- Cell tower IDs and signal strength (for detection)
- Your location (to validate tower positions)
- SMS metadata (optional, for silent SMS detection)

### What We DON'T Do
- ❌ No cloud sync or external servers
- ❌ No analytics or tracking
- ❌ No data sharing with third parties
- ❌ No external tower databases

**All data is encrypted and stored locally on your device.**

---



## 📜 License

**Cymatune LT is proprietary, closed-source software.** See the [LICENSE](LICENSE) file for details.

### Open Source Dependencies
This application uses open-source components (SQLCipher, AndroidX, Material Components) which remain under their respective licenses. See [LICENSE](LICENSE) for complete attribution.

### Code Independence & Licensing Compliance
**Comprehensive Analysis Verified:** Cymatune LT is completely independent with zero code reuse from external IMSI catcher detection projects. Our thorough comparison against 5 major repositories confirmed no GPL 3.0 license violations:

1. **snoopsnitch (GPL-3.0)** - No code reuse found
2. **Android-IMSI-Catcher-Detector (GPL-3.0)** - No code reuse found
3. **IMSI Catcher Detector (MIT)** - No code reuse found
4. **IMSI-detectore (No license)** - No code reuse found
5. **LogcatReader (MIT)** - No implementation found

**All detection algorithms, architecture, and implementations are original proprietary work.**

### Acknowledgments
- Research papers on IMSI catcher detection (see [ACKNOWLEDGMENTS.md](ACKNOWLEDGMENTS.md))
- Android telephony APIs and documentation
- SQLCipher for database encryption

---

## ⚠️ Disclaimer

Cymatune LT is a **detection tool** for educational and research purposes.

**Limitations:**
- Cannot guarantee detection of all IMSI catchers
- May produce false positives or false negatives
- Cannot prevent surveillance or block fake towers
- Effectiveness varies by device, network, and attack sophistication

**Not Tested Against:**
- Real-world IMSI catchers in controlled environments
- All attack vectors and evasion techniques
- Every cellular network configuration

**Use Responsibly:** This app is intended for personal security and privacy protection. Do not use it for illegal surveillance or unauthorized network monitoring.

This software is provided "AS IS" without warranty of any kind.

---

## 📞 Support

- **Issues:** https://github.com/sandtuskers/CymatuneLT/issues
---
