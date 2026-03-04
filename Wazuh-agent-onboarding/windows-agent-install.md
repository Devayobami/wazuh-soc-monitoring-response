# Windows Endpoint Onboarding

This document describes how the Windows endpoint was onboarded into the SOC platform.

## Agent deployment procedure

1. Downloaded the official Wazuh Windows agent package.
2. Installed the agent on the Windows 11 endpoint.
3. Registered the agent with the SOC manager during installation.
4. Started the Wazuh agent service.
5. Confirmed that the agent successfully connected to the manager.

## Verification

The agent status changed to "Active" in the SOC dashboard.

Verification:
Agent heartbeat and event flow were confirmed in the dashboard.
