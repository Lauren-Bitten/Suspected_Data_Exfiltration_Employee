📌 What Happened?
With the file archiving confirmed, the next step was to trace potential exfiltration attempts. The focus was on network logs, looking for suspicious outbound connections or uploads to external locations.

🔍 Key Findings
🌐 No immediate outbound network transfers detected.
☁️ No evidence of cloud uploads (OneDrive, Google Drive, Dropbox).
🔍 Logs reviewed for FTP, SSH, and external IP connections.
🛡️ Defensive Measures
Implement egress filtering to block unauthorized external connections.
Set up alerts for large data transfers or unexpected outbound activity (DeviceNetworkEvents).
Use Defender for Cloud Apps to detect unusual cloud activity.
