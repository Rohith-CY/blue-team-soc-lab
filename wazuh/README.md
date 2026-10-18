# Wazuh Configuration

Wazuh is used as the centralized security monitoring and investigation platform in this project.

## Integration

- Collects Suricata EVE JSON events.
- Displays detected network activity in Wazuh Threat Hunting.
- Supports investigation of authentication-failure events.
- Suricata custom detection alerts were verified in Wazuh.

## Custom Rules

The project currently documents custom Suricata rules. Custom Wazuh detection rules will be added here if implemented and tested.

## Security Note

Sensitive credentials and complete machine-specific configuration files are intentionally excluded from this repository.