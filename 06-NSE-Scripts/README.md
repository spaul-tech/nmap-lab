# 🤖 NSE (Nmap Scripting Engine) scripts

### The Nmap Scripting Engine (NSE) is one of Nmap's most powerful features, allowing users to automate networking and security tasks using scripts written in the Lua programming language
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
  
---
# **🗃️ script.db**
**To manage its massive library of automation scripts, Nmap relies on a centralized database called script.db. This index file tells Nmap exactly which scripts to run without wasting time reading every file manually.Below is a breakdown of the most common NSE scripts used by security professionals in the field.**  
- All the scripts are stored inside a directory in  `/usr/share/nmap/scripts/script.db`.
- It Keeps track of which scripts belong to `vuln`, `safe`, `discovery`, etc.
- If you download or write a custom NSE script, you must run `nmap --script-updatedb` to refresh this file.  


## 💠 Here are the most frequently used NSE scripts across major network protocols:  
🌐 Web Services (HTTP / HTTPS)  
`http-enum`: Enumerates common web directories, administrative panels, and login pages.  
`http-title`: Grabs the HTML title tag of a website to quickly identify its purpose.  
`http-methods`: Checks which HTTP methods (GET, POST, PUT, DELETE) are enabled on the server.  
`ssl-cert`: Inspects SSL/TLS certificates to find expiration dates and common names. 

---
📂 File Sharing & Directory Services (SMB)  
`smb-os-discovery`: Determines the exact Windows OS version and computer name over SMB.  
`smb-vuln-ms17-010`: Checks if the target is vulnerable to EternalBlue.  
`smb-enum-shares`: Lists open and hidden network shares on a target machine.  

---

 🖥️ Remote Access (SSH)  
 `ssh-auth-methods`: Lists the authentication methods (password, public key) allowed by an SSH server.

 ---

🔓 Vulnerability & Brute Force  
`ssh-brute`: Performs targeted dictionary password attacks against SSH logins.








