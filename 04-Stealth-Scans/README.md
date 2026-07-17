# 🥷 Nmap Scan Types

A quick-reference comparison of advanced Nmap scanning techniques. This guide covers TCP SYN stealth scans alongside inverse stealth scans (`FIN`, `Null`, and `Xmas`) used to map ports and bypass stateless firewalls.


|Scan Type| Name | Target Flags Set | Open Port Response|  Closed Port Response |
|-|-|-|-|-|
|`-sS` |SYN Stealth |SYN |SYN/ACK| RST|
|`-sF` |FIN Scan|FIN |No response |RST|
|`-sN` |Null Scan |None (0)| No response| RST|
|`-sX` |Xmas Scan|FIN, PSH, URG |No response| RST|

- -sS is the standard, fastest scan type for general use.
- -sF, -sN, and -sX are "inverse" scans used to bypass stateless firewalls.
