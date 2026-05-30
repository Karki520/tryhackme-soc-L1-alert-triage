# Task 2: Events and Alerts + L1 Role in Alert Triage

**Room:** TryHackMe - SOC L1 Alert Triage  
**Date:** 30-05-2026  
**Room Progress:** 8%

## 1. From Events to Alerts - What I Learned
Started with the basics of how alerts are actually created:

**Alert Lifecycle:**
Event → Log → SIEM/EDR → Detection Rule → Alert → Triage

**Key Points:**
1. **Event**: Anything that happens - user login, file download, process launch.
2. **Log**: System like OS, firewall, cloud provider records that event as a log.
3. **SIEM/EDR**: Tools like Splunk ES, Elastic, CrowdStrike collect millions of logs daily.
4. **Alert**: SIEM creates an alert only when logs match a suspicious pattern/rule. 
   This saves analysts from reading millions of logs manually. We just triage dozens of alerts.

**Alert Management Platforms:**
- **SIEM**: Splunk ES, Elastic - Best for alert management in SOC
- **EDR/NDR**: CrowdStrike, MS Defender - Good but SIEM is preferred for central view
- **SOAR**: Splunk SOAR, Cortex - For bigger teams to automate + aggregate alerts
- **ITSM**: Jira, TheHive - For ticket management after triage

## 2. L1 Role in Alert Triage - My Notes
SOC L1 analysts: are the first line of defense. We deal with alerts the most
SOC L2 analysts:  Receive the alerts escalated by L1 analysts and perform deeper analysis and remediation
SOC engineers:  Ensure the alerts contain enough information required for efficient alert triage
SOC manager:  Track speed and quality of alert triage to ensure that real attacks won't be missed



**Responsibilities by Role:**
- **L1 Analyst**: My role. Review alerts, decide if it's bad/good, escalate real threats to L2.
  
**My Task in Dashboard:**
Had to count total alerts and find the most recent one. 
Important learning: Always check the "Time" column sorted newest first. 
And alert names in SIEM use underscores instead of spaces.

## 3. SOC Dashboard Workflow
The dashboard has 5 main columns like a Kanban board:
1. **New**: Fresh alerts waiting for L1 to pick up
2. **In Progress**: Alert I assigned to myself for triage
3. **True Positives**: Confirmed malicious alerts after investigation  
4. **False Positives**: Benign alerts, closed as noise
5. **Archive**: Old closed alerts for records

## My Takeaway
Alerts are not random. They are SIEM's way of saying "Hey, this looks weird, check it out".
As L1, my job is to be the filter. 90% alerts are noise, but I can't miss the 10% that are real attacks.
