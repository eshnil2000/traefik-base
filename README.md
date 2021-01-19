# traefik-base

### Localhost setup

* Install docker, and initialize docker swarm mode

```
docker swarm init
```

* modify /etc/hosts to add in subdomains you plan to use with Traefik
* In a cloud server deployment, use wildcard "A" record to map to your IP address
```
###Traefik
127.0.0.1       whoami.localhost
127.0.0.1       crypto.localhost
```
* Launch Traefik
```
docker stack deploy -c docker-compose.traefik-base.yml traefik
```

* Monitor dashboard at: 
- http://localhost:8080
