 Incident-Response-Mail-and-Trail-
 📡 Mail & Trail – SOC Log Analysis & Splunk Threat Hunting

 📌 Overview
This investigation involved connecting to a mail server via Telnet to recover credentials, using Splunk to analyze suspicious web traffic captured by a honeypot (Cowrie), and verifying malicious URLs using VirusTotal. The case concluded by decoding a Base64-encoded hash that served as the investigation flag.

 🔍 Key Skills Demonstrated
- Manual Telnet-based mailbox access  
- Retrieval of credentials from mail server  
- Splunk SPL query creation & log filtering  
- URL-based threat hunting  
- VirusTotal web investigation  
- Base64 hash decoding  
- Honeypot (Cowrie) log interpretation

 🛠️ Tools Used
- Telnet – Access mail server & retrieve emails  
- Splunk – Analyze logs, filter suspicious URLs  
- VirusTotal – Identify malicious links  
- Base64decode – Extract and decode embedded hash  
- Cowrie Honeypot Data – Source of malicious activity

## 🧪 Investigation Summary
- Connected to mail server using Telnet & harvested credentials  
  - Username: admin* 
  - Password: CTF_Final!
- Used SPL to filter for `pastebin.com` URLs  
- Identified malicious link:  
  `https://pastebin.com/raw/jpSBiHjC`
- Extracted Base64 hash:  
  `Q29uZ3JhdHMsIHlvdSBoYXZlIGZpbmlzaGVkIENJVF9GSU5BTCBzdWNjZXNzZnVsbHk=`
- Decoded message:  
  "Congrats, you have finished CIT_FINAL successfully"

## 🔐 MITRE ATT&CK Mapping
- TA0001 – Initial Access (Phishing / Malicious URL)  
- TA0002 – Execution**  
- TA0007 – Discovery (Log hunting) 

## 📄 Full Report  
See: [Mail & Trail Report.docx.pdf](https://github.com/user-attachments/files/23513624/Mail.Trail.Report.docx.pdf)
