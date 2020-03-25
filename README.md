# DockerSwarm Monitoring
 Deploy monitoring service in Docker Swarm - Prometheus / Grafana / cAdvisor / Node Exporter / Alert Manager

### Install

Set your options :
* traefik domains
* alert rules
* prometheus data sources

```shell
docker stack deploy -c docker-stack.yml monitoring
```

Access Grafana : [http://grafana.localhost](http://grafana.localhost)  
Access Prometheus : [http://prometheus.localhost](http://prometheus.localhost)
