# Blue Team SOC Lab Architecture

## 1. Overview

The lab demonstrates network threat detection and centralized security event investigation using Wazuh and Suricata across Ubuntu and Kali Linux virtual machines.

## 2. Components

- **Kali Linux:** Generates controlled network traffic for testing.
- **Ubuntu Linux:** Hosts Suricata and the Wazuh monitoring components.
- **Suricata:** Inspects network traffic and generates alerts using custom detection rules.
- **Wazuh:** Collects and displays security events for centralized investigation.
- **Windows Host:** Stores project documentation and evidence.

## 3. Detection Workflow

1. Kali generates authorized ICMP traffic or a TCP SYN scan.
2. Suricata inspects the network traffic on Ubuntu.
3. Custom Suricata rules identify matching traffic and generate alerts.
4. Suricata writes events to its EVE JSON log.
5. Wazuh collects the Suricata log events.
6. The analyst investigates the alerts in Wazuh Threat Hunting.

## 4. Custom Detection Rules

| Scenario | Suricata SID | Signature |
|---|---|---|
| ICMP traffic | 1000001 | LOCAL TEST ICMP detected |
| TCP SYN scan | 1000002 | LOCAL TEST TCP SYN scan detected |

## 5. Validation

The custom ICMP and TCP SYN detection alerts were verified in Suricata logs. The TCP SYN scan alert and ICMP event were also located in Wazuh during testing.

## 6. Limitations

- The custom rules are intended for a controlled educational lab.
- The ICMP rule detects ICMP traffic and does not, by itself, prove malicious activity.
- The TCP SYN rule is a basic detection rule and may require tuning to reduce false positives.
- Automated containment and incident response actions have not been implemented.

## 7. Future Enhancements

- Add additional detection rules.
- Improve alert correlation and severity tuning.
- Document more investigation scenarios.
- Explore automated response in a controlled environment.