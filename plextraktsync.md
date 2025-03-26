# docker-compose.yml
```
  plextraktsync:
    image: ghcr.io/taxel/plextraktsync:latest
    command: sync
    container_name: plextraktsync
    restart: always
    volumes:
      - /root/docker/plextraktsync:/app/config
    environment:
      - PUID=1000
      - PGID=1000
      - TZ=Asia/Kolkata
```
