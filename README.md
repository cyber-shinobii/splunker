# Splunker App

## Overview
The Splunker App is a unified suite of operational dashboards designed to help Splunk administrators, engineers, and analysts monitor ingestion health, internal logs, scheduled searches, configuration changes, and system performance — all from one organized interface.

This app consolidates key visibility areas into focused, ready-to-use dashboards that simplify troubleshooting, capacity planning, and environment health checks.

## Navigation Structure
The app is organized by functional categories for easy access:

### Default
- Search – Standard search view
- Analytics Workspace, Datasets, Reports, Alerts, Dashboards – Core Splunk interfaces

### Internal Logs
- Splunk Internal Audit Tracker – Audit user activity, searches, and system-level actions
- Splunk Config Changes – Track real-time configuration changes across props, transforms, inputs, and outputs
- Watched File Activity – Monitor file ingestion behavior and tailing activity
- Splunk Queue Monitor – Observe ingestion queue sizes, utilization, and throughput health

### Troubleshooting
- Data Explorer – Quickly locate which indexes, sourcetypes, and hosts are sending data into Splunk

### Splunk Jobs
- Scheduled Jobs Tracker – View active scheduled searches, success/failure rates, and triggered alerts

### Data Ingests / Connections
- tcpout Connection Metrics – Track forwarder-to-indexer connection health and throughput
- Daily Ingest Metrics – Measure ingest volume by source, sourcetype, host, and index in MB or GB

### OS
- Linux/Unix Overview – Monitor system health using data from the Splunk Add-on for Unix and Linux

## Key Dashboards

### 1. Daily Ingest Metrics
Visualize ingestion trends by source, sourcetype, host, and index. Switch between MB and GB views, analyze total ingestion, and detect data drops or anomalies.

### 2. Splunk Config Changes
Audit and visualize configuration edits to .conf files across your Splunk environment — including app context, user, and time of change.

### 3. Splunk Queue Monitor
Inspect queue utilization and backlog trends to ensure consistent data flow from inputs to indexers.

### 4. tcpout Connection Metrics
Monitor Splunk forwarding behavior, connection statuses, throughput (KBps/MBps), and TCP group health.

### 5. Scheduled Jobs Tracker
Track saved searches, cron schedules, alert counts, and execution trends across all Splunk apps and users.

### 6. Splunk Internal Audit
Gain visibility into user actions, searches, and app-level activities for compliance and audit purposes.

### 7. Linux/Unix Overview
Monitor login activity, uptime, top processes, CPU and memory usage, and system performance metrics from Unix/Linux hosts.

### 8. Watched File Activity
Troubleshoot input delays, identify watched files, and verify real-time tailing behavior using _internal logs.

### 9. Data Explorer
Answer the question — “Where’s my data?” — by exploring index, sourcetype, and host coverage with event and time summaries.

## Requirements
- Splunk Enterprise or Splunk Cloud (v8.2+)
- Access to internal indexes (_internal, _audit, _configtracker)
- Appropriate user roles with read access to internal logs

## Installation
1. Copy the app folder into `$SPLUNK_HOME/etc/apps/`.
2. Restart Splunk:
   ```bash
   $SPLUNK_HOME/bin/splunk restart
   ```
3. Open Splunk Web and navigate to Apps → Splunker.

## Recommended Use Cases
- Troubleshooting missing or delayed data
- Auditing configuration and user activity
- Monitoring ingest performance and queue bottlenecks
- Analyzing system health for Splunk infrastructure and forwarders

## Author Notes
This app was built for Splunk engineers who need immediate insight into data flow, internal operations, and environment health — without switching between multiple tools or saved searches.