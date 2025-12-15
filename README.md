# IT Support Troubleshooting Lab

This repository documents hands-on IT support troubleshooting scenarios,
focused on real-world desktop and network issues.

The goal is to demonstrate:
- Logical troubleshooting methodology
- Understanding of Windows networking fundamentals
- Clear documentation of problems, diagnosis, and resolution

All scenarios are written from an IT Support / Helpdesk perspective.

# Case 1: No Internet Connection (Wi-Fi)

Problem

User reports that their laptop is connected to Wi-Fi but has no internet access.

⸻

Initial Checks
	1.	Checked the network icon in the system tray to confirm Wi-Fi connection.
	2.	Verified that the device is connected to the correct Wi-Fi network.
	3.	Opened Command Prompt to inspect network configuration.
You sent
Diagnosis
You sent
•	Ran:
You sent
ipconfig
You sent
•	Observed that the device had an APIPA address (169.254.x.x).
	•	This indicates that the computer did not receive an IP address from DHCP.
	•	Confirmed that without a valid IP, the device cannot reach the default gateway or the internet.

⸻

Troubleshooting Steps
	1.	Attempted to renew the IP configuration:
You sent
ipconfig /release
ipconfig /renew
You sent
2.	After renewal, verified that the device received:
	•	A valid IP address
	•	A default gateway
	•	DNS server information
	3.	Tested connectivity:
You sent
Resolution
	•	The issue was caused by a failure to obtain an IP address from the DHCP server.
	•	Renewing the IP configuration successfully restored network connectivity.

⸻

What I Learned
	•	How to identify DHCP-related issues using ipconfig
	•	The meaning and impact of APIPA addresses
	•	A structured approach to troubleshooting Wi-Fi connectivity issues
	•	The importance of validating IP, gateway, and DNS before deeper troubleshooting
