### **These detections allows Nmap to determine what software application and specific version are running on an open port.**
---
## `-sV` 🔍 Version Detection:

This is the core flag that enables service version detection. It sends a series of probes from the nmap-service-probes database to determine the application name,
version number, product name, and operating system details.
```bash
nmap -sV <target_IP>
```
---
## `--version-intensity` 🎚️ Intensity Control:  
This flag takes a number from 0 to 9 to dictate how aggressively Nmap probes the port.
 A lower number (e.g., 2) only sends the most likely probes to save time.A higher number (e.g., 9) tries every single probe in the database,
 which is useful for heavily modified or rare services.

---
 ## `--version-light` 💡 Light Mode:
A shortcut equivalent to setting -version-intensity 2. It minimizes network traffic and speeds up the scan by only testing the most common services.
```bash
nmap -sV --version-light <target_IP>
```
---
## -`-version-all` 💥 All Probes Mode:
A shortcut equivalent to setting --version-intensity 9. It forces Nmap to try every single available probe against the open ports,
ensuring maximum accuracy at the expense of speed.
```bash
nmap -sV --version-all <target_IP>
```
