# docker-compose.yml
```
  jellyfin:
    image: jellyfin/jellyfin:latest
    container_name: jellyfin
    networks:
      my_network:
        ipv4_address:
    volumes:
      - /root/docker/jellyfin:/config
      - /root/docker/jellyfin/cache:/cache
      - /home/ubuntu/YeetersShows:/media/gdrive/
      - /home/ubuntu/Onedrive/Plex:/media/onedrive/
    ports:
      - '8096:8096/tcp'
    restart: unless-stopped
    # Optional - alternative address used for autodiscovery
    environment:
      - JELLYFIN_PublishedServerUrl=http://example.com
    # Optional - may be necessary for docker healthcheck to pass if running in host network mode
    extra_hosts:
      - "host.docker.internal:host-gateway"
```
