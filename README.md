# Task 5 : Capture and Analyze Network Traffic Using Wireshark 

### Overview 

This respository contains a hands-on network traffic analysis perfomed using Wireshark. 
I captured real network packets, explored diverse protocols, and documented detailed findings, including screenshots and raw notes. 

--- 

### Tools Used 

- **Wireshark** (GUI-based analysis)
- **Windows 10** (host machine)
- **VS Code** (for writing this report)
- **Ping/Curl Commands** (to generate intentonal traffic)

--- 

### Project Structure 
    CyberSecurity-TASK-5 
        - network_capture.pcap 
        - screenshots 
            - screenshot_dns.png 
            - screenshot_http.png 
            - screenshot_tcp.png 
            - screenshot_udp.png 
            - screenshot_quic.png 
        - analysis_summary.md 
        - README.md 

--- 

### Protocols Identified 

| Protocols | | Description --------------------------------------------------------------- |
| --------- | | --------------------------------------------------------------------------- | 
| **DNS**   | | Resolving domain names to IPs (example.com, cloudfront.net) --------------- | 
| **HTTP**  | | Web requests and responses (GET, POST, status codes) ---------------------- | 
| **TCP**   | | Connection setup (SYN, ACK), reliable data delivery ----------------------- | 
| **UDP**   | | Lightweight, connectionless transport for fast traffic -------------------- | 
| **QUIC**  | | Modern encrypted transport replacing TCP for speed (seen on Google traffic) | 
| **mDNS**  | | Local device discovery (Chorecast, Android local) ------------------------- | 
| **ARP**   | | LAN layer address resolution (MAC-to-IP mapping) -------------------------- |

--- 

### Screenshots 

All key protocol snapshots are stored in the 'screenshots/' folder : 
    - DNS queries and responses. 
    - HTTP web transactions. 
    - TCP session handshakes. 
    - UDP-based Qu=UIC encrypted streams. 
    - Local mDNS and ARP traffic. 

--- 

### Unique Insights 

- **QUIC Detection** : Found modern UDP-based encryted traffic, showing real-world trends in faster web communication. 
- **LAN Discovery** : Detected mDNS and ARP packets revealing smart device interactions on the local network. 
- **Layered Traffic** : Saw a mix of IPv4, IPv6, TCP, UDP, and application-layer protocols - showcasing the full stack in action. 

--- 

### Deliverables 

- 'network_capture.pcap' - complete capture file 
- 'screenshots/' - organized by protocol 
- 'analysis_summary.md' - raw notes and detailed bullet points 
- 'README.md' - this report 

--- 