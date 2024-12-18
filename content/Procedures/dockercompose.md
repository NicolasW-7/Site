#  Exemple de docker-compose.yml

```bash
version: '3.7'

services:
  vaultwarden:
    image: vaultwarden/server:latest
    container_name: vaultwarden
    restart: always
    environment:
      WEBSOCKET_ENABLED: true
      ADMIN_TOKEN: cf.Argon2section #YourAdminToken
      DOMAIN: "YourDomain" # Your domain; vaultwarden needs to know it's https to work properly with attachments
    volumes:
      - vw-data:/data

  caddy:
    image: caddy:2
    container_name: caddy
    restart: always
    ports:
      # Needed for the ACME HTTP-01 challenge.
      - 443:443
    volumes:
      - ./Caddyfile:/etc/caddy/Caddyfile:ro
      - ./ssl:/ssl
      - caddy-config:/config
      - caddy-data:/data
      - caddy-logs:/logs
    environment:
      - DOMAIN= # Your domain.
      #EMAIL: "YOUR EMAIL"                 # The email address to use for ACME registration.
      #LOG_FILE: "/data/access.log"

volumes:
  vw-data:
  caddy-config:
  caddy-data:
  caddy-logs:
  ```