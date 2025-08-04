# Network Port Scanning Task (Kali Linux)

## Tools Used
- Nmap
- Wireshark (optional)

## Steps Performed
1. Found local IP range using `ip a`
2. Performed TCP SYN scan using Nmap
3. Saved results as text and HTML
4. Analyzed services running on open ports
5. Identified potential risks

## Key Findings
- Device 192.168.1.41/24 → Open ports: 80, 443 (Web services)
- Device 192.168.1.1 → Open ports: 21 (SSH)

## Files Included
- `scan_result.txt`
- `wireshark_result.pcapng`
- Screenshots

## Interview Questions (with answers)
1. **What is an open port?**  
   An open port is a network port that is accepting incoming connections. It indicates that a service or application is actively listening on that port, making it accessible to other devices or users.

2. **How does Nmap perform a TCP SYN scan?**  
   Nmap sends a TCP SYN packet to a target port. If it receives a SYN-ACK response, the port is considered open. It then sends a RST (reset) packet to avoid completing the handshake, making it a stealthy and fast scanning technique.

3. **What risks are associated with open ports?**  
   Open ports can expose services that may have vulnerabilities. Attackers can exploit these services to gain unauthorized access, execute commands, or steal data. Unused or insecure ports increase the attack surface of a device.

4. **Explain the difference between TCP and UDP scanning.**  
   TCP scanning checks ports by initiating a three-way handshake. It's reliable because it confirms whether a service is accepting connections.
   UDP scanning is less reliable and slower. It sends empty UDP packets to a port and waits for a response or timeout. UDP services don't always respond, making results harder to interpret.

5. **How can open ports be secured?**  
   Close unused ports
   Use firewalls to restrict access
   Enable encryption and authentication on services
   Regularly update and patch exposed services

6. **What is a firewall's role regarding ports?**  
   A firewall monitors and controls incoming and outgoing network traffic. It allows or blocks ports based on security rules, preventing unauthorized access and protecting the system from port-based attacks.

7. **What is a port scan and why do attackers perform it?**  
   A port scan is a technique to discover open ports and services on a networked device. Attackers use it to map the target system and find vulnerabilities. Ethical hackers also use it to test network security.

8. **How does Wireshark complement port scanning?**  
   Wireshark captures and analyzes network packets in real time. While Nmap reveals open ports, Wireshark helps visualize how the scan works, monitor responses, detect suspicious activity, and better understand network behavior during a scan.
...




nmap-local-network-scan/
├── scan_result.txt            # Raw Nmap output in text format 
├── screenshots/               # Folder containing screenshots 
│   ├── nmap-scan.png
│   └── nmap-scann.png
├── README.md                  # Explanation of what you did
└── wireshark-capture.pcapng   # Saved Wireshark capture file
