# 🤖 NSE (Nmap Scripting Engine) scripts

### This repository provides a quick, practical reference for deploying advanced Nmap switches to automate asset discovery and security assessments.

---
💠 **These below parameters are core configuration tools that tell Nmap exactly how to interact with network services.**  

`-sC`: Runs default safe scripts 🛡️  
```bash
nmap -sC 192.168.1.1
```
---
`--script`: Activates the script scanning engine ⚙️  

`vuln`: Checks for known security vulnerabilities ⚠️  
```bash
nmap --script vuln 192.168.1.50
```
---
`http-*`: Runs all scripts targeting web servers 🌐  
```bash
nmap -p 80,443 --script "http-*" 192.168.1.100
```
---
`ftp-*`: Runs all scripts targeting file transfer services 📂  
```bash
nmap -p 21 --script "ftp-*" 192.168.1.105
```
---
`ssh-*`: Runs all scripts targeting secure shell access 🔑 
```bash
nmap -p 22 --script "ssh-*" 192.168.1.110
```
---
### Common scripts used:-  
-  🟢 `safe`: Minimizes crash risks.  
-  🗺️ `discovery`: Maps active network services.  
- ⚙️ `default`: Runs standard safe tools.  
- ⚠️ `vuln`: Checks for known vulnerabilities.
-  🔑 `auth`: Bypasses or tests authentication.
-  🔨 `brute`: Guesses passwords using brute-force.  
-  💥 `intrusive`: Risks crashing the target.
-  🎯 `exploit`: Actively exploits security flaws.
