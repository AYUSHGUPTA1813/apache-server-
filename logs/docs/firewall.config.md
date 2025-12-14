# Windows Firewall Configuration for Apache

1. Open Windows Defender Firewall -> Advanced Settings.
2. Create a new Inbound Rule:
   - Rule Type: Port
   - Protocol: TCP
   - Ports: 80, 443
   - Action: Allow the connection
   - Profile: Domain, Private, Public (as required)
   - Name: Apache HTTP/HTTPS

3. Alternatively use netsh (admin):
   netsh advfirewall firewall add rule name="Apache HTTP" dir=in action=allow protocol=TCP localport=80
   netsh advfirewall firewall add rule name="Apache HTTPS" dir=in action=allow protocol=TCP localport=443

4. Allow Apache executable in firewall:
   netsh advfirewall firewall add rule name="Apache Service" dir=in action=allow program="C:\Apache24\bin\httpd.exe" enable=yes
