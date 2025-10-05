# run
sudo docker compose up -d

# stop
sudo docker compose stop

# access on browser
open browser and access this url: http://localhost:5678/


# setup https locally
mkdir certs
openssl req -x509 -newkey rsa:4096 -sha256 -nodes \
  -keyout certs/selfsigned.key \
  -out certs/selfsigned.crt \
  -days 365 \
  -subj "/CN=localhost"

open browser and access this url: http://localhost:5678/
open browser and access this https url: https://localhost/setup