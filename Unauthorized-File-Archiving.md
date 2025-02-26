📌 What Happened?
A routine file integrity check uncovered suspicious PowerShell activity, silently installing 7-Zip and archiving sensitive employee data. These archives were stored in a "backup" folder, hinting at possible data staging before exfiltration.

🔍 Key Findings
🛑 PowerShell script executed without user interaction.
🔧 Unauthorized installation of 7-Zip.
🗂️ Employee data compressed into ZIP archives.
📂 Archives stored in a non-standard backup location.
🛡️ Defensive Measures
Monitor for unauthorized PowerShell executions (DeviceProcessEvents).
Alert on ZIP file creation within critical directories (DeviceFileEvents).
Restrict unapproved software installations using AppLocker/WDAC.
