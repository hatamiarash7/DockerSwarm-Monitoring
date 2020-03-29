# DockerSwarm Monitoring
 Deploy monitoring service in Docker Swarm - Prometheus / Grafana / cAdvisor / Node Exporter / Alert Manager

### Install

Set your options :
* traefik domains
* alert rules
* prometheus data sources

```shell
docker stack deploy -c docker-stack.yml Monitoring
```

Access Grafana : [http://grafana.localhost](http://grafana.localhost)  
Access Prometheus : [http://prometheus.localhost](http://prometheus.localhost)

### Extra sources

You can update or remove this sources

* [Docker Registry v2](https://docs.docker.com/registry)
  * Set your registry address in `docker-registry` job
* [PiHole](https://pi-hole.net)
  * Configure ENV data of PiHole server in `pihole/config` file
  * You can use dashboard id : `10176`
