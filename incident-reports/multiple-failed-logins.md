## Incident Title
Multiple Failed Windows Logins

## Incident Summary
Multiple failed login attempts were detected on a Windows 11 endpoint. The activity triggered an Elastic Security detection rule for repeated Windows Event ID 4625 failed logons.

## Incident Details

- Host: Windows 11 endpoint
- User: Local Windows user
- Event ID: 4625
- Source IP: 127.0.0.1
- Logon Type: 2 (Interactive)
- Failure Reason: Bad password
- Detection Rule: Windows Multiple Failed Login Detection
- Detection Threshold: 3 events
- Detected Count: 4 events
- Severity: Low
- Risk Score: 30
- Status: Resolved

## Investigation

The Windows Security logs showed multiple failed authentication attempts for the local user account.

The source IP was 127.0.0.1, indicating that the activity originated from the local Windows machine.

The failed login attempts were intentionally generated as part of a controlled SOC lab simulation.

## Response

1. Reviewed Windows Event ID 4625 events.
2. Verified the affected user and endpoint.
3. Checked the source IP address.
4. Investigated the Elastic Security alert.
5. Confirmed that the threshold rule detected 4 failed logons.
6. Successfully logged in using the correct password.
7. Confirmed there was no evidence of remote compromise.

## Conclusion

The alert was successfully detected and investigated. The activity was a controlled simulation and was not a confirmed real-world attack.

## MITRE ATT&CK Mapping

- T1110 — Brute Force
- T1110.001 — Password Guessing

This mapping represents the simulated detection scenario and does not confirm adversary activity.

## Lessons Learned

This lab demonstrated the complete SOC detection workflow:

Windows Event Logs → Elastic Agent → Elastic Security → Detection Rule → Alert → Investigation → Incident Report
