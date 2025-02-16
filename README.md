# Find-All-Devices-on-Your-Network

Discover all active devices on home network

1. Scanning the network 

Nmap
run a network scan to find all devices:
nmap -sn 192.168.1.1/24

- This will sends a ping to all devices in the subnet
- if some devices don't respond such as windows devices with a firewall use this command:
nmap -Pn 192.168.1.1/24

- this will forces Nmap to scan without checking if the host is online first

Netdiscover
   netdiscover -r 192.168.1.1/24

- this is useful if your on a Wi-Fi network and want to quickly find devices


2. Scan a specific device for open ports
once your indetified your laptop or the devices IP address scan for open ports

Basic Port Scan
nmap -sS -p- 192.168.1.100
- "sS" Stealth SYN scan (avoids detection by some firewalls)
- "-p-" = Scans all 65,535 ports

Detailed Service and OS Detection
  nmap -sV -O 192.168.1.100
- "-sV" = Detects running services and versions
- "-O" = Tries to determine the OS

  
