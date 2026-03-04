# Wazuh Server OVA Deployment

This document describes the operational deployment of the SOC server.

## Deployment steps

1. Imported the official Wazuh all-in-one OVA into the virtualization platform.
2. Booted the appliance and verified that the following services were running:

   - Wazuh manager service
   - File Integrity Monitoring engine
   - Vulnerability detection module
   - Web dashboard service

3. Logged into the server console and verified network configuration using standard Linux network commands.
4. Confirmed the SOC dashboard was reachable over HTTPS.
5. Confirmed API and indexing services were operational through successful dashboard login.

## Result

The SOC server was successfully deployed and ready to receive endpoint telemetry.
