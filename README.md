Installation

Create the project directory
```
mkdir -p ~/dev/docker/projects/traefik
```

Encode a Basic HTTP authentication user and password
```
traefik-dashboard-password stephane p...
```

Start the services
```
cd ~/dev/docker/projects/traefik;
docker stack deploy --compose-file docker-compose.yml traefik;
docker stack deploy --compose-file docker-compose-hw.yml traefik-hw
```

Stopping the common services
```
docker stack rm traefik-hw;
docker stack rm traefik
```

