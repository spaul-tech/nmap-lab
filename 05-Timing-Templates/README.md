
## ⏳ The 6 Timing Templates (0 to 5)

|Timing| Speed| Purpose / Primary Use Case|
|-|-|-|
|`-T0` (Paranoid)|Extremely Slow|Evading Intrusion Detection Systems (IDS). It serializes scans and waits 5 minutes between sending packets.|
|`-T1` (Sneaky) |Sneaky|Very Slow|Used for IDS evasion but slightly faster than Paranoid. It waits 15 seconds between packets.|
|`-T2` (Polite)|Slow|Reduces bandwidth consumption and lowers target server stress to avoid crashing fragile devices.|
|`-T3` (Normal)|Moderate|The default Nmap timing profile. Dynamic, adaptive, and reliable for everyday network environments.|
|`-T4` (Aggressive)|Fast|Speeds up scans significantly. Best suited for reasonably fast, modern, and reliable enterprise networks.|
|`-T5` (Insane)|Extremely Fast|Speed-optimized scanning. Sacrifices accuracy and stealth; likely to drop packets or overwhelm weak targets.|

- These templates offer a simple shortcut to scale performance based on your network conditions and stealth requirements.
