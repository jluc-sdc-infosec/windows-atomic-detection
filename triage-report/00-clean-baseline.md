## Windows Machine  VM endpoint (Agent Window-Watcher)

**Base Line**
Windows 10 Enterprise LTSC 2021 Configuration
(Default out of the Box)

### System Inventory
4 Cores
6GB Memory
CPU AMD Ryzen 5 5600x 6-Core Processor

### Network
IPv4 Address: 192.168.122.10 Static
Default Gateway: 192.168.122.1
Tailscale IP: 100.xx.xx.xx
Wazuh: 100.xx.xx.xx
Active Private Network : Tailscale

<img width="906" height="306" alt="2026-11-21-195847_hyprshot" src="https://github.com/user-attachments/assets/b637530b-a270-4375-b598-f5d7064d13de" />

### Vulnerability:
1199 Total- Fresh install
  -  925 on Microsoft Windows 10 Enterpise LTSC 2021 10.0.19044.7725
  -   274 on Microsoft Edge
- 47 Critical
  
- 783 High
  
- 361 Medium
  
- 8 low
     

### Inventory: 38
### Windows Registry: 5921  > 6290 (initial baseline crawl)

<img width="911" height="354" alt="2026-11-21-195913_hyprshot" src="https://github.com/user-attachments/assets/eb5e83c3-de59-421e-8e25-bb900b19251c" />

<img width="1884" height="576" alt="2026-11-21-234737_hyprshot" src="https://github.com/user-attachments/assets/7ebe7295-e512-46bb-a420-b6acf192ac23" />

### Destination Ports
- 443 - https
- 80 - http
- 1514 - wazuh agent (sending logs through tailscale)

### Source Ports
- 135 - rpc
- 137- netbios service
- 138 - netbios datagram service
- 139 - netbios session service
- 445 - microsoft - DS (Direct SMB)

### Software (Unique Packages)
Package Name
	- Microsoft Edge
	- Wazuh Agent
	- Tailscale
	- Microsoft Edge Update
	- Outlook for Windows
### Process
94 total 
	- tailscaled.exe
	- tailscale-ipn.exe
	- wazuh-agent.exe
	- SecurityHealthSystray.exe
  - and alot of svchost.exe
### Users
8 - user.name
	- Administrator
	- DefaultAccount
	- Guest
	- Local Service
	- Network Service
	- System
	- WDAUtilityAccount
	- User

### Traffic

<img width="1863" height="584" alt="screenshot_20261122_005124-annotated" src="https://github.com/user-attachments/assets/df20b4fc-3f52-4010-8949-e55950bce404" />


### 617 - unique services
<img width="1871" height="278" alt="2026-11-22-001030_hyprshot" src="https://github.com/user-attachments/assets/809d40aa-668d-4de0-9bef-9ffcf4749bae" />


Note:
## 400 alert spike on initial enrollment — confirmed as Wazuh SCA baseline scan on default Windows 10 LTSC 2021.
