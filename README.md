# Splunk VPN Log Investigation

## Overview

This project demonstrates a hands-on investigation of VPN authentication logs using Splunk.

The objective was to analyze login activity, identify failed and successful authentication attempts, investigate activity from a specific source IP, and correlate events based on users and timestamps.

## Investigation Workflow

Raw Logs → Search → Filter → Correlate → Investigate → Identify Relevant Activity

## Tools Used

- Splunk Enterprise
- SPL (Search Processing Language)
- VPN Authentication Logs

## Investigation Performed

### 1. Source IP Investigation

Filtered VPN logs based on a specific Source IP to investigate authentication activity.

### 2. Authentication Status Analysis

Analyzed successful and failed login attempts.

### 3. User-Based Analysis

Grouped authentication activity by username to identify accounts associated with failed and successful attempts.

### 4. Time-Based Analysis

Used `timechart` to visualize authentication activity over time.

## SPL Queries

### Source IP Investigation

```spl
index=VPN_Logs Source_IP="107.14.182.38"
