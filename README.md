## Wazuh-based SOC monitoring, detection and response lab for Windows endpoint on VMware


## Project Overview
This project demonstrates hands-on experience deploying and operating a small-scale Security Operations Center using Wazuh in a virtualized lab built on VMware, with a monitored Windows endpoint.

The lab focuses on practical SOC operations rather than tool installation only. It includes centralized log and telemetry collection, real-time alerting, vulnerability detection, file integrity monitoring, and configuration/compliance checks. An analyst workflow is implemented covering alert triage, investigation, and response decision-making.

A real investigation case is documented, where a vulnerable application (7-Zip) was detected through automated vulnerability monitoring, assessed for impact, and mapped to remediation actions. The project also includes deployment runbooks, endpoint onboarding procedures, detection capability documentation, and a validation checklist.

## Key competencies demonstrated

- SOC platform deployment and validation
- Windows endpoint onboarding and telemetry ingestion
- Alert triage and investigation workflow
- Vulnerability analysis and remediation planning
- File integrity and configuration monitoring
- Clear analyst-style documentation suitable for operational SOC environments

---
## Architecture

**SOC Platform**

- Wazuh all-in-one server deployed from official OVA
- Web-based dashboard for monitoring and investigation
- Integrated manager, indexing, and API services

**Endpoint**

- Windows 11 Enterprise workstation
- Wazuh agent installed and registered to the manager

**High-level flow**

1. Endpoint telemetry ingestion
2. Event normalization and correlation
3. Alert generation
4. Analyst triage and investigation
5. Response and remediation decision

---

## Validation Checklist

- Wazuh server reachable on network
- Dashboard accessible and operational
- Windows agent authenticated and active
- Alerts successfully generated and processed
- Endpoint telemetry visible in dashboard
- Vulnerability and configuration modules enabled

---
## Why this project matters

This lab demonstrates end-to-end SOC operations including:

- monitoring
- detection
- triage
- investigation
- vulnerability assessment
- security validation
