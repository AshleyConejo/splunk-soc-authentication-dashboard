Splunk SOC Authentication Monitoring Dashboard
<img width="1280" height="677" alt="dashboard1" src="https://github.com/user-attachments/assets/3d83472d-dbba-46aa-a761-34feb54591af" />
<img width="1271" height="676" alt="dashboard 2" src="https://github.com/user-attachments/assets/d43f6ba8-faed-4c20-9f6c-3d29672ac482" />

Project Overview:
This project is an isolated SOC lab that collects and analyzes
Windows authentication events using Splunk Enterprise.

Architecture:
<img width="1672" height="941" alt="Topology Diagram" src="https://github.com/user-attachments/assets/88542382-9dec-4237-a390-74c3719d73b6" />

- Windows 11 monitored endpoint
- Splunk Universal Forwarder
- Ubuntu Splunk Enterprise server
- TCP 9997 forwarding
- Splunk Dashboard Studio

Monitored Events:

- Event ID 4624: Successful login
- Event ID 4625: Failed login

Features:

- Successful login monitoring
- Failed login monitoring
- Brute-force detection
- Password-spraying detection
- Successful login following repeated failures
- Scheduled alerts
- Interactive dashboard

Technologies:

- Splunk Enterprise
- Splunk Universal Forwarder
- Splunk Add-on for Microsoft Windows
- Windows 11
- Ubuntu Server
- Oracle VirtualBox
- SPL

Detection Logic:

Possible brute force is defined as five or more failed login
attempts against the same account during a five-minute period.

MITRE ATT&CK Mapping:

- T1110: Brute Force
- T1110.001: Password Guessing
- T1110.003: Password Spraying

Testing:

All detection testing was performed against a dedicated local
account inside an isolated Windows virtual machine.

Limitations:

This is an educational Splunk Enterprise lab. It is not a production Splunk Enterprise Security deployment.



