# docker-compose.yml
```
  sonarr:
    image: lscr.io/linuxserver/sonarr:develop
    container_name: sonarr
    environment:
      - PUID=1000
      - PGID=1000
#      - DOCKER_MODS=ghcr.io/themepark-dev/theme.park:sonarr  
#      - TP_THEME = hotpink
    volumes:
      - /root/docker/sonarr:/config
      - /home/ubuntu/YeetersShows:/media/gdrive/
      - /home/ubuntu/Onedrive/Plex:/media/onedrive/
    ports:
      - 8989:8989
    restart: unless-stopped
```

# Formats
### Series Folder Format
```
{Series TitleYear} {tvdb-{TvdbId}}
```

### Season Folder Format
```
Season {season:00}
```
### Specials Folder Format
```
Specials
```

### Standard Episode Format
```
{Series TitleYear} - S{season:00}E{episode:00} - {Episode CleanTitle} [{WEBrip}{Quality Full}]{[MediaInfo VideoDynamicRangeType]}{[Mediainfo AudioCodec}{ Mediainfo AudioChannels]}{[MediaInfo VideoCodec]}{-Release Group}
```

### Daily Episode Format
```
{Series TitleYear} - {Air-Date} - {Episode CleanTitle} [{Custom Formats }{Quality Full}]{[MediaInfo VideoDynamicRangeType]}{[Mediainfo AudioCodec}{ Mediainfo AudioChannels]}{[MediaInfo VideoCodec]}{-Release Group}
```

### Anime Episode Format
```
{Series TitleYear} - S{season:00}E{episode:00} - {absolute:000} - {Episode CleanTitle} [{Custom Formats }{Quality Full}]{[MediaInfo VideoDynamicRangeType]}[{MediaInfo VideoBitDepth}bit]{[MediaInfo VideoCodec]}[{Mediainfo AudioCodec} { Mediainfo AudioChannels}]{MediaInfo AudioLanguages}{-Release Group}
```
