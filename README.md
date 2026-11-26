# ITSOLERA SOC Internship — Task 01: Wazuh Installation & FIM Monitoring

**Programme:** ITSOLERA Cybersecurity (SOC) Winter Internship 2026  
**Task:** 01 — Wazuh Installation & File Integrity Monitoring  
**Duration:** 10 days  
**Completed:** 7 January 2026  
**Prepared by:** Rahul Kumar  
**Technical supervisor:** Dr. Hafbez Ur Rehman, Founder & CEO  

## Objective

Deploy a Wazuh SIEM in a virtual lab, begin collecting real-time security logs, and configure File Integrity Monitoring (FIM) on sensitive directories. The task establishes the monitoring foundation used in the later SOC labs.

## Lab architecture

| Component | Details |
|---|---|
| Host | Windows 11 Pro (10.0.22621.4317) |
| Virtualisation | VirtualBox, bridged networking |
| Wazuh OVA | v4.14.1, running manager, indexer and dashboard |
| Wazuh manager IP | `192.168.10.17` |
| Monitored endpoint | Windows 11, `MyWindows`, `192.168.10.11` |
| Agent ID | `001` |
| FIM scope | Custom internship documentation path with file-type exclusions |

## What was done

1. Downloaded the official Wazuh v4.14.1 virtual appliance and imported it into VirtualBox.
2. Booted the appliance, verified network reachability, and accessed the Wazuh web dashboard.
3. Installed and registered the Windows agent, then confirmed its status as **Active** with logs flowing to the manager.
4. Added a custom FIM configuration for the internship documentation directory.
5. Applied exclusions for noisy file types so that meaningful file adds, changes and deletions remained visible without being buried in false positives.
6. Reviewed real-time events in the dashboard to validate alert generation and agent health.

## Key outcomes

- Operational Wazuh SIEM with manager, indexer and dashboard online.
- Windows endpoint actively reporting to the manager.
- Custom FIM policy implemented and tuned for fewer false positives.
- Central dashboard providing visibility into endpoint and file-integrity events.
- Lab ready for the firewall integration, malware detection and incident response tasks that followed.

## Repository contents

- `Rahul_Kumar_Task_01_Report.pdf` — final implementation report.
- `Rahul_Kumar_Task_01_Brief.pdf` — original task brief.
- `evidence/screenshots/` — 24 screenshots documenting the deployment, agent status and FIM configuration.
