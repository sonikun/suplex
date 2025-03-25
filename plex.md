# docker-compose.yml
```
  plex:
    container_name: plex
    image: linuxserver/plex
    ports:
      - 32400:32400
    environment:
      - VERSION=docker
      - PLEX_CLAIM= #optional
      - PLEX_UID=1000
      - PLEX_GID=1000
      - TZ=Asia/Kolkata
    volumes:
      - /root/docker/plex:/config
      - /root/docker/plex/transcode:/transcode
      - /home/ubuntu/YeetersShows:/media/gdrive/
      - /home/ubuntu/Onedrive/Plex:/media/onedrive/
    restart: unless-stopped
    networks:
      my_network:
        ipv4_address:
```

# updating plex server
- open container in portainer,
- at top-right, beside duplicate, use 'recreate' and turn on 'repull image'.

or
- `cd` to where docker-compose.yml is located,
```
$ cd /root/docker/docker-compose
```
- run the followings
```
$ docker-compose pull plex
```
```
$ docker-compose up -d plex
```
