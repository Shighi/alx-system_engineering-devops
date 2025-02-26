# Webstack Monitoring with Datadog

## Overview
This project involves setting up monitoring for a web server using Datadog. Tasks include installing the Datadog agent, monitoring system metrics, and creating a dashboard.

## Tasks

### 0. Sign Up for Datadog and Install `datadog-agent`
1. Sign up for a free Datadog account on the **US1 region**: [Datadog US](https://app.datadoghq.com)
2. Install the `datadog-agent` on **web-01** by following the instructions on the Datadog website.
3. Create an **application key** in Datadog.
4. Copy and paste your **Datadog API key** and **application key** into your Intranet user profile.
5. Ensure that your **web-01** server appears in Datadog under the hostname `XX-web-01`.
6. Validate using the Datadog API.

### 1. Monitor Some Metrics
1. Set up a monitor to track **read requests per second** on the device.
2. Set up a monitor to track **write requests per second** on the device.

### 2. Create a Dashboard
1. Create a new dashboard in Datadog.
2. Add at least **four widgets** to display various system metrics.
3. Save the dashboard ID in a file named `2-setup_datadog`.
4. Use the Datadog API if needed to retrieve the dashboard ID.

## Repository Structure
```
├── alx-system_engineering-devops
│   ├── 0x18-webstack_monitoring
│   │   ├── 2-setup_datadog
│   │   ├── README.md  (this file)
```

## Resources
- [Datadog Documentation](https://docs.datadoghq.com/)
- [System Check Metrics](https://docs.datadoghq.com/integrations/system/)
- [Datadog API](https://docs.datadoghq.com/api/)


