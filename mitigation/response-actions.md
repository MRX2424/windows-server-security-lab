# Mitigation and Response Actions

## Automated Mitigation
Account lockout policies successfully limited the effectiveness of the authentication attack.

- Repeated failed logons triggered account lockout
- Further login attempts were blocked automatically

## Verification
The locked account status was verified using PowerShell:
net user testuser

## Effectiveness
The mitigation prevented brute-force attacks without manual intervention and allowed the system to continue operating normally.
