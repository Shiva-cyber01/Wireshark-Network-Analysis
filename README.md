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

```

---

## 🧪 Featured Lab Write-Ups

### 🔹 Lab 01: HTTP & Cleartext Credential Analysis

* **Objective:** Analyze an unencrypted HTTP session to trace user activity and reconstruct plain-text transmissions.
* **Key Filters Used:** `http.request.method == "POST"`, `tcp.port == 80`
* **Findings:** Successfully reconstructed the TCP stream to isolate a cleartext HTTP POST request, identifying submitted credentials and form parameters.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a7cde2fa-fc21-43b1-ad86-72cce59d434a" />

---

### 🔹 Lab 02: DNS Query Inspection & Anomaly Detection

* **Objective:** Inspect DNS traffic flows to map query-response patterns and identify abnormal domain requests.
* **Key Filters Used:** `dns.flags.response == 0`, `dns.qry.name`
* **Findings:** Identified standard recursive DNS resolution processes, mapped requested A/AAAA records, and highlighted high-frequency lookups indicative of network scanning.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/93199a22-ce4d-4c67-91fc-265e397b47dd" />

---

### 🔹 Lab 03: TCP Handshake Analysis & Performance Diagnostics

* **Objective:** Dissect a standard TCP 3-way handshake (`SYN` -> `SYN-ACK` -> `ACK`) and evaluate stream connection stability.
* **Key Filters Used:** `tcp.flags.syn == 1`, `tcp.analysis.retransmission`
* **Findings:** Evaluated connection setup times using RTT graphs and successfully pinpointed packet retransmissions causing transmission delays.
* **🔗 [View Full Lab Documentation & Screenshots**](https://www.google.com/search?q=./PCAP-Labs/Lab-03-TCP-Handshake-Troubleshooting/)

---

## 🌐 Sample PCAP Data Sources

The `.pcap` sample files analyzed in this repository were gathered from open-source educational platforms and public diagnostic archives:

* [Wireshark Official Sample Captures](https://www.google.com/search?q=https://wiki.wireshark.org/SampleCaptures)
* [Malware-Traffic-Analysis.net](https://www.google.com/search?q=https://www.malware-traffic-analysis.net/)
* Custom lab environments (TryHackMe / Hack The Box)

---

## 💼 Let's Connect!

I am actively seeking opportunities in **Cybersecurity, SOC Analysis, and Network Security Engineering**.

* **LinkedIn:** [linkedin.com/in/your-profile](https://www.google.com/search?q=https://www.linkedin.com/in/your-profile)
* **Email:** `your.email@example.com`

```

```
