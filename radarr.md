# docker-compose.yml
```
  radarr:
    image: lscr.io/linuxserver/radarr:latest
    container_name: radarr
    environment:
      - PUID=1000
      - PGID=1000
    volumes:
      - /root/docker/radarr:/config
      - /home/ubuntu/Onedrive/Plex:/media/onedrive/
      - /home/ubuntu/YeetersShows:/media/gdrive/
    ports:
      - 7878:7878
    networks:
      my_network:
        ipv4_address: 
    restart: unless-stopped
```

# Format
- Standard Movie Format
```
{Movie CleanTitle} {(Release Year)} {imdb-{ImdbId}} {edition-{Edition Tags}} {[Quality Full]}{[MediaInfo 3D]}{[MediaInfo VideoDynamicRangeType]}{[Mediainfo AudioCodec}{ Mediainfo AudioChannels]}[{Mediainfo VideoCodec}]{-Release Group}
```

- Movie Folder Format
```
{Movie Title} ({Release Year}) {tmdb-{TMdbid}}
```
