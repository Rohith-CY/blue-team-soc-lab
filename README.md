# Blue Team SOC Lab: Threat Detection and Investigation

## Project Overview

This project implements a small Blue Team Security Operations Center (SOC) lab using open-source security tools. It focuses on detecting suspicious network activity, monitoring authentication events, and investigating security alerts.

## Tools Used

- **Ubuntu Linux:** Security monitoring server
- **Kali Linux:** Controlled testing machine
- **Wazuh:** Security event monitoring and investigation
- **Suricata:** Network intrusion detection system
- **Nmap:** Authorized network scanning for testing

## Implemented Detection Scenarios

1. **ICMP Detection:** Custom Suricata rule to detect ICMP traffic.
2. **TCP SYN Scan Detection:** Custom Suricata rule to detect TCP SYN scanning activity.
3. **Authentication Failure Monitoring:** Investigation of authentication-failure events in Wazuh.
4. **Alert Integration:** Forwarding Suricata events to Wazuh for centralized investigation.

## Lab Architecture

Kali Linux → Network Traffic → Suricata on Ubuntu → Wazuh → Threat Hunting and Investigation

## Project Structure

- `suricata/` — Custom Suricata detection rules
- `wazuh/` — Relevant Wazuh custom rules, if applicable
- `evidence/` — Screenshots of verified detection results
- `incident-reports/` — Investigation notes and incident reports
- `docs/` — Architecture and setup documentation

## Testing

The detection scenarios were tested in an isolated virtual lab using authorized traffic. Custom ICMP and TCP SYN scan alerts were verified in Suricata and Wazuh.

## Future Improvements

- Add more detection rules and investigation scenarios.
- Improve alert severity and correlation.
- Document incident response procedures.
- Explore automated response and additional open-source security tools.

## Disclaimer

This project is intended for educational cybersecurity practice in an authorized lab environment only.