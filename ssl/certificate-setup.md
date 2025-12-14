# SSL Certificate Setup (Windows + Apache)

1. Generate key and CSR using OpenSSL (see openssl-commands.txt).
2. Place `site1.key` and `site1.crt` in `C:\Apache24\certs\`.
3. Update vhost HTTPS block to point to certificate and key.
4. Ensure `mod_ssl` or `mod_socache_shmcb` modules are enabled (Apache Windows build has modules precompiled).
5. Restart Apache: `net stop Apache24 && net start Apache24`.
6. Test https://site1.local in browser (you may need to accept self-signed cert).
