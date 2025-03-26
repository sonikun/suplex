# docker-compose.yml
```
  uptime-kuma:
    image: louislam/uptime-kuma:latest
    container_name: uptime-kuma
    volumes:
      - /root/docker/uptime-kuma:/app/data
    ports:
      - "3001:3001"  # <Host Port>:<Container Port>
    restart: always
```