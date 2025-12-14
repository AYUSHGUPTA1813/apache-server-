# Identifying & Resolving Port Conflicts (80 / 443)

1. Find process using port:
   netstat -ano | findstr :80
   netstat -ano | findstr :443

2. Note PID and check process:
   tasklist /FI "PID eq <pid>"

3. Common culprits:
   - IIS (World Wide Web Publishing Service)
   - Skype (older versions)
   - SQL Server Reporting Services
   - VMware
   - Other web servers

4. To stop a service (temporary):
   net stop w3svc   (IIS)
   sc stop <serviceName>

5. To disable on boot (if safe):
   sc config <serviceName> start= disabled
