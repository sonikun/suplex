# docker-compose.yml
```
  portainer:
    image: portainer/portainer-ce:latest
    container_name: portainer
    networks:
      my_network:
        ipv4_address: 
    restart: unless-stopped
    volumes:
      - /root/docker/portainer:/data
      - /var/run/docker.sock:/var/run/docker.sock
    ports:
      - '9000:9000'
```
