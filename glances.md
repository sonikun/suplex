# docker-compose.yml
```
  glances:
    container_name: glances
    image: nicolargo/glances:latest
    restart: always
    pid: host
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock
    environment:
      - "GLANCES_OPT=-w"
    ports:
      - 61208:61208
    labels:
      - "traefik.port=61208"
      - "traefik.frontend.rule=Host:glances.docker.localhost"
```