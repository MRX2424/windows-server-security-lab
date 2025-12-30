# Attack Simulation

## Attack Scenario
A Kali Linux machine was used to simulate unauthorized authentication attempts against a hardened Windows Server.

## Reconnaissance
The target was scanned using nmap to identify exposed services.

Command used:
nmap -Pn <Windows_Server_IP>

Result:
- Most ports filtered
- WinRM service (TCP 5985) exposed

## Attack Method
Authentication attempts were made against WinRM using invalid credentials.

Command used:
evil-winrm -i <Windows_Server_IP> -u testuser -p WrongPassword123

## Outcome
- Authentication failed as expected
- No unauthorized access was gained
- Security events were generated on the Windows Server
