Execute this command to create selfsigned.crt and selfsigned.key
```bash
mkdir certs
openssl req -x509 -newkey rsa:4096 -sha256 -nodes \
  -keyout certs/selfsigned.key \
  -out certs/selfsigned.crt \
  -days 365 \
  -subj "/CN=localhost"
```