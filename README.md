# Wazuh + n8n Threat Intelligence Automation

## Overview

This project demonstrates an automated SOC workflow that integrates Wazuh, n8n, VirusTotal, Gmail, and Slack to enrich security alerts and accelerate incident response.

When Wazuh detects a suspicious file through File Integrity Monitoring (FIM), the workflow automatically extracts file hashes, validates them against VirusTotal, calculates a risk level, and generates alert notifications.

## Architecture

Wazuh → n8n → VirusTotal → Gmail / Slack

## Features

* Automated file hash extraction (MD5, SHA1, SHA256)
* VirusTotal threat intelligence enrichment
* Risk-based alert classification
* Automated email incident reporting
* Slack security alert notifications
* Security workflow orchestration using n8n

## Technologies Used

* Wazuh SIEM
* n8n Automation Platform
* VirusTotal API
* Gmail Integration
* Slack Integration
* Ubuntu Linux

## Workflow Process

1. Wazuh detects a suspicious file event.
2. n8n receives the alert through a webhook.
3. File hashes are extracted from the alert.
4. VirusTotal validates the SHA256 hash.
5. Risk level is calculated based on detection results.
6. Incident summary is generated automatically.
7. Email notification is sent to analysts.
8. Slack alert is delivered to the security channel.

## Repository Structure

```text
workflow/
└── Wazuh Malicious File Detection.json
```

## Security Note

All credentials, API keys, email addresses, and sensitive information have been removed or sanitized before publication.

## Future Improvements

* ServiceNow integration
* Automated ticket creation
* IOC enrichment from multiple threat intelligence feeds
* Automated response actions
* SOAR playbook expansion

## Author

Dhruv Kachchhi
Aspiring SOC Analyst
