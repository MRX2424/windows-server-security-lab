# Detection and Log Analysis

## Log Collection Method
Windows Security Event Logs were analyzed using PowerShell.

Command used:
Get-WinEvent -LogName Security -MaxEvents 20

## Detected Events

### Failed Authentication (Attack)
- Event ID: 4625
- Description: An account failed to log on
- Source IP: Kali Linux machine
- Indicator: Malicious authentication attempt

### Account Lockout
- Event ID: 4740
- Description: A user account was locked out
- Indicator: Automated security control triggered

### Successful Authentication (Authorized)
- Event ID: 4624
- Description: An account was successfully logged on
- Indicator: Legitimate access

## Conclusion
Windows Security logs clearly distinguish between malicious activity and authorized user behavior.
