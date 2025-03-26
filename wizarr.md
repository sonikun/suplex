# docker-compose.yml
```
  wizarr:
    container_name: wizarr
    image: ghcr.io/wizarrrr/wizarr:latest
    #user: 1000:1000 #Optional but recommended, sets the user uid that Wizarr will run with
    ports:
      - 5690:5690
    volumes:
      - /root/docker/wizarr/config:/data/database
    environment:
      - APP_URL= #URL at which you will access and share 
      - DISABLE_BUILTIN_AUTH=false #Set to true ONLY if you are using another auth provider (Authelia, Authentik, etc)
      - TZ=Asia/Kolkata #Set your timezone here
```