# Analysis Summary 

This file contains raw notes and observations gathered during packet capture and Wireshark analysis. 
It adds extra depth to the report beyond just listing protocols. 

--- 

### Capture Session Notes 

- **Interface Used** : Wi-Fi 
- **Duration** : ~2 minutes 
- **Traffic Generated** : 
    - Browsed several websites (including YouTube and example.com). 
    - Ran 'ping 8.8.8.8' to create ICMP traffic. 
    - Opened apps like chat/messaging tools to stimulate background traffic. 
    - Reconnected Wi-Fi to catch ARP and mDNS traffic. 

--- 

### Protocols Observed 

| Protocol | | Details ----------------------------------------------------- | 
| -------- | | ------------------------------------------------------------- | 
| **DNS**  | | Querying domains like example.com, cloudfront.net ----------- | 
| **HTTP** | | Cleartext GET/POST, status codes (200 OK, 301 Redirec) ------ | 
| **TCP**  | | Reliable connection setup (SYN, SYN-ACK, ACK), retransmission | 
| **UDP**  | | Light traffic, used by DNS, QUIC, mDNS ---------------------- | 
| **QUIC** | | Encrypted traffic from Google services ---------------------- | 
| **mDNS** | | Local Device discovery (Chromecast, Android local lookups) -- | 
| **ARP**  | | LAN MAC-to-IP resolution, caught via broadcast traffic ------ | 

--- 

### Unique Findings 

- QUIC protocol appeared frequently, showcasing the shift away from traditional TCP-based HTTPS. 
- Several mDNS packets were observed, likely from smart devices on the local network. 
- Found ARP requests after toggling Wi-Fi, capturing real-time LAN traffic events. 
- Observed multiple layers working together : Ethernet → IP → TCP/UDP → Application (HTTP, DNS). 

--- 

### Commands & Filters Used 

- Wireshark filters : 
    - 'dns', 'http', 'tcp', 'quic', 'mdns', 'arp' 
- Protocol Hierarchy (undr Statistics → Protocol Hierarchy) used to break down % of protocols. 
- Applied custom coloring rules to highlight QUIC and DNS packets. 

--- 

### Final Deliverables 

- Full '.pcp' capture. 
- Five protocol-specific screenshots. 
- README.md sumarizing methods and findings. 
