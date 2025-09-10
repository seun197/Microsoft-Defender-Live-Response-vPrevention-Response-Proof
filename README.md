# Microsoft Defender Live Response — Prevention & Response Proof

## 📌 Project Overview
This lab demonstrates **endpoint prevention and response** using Microsoft Defender for Endpoint (Live Response).  
The goal was to execute real SOC analyst actions on a lab VM, validate prevention controls, and prove containment/remediation capabilities.  
Positioned for **Security Engineer / SOC Analyst roles**, with evidence suitable for deliverables.

---

## 🎯 Objectives
- Verify Microsoft Defender ASR/AV prevention policies block malicious behaviours.  
- Prove analyst capability to use **Live Response** for investigation and remediation.  
- Demonstrate device containment and full incident response workflow.  
- Capture audit-ready logs (Action Center and Device Timeline).  

---

## 🔁 Response Playbook (Executed)
1. Devices → select lab PC → **Initiate Live Response session**.  
2. Commands executed:  
   ```text
   get "C:\Users\Public\demo-lr.txt"
   processes
   processes -name notepad.exe
   remediate process 7780
   remediate file C:\Users\Public\demo-lr.txt
