# KQL Threat Hunting Queries

A collection of KQL queries for advanced threat hunting and attack detection.

## 🎯 Detection Categories

- **BYOVD Attacks**: Bring Your Own Vulnerable Driver detection
- **Persistence**: Registry, scheduled tasks, services
- **Lateral Movement**: Network and credential-based movement

## 🚀 Quick Start

1. Copy the desired KQL query from the `queries/` directory
2. Paste into your Microsoft Sentinel or Microsoft 365 Defender environment
3. Adjust time ranges and thresholds as needed for your environment

## 📋 Query Index

| Query Name | Category | MITRE Technique | Severity |
|------------|----------|-----------------|----------|
| [Defender Bypass via Vulnerable Driver](queries/byovd-attacks/defender-bypass-vulnerable-driver.kql) | BYOVD | T1562.001 | High |

## 🤝 Contributing

Feel free to submit pull requests with new queries or improvements!
