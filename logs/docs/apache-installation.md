# Apache Installation on Windows (2.4.x)

1. Download Apache Windows binary (Apache Lounge recommended).
2. Install Visual C++ Redistributable (matching Apache build).
3. Extract Apache to `C:\Apache24`.
4. Open elevated command prompt:
   - Install as service: `httpd -k install`
   - Start service: `httpd -k start` or `net start Apache24`
5. Verify `http://localhost` loads.
6. Add `C:\Apache24\bin` to PATH for convenience.
7. Configure `httpd.conf` to include `conf/vhosts/*.conf`:
   - Add: `Include conf/vhosts/*.conf`
