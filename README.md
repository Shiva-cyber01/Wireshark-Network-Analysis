# Wireshark-Network-Analysis

# 🦈 Wireshark Packet Analysis & Network Diagnostics Labs

Welcome to my Wireshark hands-on lab repository! This project serves as a practical portfolio demonstrating my ability to analyze live network traffic, inspect protocol flows, troubleshoot network performance issues, and detect security anomalies at the packet level.

---

## 🛠️ Skills & Technical Capabilities Demonstrated

* **Packet Inspection & Protocol Analysis:** Deep-dive analysis of TCP 3-way handshakes, DNS resolution, HTTP/HTTPS transaction flows, and ARP queries across the OSI model.
* **Advanced Display Filtering:** Utilizing targeted display filters (`ip.addr`, `tcp.flags.syn == 1`, `dns.flags.response`, `http.request.method`) to rapidly isolate specific traffic and eliminate network noise.
* **Stream Reconstruction:** Following and reassembling TCP/UDP streams to analyze application-layer data payloads and identify cleartext credential transmissions.
* **Performance & Traffic Diagnostics:** Leveraging Wireshark's I/O Graphs, Round-Trip Time (RTT) charts, and TCP Stream Graphs to identify latency, packet loss, duplicate ACKs, and retransmissions.
* **Security & Threat Detection:** Detecting network scanning (SYN sweeps, port scans), malformed packets, and suspicious traffic patterns across sample capture files.

---

## 📁 Repository Structure

```text
├── PCAP-Labs/
│   ├── Lab-01-HTTP-Credential-Analysis/
│   │   ├── README.md               # Detailed walkthrough & findings
│   │   ├── sample-capture.pcap     # Sample PCAP dataset
│   │   └── screenshots/            # Visual proof & filter results
│   ├── Lab-02-DNS-Traffic-Inspection/
│   │   ├── README.md
│   │   ├── sample-capture.pcap
│   │   └── screenshots/
│   └── Lab-03-TCP-Handshake-Troubleshooting/
│       ├── README.md
│       ├── sample-capture.pcap
│       └── screenshots/
└── README.md                       # Main Repository Overview

🧪 Featured Lab Write-Ups

 🔹 Lab 01: HTTP & Cleartext Credential Analysis
Objective: Analyze an unencrypted HTTP session to trace user activity and reconstruct plain-text transmissions.

Key Filters Used: http.request.method == "POST", tcp.port == 80

Findings: Successfully reconstructed the TCP stream to isolate a cleartext HTTP POST request, identifying submitted credentials and form parameters.

🔗 View Full Lab Documentation & Screenshots

![Wireshark Network Analysis](https://raw.githubusercontent.com/Shiva-cyber01/Demo_file/5ae0a862a791c5ebea9ca08bad8e6163d2b3b7bf/Screenshot%202026-09-06%20102221.png?token=B3WFHSEWBYOGRQRKL6I4ON3KTUZVK)
# 🔹 Lab 02: DNS Query Inspection & Anomaly Detection
Objective: Inspect DNS traffic flows to map query-response patterns and identify abnormal domain requests.

Key Filters Used: dns.flags.response == 0, dns.qry.name

Findings: Identified standard recursive DNS resolution processes, mapped requested A/AAAA records, and highlighted high-frequency lookups indicative of network scanning.

🔗 View Full Lab Documentation & Screenshots

🔹 Lab 03: TCP Handshake Analysis & Performance Diagnostics
Objective: Dissect a standard TCP 3-way handshake (SYN -> SYN-ACK -> ACK) and evaluate stream connection stability.

Key Filters Used: tcp.flags.syn == 1, tcp.analysis.retransmission

Findings: Evaluated connection setup times using RTT graphs and successfully pinpointed packet retransmissions causing transmission delays.

🔗 View Full Lab Documentation & Screenshots

🌐 Sample PCAP Data Sources
The .pcap sample files analyzed in this repository were gathered from open-source educational platforms and public diagnostic archives:

Wireshark Official Sample Captures
