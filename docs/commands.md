# Blue Team SOC Lab — Useful Commands

## 1. Check Security Services

```bash
sudo systemctl is-active wazuh-manager
sudo systemctl is-active suricata
sudo systemctl is-active wazuh-agent
```

## 2. Validate Suricata Configuration

```bash
sudo suricata -T -c /etc/suricata/suricata.yaml -v
```

## 3. Generate ICMP Traffic from Kali

```bash
ping -c 4 192.168.56.107
```

## 4. Perform a Controlled TCP SYN Scan

```bash
sudo nmap -sS -Pn -p 1-30 192.168.56.107
```

## 5. Verify Suricata Alerts on Ubuntu

```bash
sudo tail -n 100 /var/log/suricata/eve.json | grep "LOCAL TEST TCP SYN scan detected"
```

For ICMP alerts:

```bash
sudo tail -n 100 /var/log/suricata/eve.json | grep "LOCAL TEST ICMP detected"
```

## 6. Inspect Wazuh Archived Events

```bash
sudo grep 'LOCAL TEST ICMP detected' /var/ossec/logs/archives/archives.json | tail -n 5
```

## Note

Run network tests only against systems you own or are authorized to test. These commands reflect the lab configuration and IP addresses used during testing.