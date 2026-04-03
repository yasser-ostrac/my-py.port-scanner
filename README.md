# my-py.port-scanner
my first port scanner python based
Python Port Scanner with Security Alerts

A lightweight network security tool developed in Python to scan ports on a specified host. Designed and tested in a Kali Linux environment.

🔍 Features
- Scans ports in the range 1–1024
- Identifies open and closed ports
- Flags insecure or risky services:
  - FTP (unencrypted)  
  - Telnet (insecure)  
  - SMTP (can be abused)  
  - SMB (file sharing vulnerabilities)
- Implements multithreading for faster scanning
- Provides clear console output with visual indicators (✅, ❌, ⚠️)

🎯 Purpose
This project demonstrates fundamental cybersecurity concepts in network reconnaissance and defensive awareness.  
Port scanning is a critical step in penetration testing and vulnerability assessment, helping identify exposed services that may pose security risks.

⚙️ Requirements
- Python 3.x  
- Kali Linux (or any Linux/Unix environment)  
- No external libraries required (uses built-in socket and threading)

🚀 Usage
Clone the repository and run:
`bash
python3 portscanner.py
`

To test functionality, enable a service (e.g., SSH):
`bash
sudo systemctl start ssh
`
Port 22 will then appear as OPEN in the scan results.

📊 Example Output
`
Scanning 127.0.0.1 for ports 1–1024...

❌ Port 21 is CLOSED on 127.0.0.1
✅ Port 22 is OPEN on 127.0.0.1
❌ Port 23 is CLOSED on 127.0.0.1
⚠️ Port 445 OPEN — SMB (file sharing vulnerabilities)
`

📌 Future Improvements
- Save results to a log file with timestamps  
- Banner grabbing to identify running services  
- Command-line arguments for host and port range  
- Export results to CSV/JSON for reporting  
-
