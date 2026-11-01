**Incident handler's journal**

**Instructions**

As you continue through this course, you may use this template to record your findings after completing an activity or to take notes on what you've learned about a specific tool or concept. You can also use this journal as a way to log the key takeaways about the different cybersecurity tools or concepts you encounter in this course.

| Date: 14/10/2026 | Entry: 2026-001 |
| :--- | :--- |
| Description | Business operations severely disrupted by ransomware. The cause of the security incident was a phishing email that contained a malicious attachment: once it was downloaded, ransomware was deployed encrypting the organization's computer files. |
| Tool(s) used | None |
| The 5 W's | **Who**? An organized group of unethical hackers. **What**? A ransomware security incident. The ransomware encrypted organization’s computer files. **When**? Tuesday 9:00a.m **Where**? In a small U.S. health care clinic. **Why**? Hackers accessed the company's network by using targeted phishing emails, which were sent to several employees of the company. The phishing emails contained a malicious attachment that installed ransomware on the employee's computer once it was downloaded. |
| Additional notes | How could the clinic prevent incidents like this? Training about dangers of phishing mail and backups? Should the clinic pay for the ransom and decrypt data? |

* * *

| Date: 16/10/2026. | Entry: 2026-002 (Activity: Investigate a suspicious file hash + Activity: Use a playbook to respond to a phishing incident) |
| :--- | :--- |
| Description | An employee received a malware excel via email. |
| Tool(s) used | virustotal.com : to check the malware hash |
| The 5 W's | **Who**? Hacker with IP 114.114.114.114 **What**? Multiple unauthorized executable files are created on an employee's computer **When**? Between 1:11 and 1:20 pm. **Where**? In a financial services company. **Why**? An employee received an email containing an attachment, a password-protected spreadsheet file |
| Additional notes | **SHA256 file hash:** 54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b |

* * *


| Date: 17/10/2026 | Entry: 2026-03 (Activity: Review a final report) |
| :--- | :--- |
| Description | Data breach: an individual gained unauthorized access to approx 50,000 customer PII and financial information. |
| Tool(s) used | Web application access log Incident final report |
| The 5 W's | **Who** caused the incident? An individual **What** happened? The attacker accessed customer purchase confirmation pages, exposing data (PII and financial). **When** did the incident occur? At approx. 3:31 on Dec 22/2022 **Where** did the incident happen? At a mid-sized retail company **Why** did the incident happen? There was a vulnerability in the e-commerce web app that allowed access to customer transaction data. |
| Additional notes | Another recommendation: activate alerts in order to detect exceptionally high volumes of data in logs. |

* * *

| Date: 18/10/2026 | Entry: 2026-04 (Activity: Analyze your first packet) |
| :--- | :--- |
| Description | In this activity I learned how to use Wireshark to analyze a packet capture (pcap) file. |
| Tool(s) used | Wireshark |
| The 5 W's |     |
| Additional notes | Filter by IP: `ip.addr == 142.250.1.139` |
|     | Filter by IP source: i`p.src == 142.250.1.139` |
|     | Filter by Ethernet MAC address: `eth.addr == 42:01:ac:15:e0:02` |
|     | Filter DNS packet: `udp.port == 53` (DNS traffic uses UDP port 53) |
|     | Filter to select TCP port 80 traffic: `tcp.port == 80` |
|     | Filter to select TCP packet data that contains specific text data: `tcp contains "curl"` |

* * *

| Date: 18/10/2026 | Entry: 2026-05 (Activity: Explore signatures and logs with Suricata) |
| :--- | :--- |
| Description | Explore signatures with Suricata |
| Tool(s) used | Suricata (IDS) |
| The 5 W's |     |
| Additional notes | Rules: action header options `Action: alert, drop, pass, reject` `Header: protocol source (ip+port) -> destination (ip+port)` `Options: (msg: …; flow: …, content: …, sid:12345; rev:1)` |
|     | `sudo suricata -r sample.pcap -S custom.rules -k none` → triggers rules in suricata |
|     | /var/log/suricata contains fast.log and eve.json |

### Need another journal entry template?
| Date: Record the date of the journal entry. | Entry: Record the journal entry number. |
| :--- | :--- |
| Description | Provide a brief description about the journal entry. |
| Tool(s) used | List any cybersecurity tools that were used. |
| The 5 W's | Capture the 5 W's of an incident. **Who** caused the incident? **What** happened? **When** did the incident occur? **Where** did the incident happen? **Why** did the incident happen? |
| Additional notes | Include any additional thoughts, questions, or findings. |

* * *


If you want to add more journal entries, please copy one of the tables above and paste it into the template to use for future entries.

