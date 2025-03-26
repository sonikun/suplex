# docker-compose.yml
```
  overseerr:
    image: sctx/overseerr:latest
    container_name: overseerr
    environment:
      - LOG_LEVEL=debug
      - PORT=5055 #optional
    ports:
      - 5055:5055
    volumes:
      - /root/docker/overseerr:/config
    restart: unless-stopped
    networks:
      my_network:
        ipv4_address: 
```