# Security Hardening Checklist

1. Disable server signature and tokens:
   ServerSignature Off
   ServerTokens Prod

2. Disable directory listing where not needed:
   <Directory "C:/Apache24/htdocs">
       Options -Indexes
   </Directory>

3. Use HTTPS and redirect HTTP to HTTPS (301):
   # in vhost 80: Redirect permanent / https://site1.local/

4. Restrict access for admin paths using Allow/Deny or auth modules.

5. Keep Apache & Windows patched.

6. Remove unnecessary modules and services.

7. Protect cert/key files: restrict NTFS permissions to admin only.

8. Use firewall and limit management ports (RDP) to specific IPs if remote.
