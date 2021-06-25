Installation

Create the project directory
```
mkdir -p ~/dev/docker/projects/traefik
```

Add a hostname
Edit the /etc/hosts file
```
127.0.1.1 traefik.learnintouch.com
```

Encode a Basic HTTP authentication user and password
```
traefik-dashboard-password stephane p...
```

Viewing the dashboard
```
http://traefik.learnintouch.com/
```

Starting the services
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

