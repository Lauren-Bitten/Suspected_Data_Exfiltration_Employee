Summary of Investigation

A suspected data exfiltration attempt was investigated involving the unauthorized archiving of employee data using PowerShell and 7-Zip. The incident involved recurring PowerShell script execution, file archiving, and potential exfiltration attempts. However, no immediate signs of data exfiltration were observed. The investigation focused on PowerShell execution logs, file system activity, and network traffic analysis using Microsoft Defender for Endpoint (MDE).

Scenarios of What Took Place

Scenario 1: Unauthorized File Archiving

PowerShell script executed silently.

7-Zip was installed without authorization.

Employee data was compressed into a ZIP file.

Archives were stored in a "backup" folder.

Scenario 2: Hunting for Exfiltration Evidence

Investigated network logs for outbound transfers.

No immediate network exfiltration detected.

Logs reviewed for uploads to cloud services or external destinations.

Scenario 3: Incident Response & Containment

System was immediately isolated upon discovering the archiving.

Management was notified of PowerShell-based file compression.

No signs of data leaving the network, but monitoring remains ongoing.

MITRE ATT&CK Framework TTPs

Execution

T1059.001 – Command and Scripting Interpreter: PowerShell

Used for silent installation and execution.

Persistence

T1547.001 – Boot or Logon Autostart Execution

Possible script persistence via registry keys or scheduled tasks.

Defense Evasion

T1564.004 – Hide Artifacts: NTFS File Attributes

ZIP files may have been hidden or misleadingly named.

Collection

T1560.001 – Archive Collected Data: Archive via Utility

7-Zip was used to compress sensitive data.

Exfiltration (Potential Risk)

T1048 – Exfiltration Over Alternative Protocol

No exfiltration detected, but remains a concern.

T1567 – Exfiltration Over Web

Possible cloud service or external transfers need further monitoring.

Next Steps & Recommendations

✔ Restrict PowerShell Execution: Implement Constrained Language Mode & Script Block Logging.
✔ Enforce Application Control: Use AppLocker/WDAC to block unauthorized tools like 7-Zip.
✔ Deploy DLP Policies: Prevent unauthorized access to sensitive employee data.
✔ Monitor Network Activity: Set up egress filtering in Defender for Endpoint & Defender for Cloud Apps.
✔ Refine Advanced Hunting Queries: Automate real-time alerts for suspicious file archiving & PowerShell execution.
✔ Conduct Regular Threat Hunts: Improve incident response workflows in Sentinel & Defender for XDR.

🚀 Continuous monitoring and security enhancements are required to prevent future unauthorized data access and exfiltration attempts.

