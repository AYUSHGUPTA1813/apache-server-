# Generate private key
openssl genrsa -out site1.key 2048

# Create CSR (you will be asked for details)
openssl req -new -key site1.key -out site1.csr

# Self-sign the certificate (valid 365 days)
openssl x509 -req -days 365 -in site1.csr -signkey site1.key -out site1.crt

# Verify certificate
openssl x509 -in site1.crt -text -noout
