# Technical Report: Analyzing and Detecting Darknet Threats

**Project Author:** Rishi Jayavel
**Date:** July 31, 2025
**Project Type:** Academic (BCA Information Security, BS Abdur Rahman Crescent University)

---

### 1. Project Abstract
This report outlines the development of a command-line interface (CLI) tool designed to automate scanning and identifying potential threats on Darknet websites. The tool was built using Python and Ruby to navigate the Tor network, gather intelligence, and flag malicious content.

---

### 2. Tool Development & Architecture
* **Core Technologies:** Python (for networking via `requestsocks`) and Ruby (for text processing and regex).
* **Anonymity:** All traffic was routed through the local Tor SOCKS proxy to access `.onion` addresses.
* **Functionality:** The tool scrapes a given `.onion` URL, follows links, and analyzes the text against a dictionary of keywords related to cybercrime, generating a report of suspicious findings.

---

### 3. Conclusion
The project successfully resulted in a working proof-of-concept CLI tool capable of scanning Darknet websites. It proved effective in automatically identifying high-risk keywords, significantly speeding up the initial intelligence-gathering process. The project was awarded "Best Project" in the Cybersecurity Department.
