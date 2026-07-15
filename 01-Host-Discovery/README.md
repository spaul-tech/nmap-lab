# 🔍 Host discovery (ping scanning) 
Identifies active IP addresses and devices on a network without running full port scans. Nmap achieves this by sending a combination of ARP, ICMP, TCP, and UDP probes.

## `-sn` 
 (No Port Scan): Tells Nmap to only perform host discovery. It will determine if the targets are alive but will not attempt to scan any ports.
 ```bash
 nmap -sn <target_IP>
 ```
 ---
## `-Pn`
 (No Ping / Treat All Hosts as Online): Skips the initial stage where Nmap stops scanning if a host doesn't reply to a standard ping. With this enabled, Nmap treats the targets as online and forces the evaluation of all specified discovery probes down the line.
 ```bash
  nmap -Pn <target_IP>
 ```
 ---
## `-PE`
 (ICMP Echo Request): Sends a traditional ICMP Echo packet (a standard "ping") to check for basic connectivity.
 ```bash
 nmap -PE <target_IP>
 ```
 ---
## `-PS` 
(TCP SYN Ping): Sends empty TCP packets with the SYN flag set (by default to port 80). A response (SYN/ACK or RST) proves the host is alive.  
```bash
nmap -PS <target_IP>
```
---
## `-PA`
(TCP ACK Ping): Sends empty TCP packets with the ACK flag set (by default to port 80). Since there is no active connection, the target should drop it and return a RST packet, proving it is alive.
```bash
nmap -PA <target_IP>
```
---
## `-PU`
(UDP Ping): Sends empty UDP packets. If the host is up, it will typically return an ICMP "port unreachable" error.
```bash 
nmap -PU <target_IP>
```

