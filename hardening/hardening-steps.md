# Windows Server Hardening Steps

## Account and Password Policies
- Enforced minimum password length of 10 characters
- Enabled password complexity requirements
- Configured account lockout after multiple failed login attempts

## Firewall Configuration
- Verified Windows Defender Firewall is enabled for:
  - Domain profile
  - Private profile
  - Public profile

PowerShell command used:
Get-NetFirewallProfile | Select Name, Enabled

## Security Auditing
- Enabled auditing for logon success and failure events

PowerShell commands:
auditpol /set /subcategory:"Logon" /success:enable /failure:enable
auditpol /get /subcategory:"Logon"

## Result
The server was configured to log authentication activity and restrict unauthorized access attempts.
