### Types of scans:
---
## `-sT` 🤝 TCP Connect Scan:
This flag instructs Nmap to perform a full three-way handshake (SYN, SYN-ACK, ACK) to establish a connection with the target ports.
It is used when the user does not have raw packet privileges (like non-root users).
```bash
nmap -sT <target_IP>
```
---

## `-p-` 🌐 All Ports:
This flag tells Nmap to scan every single port from 1 to 65535.
```bash
nmap -p- <target_IP>
```
---
## `-F` ⚡ Fast Mode:
This flag restricts the scan to only the 100 most common ports, prioritizing speed over depth.
```bash
nmap -F <target_IP>
```
---
## `--top-ports` 📈 Popular Ports:
This flag restricts the scan to a user-defined number of the most frequently open ports (e.g., --top-ports 500).
```bash
nmap --top-ports <no._of_top_ports_to_scan><target_IP>
```
---
## `-p` 🎯 Specific Ports:
This flag is used to manually specify exact ports or ranges to scan (e.g., -p 22,80,443).
```bash
nmap -p <port_number> <target_IP>
```
