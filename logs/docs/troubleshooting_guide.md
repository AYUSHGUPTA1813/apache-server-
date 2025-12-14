# Troubleshooting Guide (Common Issues)

## Apache won't start
- Check `error.log` for reasons.
- If port in use: `netstat -ano | findstr :80` -> stop conflicting service.
- Check `httpd.conf` for syntax errors: `httpd -t`

## 502 / Bad Gateway (when using proxy)
- Ensure backend (e.g., Node, Uvicorn) is running.
- Check proxy/passthru ports and firewall.

## SSL handshake errors
- Check cert & key pair match.
- Verify certificate path in vhost.

## Permission denied (403)
- Check NTFS permissions for DocumentRoot.
- Ensure `Require all granted` is present for directories.

## High memory usage
- Disable unnecessary modules.
- Check for large number of connections (DDoS possibility).
