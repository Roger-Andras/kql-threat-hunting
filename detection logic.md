# Detection Logic Overview

This directory includes all detection logic documentation for KQL queries designed for threat hunting. Each query category is detailed separately.

---

## Structure

For each detection category (e.g., BYOVD, Persistence, Lateral Movement), expect a dedicated section or file:

### Example: BYOVD - Defender Bypass via Vulnerable Driver
- **What it does**: Detects Kernel-level vulnerabilities abused to disable Microsoft Defender.
- **How it works**: Monitors for suspicious driver loads (e.g., `rwdrv.sys`, `capcom.sys`), correlates with Defender service/process tampering within 30 minutes, then flags suspicious activity.
- **Why it matters**: This BYOVD method bypasses tamper protection and is a strong early warning indicator of ransomware attacks.

### Future Categories
- **Persistence**: Detection of registry-run keys, scheduled tasks, or malicious service creation.
- **Lateral Movement**: Detection of unusual remote execution, pass-the-hash, or remote WMI usage.
- **Initial Access**: Phishing link clicks, malicious file downloads, or credential abuse.

---

## How to Use This Logic
1. Install the KQL query into your Microsoft Sentinel or Defender environment.
2. Configure thresholds (e.g., timeframe window, driver list) to suit your environment.
3. Review alerts and refine rules over time.
