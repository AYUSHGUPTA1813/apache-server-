# Backup & Recovery Strategy

1. Backup list:
   - `C:\Apache24\conf\vhosts\` (vhost files)
   - `C:\Apache24\htdocs\` (website files)
   - `C:\Apache24\certs\` (certificates)
   - Windows hosts file

2. Backup methods:
   - Zip the directories daily and copy to external drive or cloud (OneDrive / Google Drive).
   - Use scheduled task to run backup script (PowerShell or batch).

3. Restore:
   - Stop Apache: `net stop Apache24`
   - Replace directories
   - Start Apache: `net start Apache24`

4. Test restore monthly on a separate machine / VM.
