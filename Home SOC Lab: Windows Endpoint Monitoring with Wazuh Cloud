# Home SOC Lab: Windows Endpoint Monitoring with Wazuh Cloud

## Project Overview

I built a beginner SOC lab using **Wazuh Cloud** and a **Windows endpoint agent** to practice security monitoring, alert review, and basic incident triage.

The Windows agent was installed on my lab computer and connected to Wazuh Cloud, allowing system logs and security events to be collected in a centralized dashboard.

The goal of this project was to understand how a SIEM collects endpoint activity, how alerts are categorized by severity, and how a SOC analyst investigates whether an event is normal system behavior or potentially suspicious.

---

## Tools Used

- Wazuh Cloud
- Wazuh Agent for Windows
- Windows PowerShell
- Windows Event Logs
- Service Control Manager Logs

---

## What I Did

I deployed a Wazuh agent on a Windows endpoint and confirmed that the agent became active in the Wazuh Cloud dashboard.

After connecting the endpoint, I reviewed generated alerts, checked severity levels, expanded event details, and analyzed Windows log data to understand what happened on the system.

---

## Alert Investigation Example

### Alert: Service Startup Type Was Changed

| Field | Details |
|---|---|
| Alert | Service startup type was changed |
| Severity | Low |
| Wazuh Rule Level | 3 |
| Agent | WindowsAgentGy |
| Computer | DESKTOP-4P21QD4 |
| Event ID | 7040 |
| Source | Windows Service Control Manager |
| Service | Background Intelligent Transfer Service |
| Service Name | BITS |

---

## What Happened

Wazuh detected that the startup type of the **Background Intelligent Transfer Service**, also known as **BITS**, changed from **demand start** to **auto start**.

This means the service was changed from starting only when needed to starting automatically when Windows starts.

---

## Why It Matters

Service startup changes are important in security monitoring because attackers can sometimes modify services to maintain persistence or make malicious programs start automatically.

In this case, **BITS** is a legitimate Windows service commonly used for Windows updates and background downloads, so the event appears to be low risk by itself.

---

## Initial Assessment

This alert was classified as **low severity** because the Wazuh rule level was **3** and the Windows event severity was listed as **Information**.

Based on the event details, this appears likely related to normal Windows activity or system updates unless other suspicious events occurred around the same time.

---

## Recommended Action

I would review surrounding events in Wazuh to confirm whether Windows updates or other software changes happened around the same time.

I would also continue monitoring for repeated service changes, suspicious PowerShell activity, new services being created, or high-severity alerts from the same endpoint.

---

## Skills Practiced

- Security monitoring
- SIEM dashboard navigation
- Endpoint log collection
- Windows Event Log analysis
- Alert severity review
- Basic SOC triage
- Incident documentation
- Identifying normal vs suspicious system behavior

---

## Portfolio Summary

Built a home SOC lab using **Wazuh Cloud** and a **Windows endpoint agent** to monitor system activity, review security alerts, and practice SOC triage.

Investigated a Windows Service Control Manager alert where the **Background Intelligent Transfer Service** startup type changed from **demand start** to **auto start**.

Documented the event, reviewed severity, assessed risk, and recommended follow-up actions based on surrounding logs.

---

## Key Takeaway

This project helped me understand how endpoint agents send logs to a SIEM, how alerts are generated, and how a SOC analyst reviews event details to decide whether an alert is normal activity or something that requires further investigation.
