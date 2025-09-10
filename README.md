# Microsoft Defender for Endpoint : Live Response Lab  

## Overview  
This lab validates Microsoft Defender for Endpoint’s ability to deliver **preventive controls** (ASR/AV) and enable **analyst-led incident response** via Live Response.  
A controlled Windows 11 endpoint was used to simulate malicious behaviour, execute remediation commands, and capture audit-ready evidence.  

---

## Objectives  
- Confirm ASR and AV policies block unauthorised file creation, process execution, and credential access attempts.  
- Exercise Live Response to:  
  - Collect and quarantine files.  
  - Enumerate and terminate processes.  
  - Contain compromised endpoint.  
- Generate verifiable evidence in **Device Timeline** and **Action Center** to support audit and SOC workflows.  

---

## Lab Environment  
- **OS**: Windows 11 Pro (lab VM).  
- **Security Controls**: Microsoft Defender for Endpoint (onboarded, ASR rules enabled).  
- **Management**: Microsoft 365 Defender portal ([https://security.microsoft.com](https://security.microsoft.com)).  

---

## Live Response Execution  
Initiated from:  
**Assets → Devices → Lab PC → Initiate Live Response session**  

Commands executed:  

```bash
get "C:\Users\Public\demo-lr.txt"
processes
processes -name notepad.exe
remediate process 7780
remediate file C:\Users\Public\demo-lr.txt
isolate
release
