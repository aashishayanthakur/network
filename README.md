This project outlines a structured workflow for performing a basic network discovery and security audit using Nmap and Wireshark. The focus is on identifying active devices, open ports, and potential security risks within a local IP range.

**📋 Project WorkflowInstallation:**
Download Nmap from the official website.Network Identification: Determine your local IP range .Scanning: Execute a TCP SYN scan (-sS) to identify open ports.Data Collection: Document discovered IP addresses and their corresponding open ports.Traffic Analysis: Use Wireshark to capture and analyze packet-level interactions.Service Research: Investigate the common services associated with the discovered ports.Risk Assessment: Identify potential security vulnerabilities based on open services.Reporting: Export and save scan results in text or HTML format.

**🛠️ Technical Details**
EnvironmentTarget Device: Local Gateway (192.168.1.1).Scanner OS: Windows 11 (25H2), Tools: Dumpcap (Wireshark) 4.6.3.Scan Methodology: TCP SYN ScanThe project utilizes the -sS flag in Nmap, known as a "half-open" or "stealth" scan. It works by sending a SYN packet and observing the response without completing the three-way handshake.Open Port: Target responds with SYN/ACK.Closed Port: Target responds with RST/ACK.

**🔍 Audit Results**
Based on the initial packet capture analysis of the target ////////:PortServiceStatusObservations53Domain (DNS)OpenResponded to SYN request.80HTTPOpenWeb management interface detected.443HTTPSOpenSecure web management detected.22SSHClosedPort rejected connection.23TelnetClosedPort rejected connection.

**🚀 How to  perform** 
run a scan similar to the one in this project, use the following command (requires administrative privileges):Bashnmap -sS -oA audit_report [YOUR_LOCAL_RANGE]RunTo
