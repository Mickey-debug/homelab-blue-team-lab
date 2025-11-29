# homelab-blue-team-lab

This repository documents a complete Security Operations Center (SOC) home lab environment built with multiple virtual machines configured for log collection, monitoring, analysis, and detection testing.

The goal of this project is to simulate a realistic enterprise network and demonstrate core SOC skills such as log forwarding, detection engineering, threat hunting, and Windows domain administration.

---

##  Lab Components

1. Windows Server 2022 (Active Directory)**
- Domain Controller
- DNS Server
- Group Policy Management
- Sysmon deployment via GPO
- Centralized authentication for the environment

2. Splunk Enterprise (Ubuntu Server)**
- Log collection and indexing
- Sysmon log ingestion
- Custom dashboards and saved searches
- Splunk Universal Forwarder connections

3. Windows 10 Workstation**
- Domain-joined workstation
- Sysmon installed
- Event logs forwarded to Splunk
- Simulation of user activity

4. Kali Linux**
- Adversary simulation
- Tooling for penetration testing and log generation
- Attack host for detection testing

---

##  Data Flow Overview

1. Sysmon logs are generated on Windows Server and Windows 10.  
2. Windows Event Logs are forwarded to Splunk using the Universal Forwarder.  
3. Splunk indexes the logs using Sysmon TA and custom inputs.  
4. Kali performs attacks that generate detectable log activity.  
5. Splunk dashboards visualize and analyze security events across the environment.

---
