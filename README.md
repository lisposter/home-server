# home-server
A home media server build with docker-compose

# The folders config
```
docker_configs
├── transmission
├── qBitorrent
├── sonarr
├── ...

data
├── downloads
│  ├── movies
│  ├── music
│  └── tv
└── media
   ├── movies
   ├── music
   └── tv
```

* `docker_configs`: all of the configs for those docker services
* `data`: main folder
    * `downloads`: the main download target folder
    * `media`: hardlink folder for everything that doing media stuff

# Env Variables
* `PUID`: user id
* `GUID`: user group id
* `DOCKER_CONFIG`: the 
* `DATA`: the main data folder


# Usage
```sh
DOCKER_CONFIG=/path/to/config DATA=/path/to/data PUID="$(id -u)" GUID="$(id -g)" docker-compose up -d
```