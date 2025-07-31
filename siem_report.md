# Technical Report: Organizational Attack Simulation & SIEM Analysis

**Project Author:** Rishi Jayavel
**Date:** July 31, 2025
**Project Type:** Academic (MSc Cyber Security, Coventry University)

---

### 1. Executive Summary

This report details a comprehensive project undertaken to simulate a multi-stage cyber-attack against a model corporate network. The primary objectives were to establish a Command and Control (C2) channel using a beacon, deploy a ransomware payload, and evaluate the effectiveness of Splunk in detecting the entire attack chain. The simulation successfully demonstrated the detection of the initial C2 beaconing traffic, privilege escalation, and final payload deployment, providing actionable insights into modern threat hunting.

---

### 2. Project Methodology

* **Network Architecture:** A virtualized corporate environment was built using Windows and Linux machines.
* **SIEM & Logging:** Splunk Enterprise was deployed on an Ubuntu Server, ingesting logs from Universal Forwarders on all client and server machines.
* **Attack Simulation Strategy:**
    1.  **Initial Compromise & C2:** Gained initial access and established persistence using a C2 beacon to the attacker's machine.
    2.  **Privilege Escalation:** Used post-exploitation techniques to escalate to a local administrator.
    3.  **Action on Objectives:** Deployed a ransomware script via the C2 channel to simulate file encryption.

---

### 3. SIEM Analysis and Threat Detection

Over 500GB of log data was analyzed. Key detections included:
* **Detecting C2 Beaconing:** Identified periodic, suspicious outbound network traffic to the attacker's IP, which is characteristic of a C2 beacon.
* **Detecting Privilege Escalation:** Flagged the creation of new admin accounts (EventCode 4720).
* **Detecting Ransomware:** Monitored for rapid file creation/modification events with Sysmon (EventCode 11).

---

### 4. Conclusion

This project confirmed that a well-configured SIEM is highly effective at detecting sophisticated, multi-stage attacks. Correlating network beaconing data with endpoint security events was critical to identifying the full attack narrative.
