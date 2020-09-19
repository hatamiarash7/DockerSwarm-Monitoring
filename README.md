# DockerSwarm Monitoring

Deploy monitoring service in Docker Swarm - Prometheus / Grafana / cAdvisor / Node Exporter / Alert Manager

## Prerequisites

- You need Traefik to access services. First install [Traefik for Docker Swarm](https://github.com/hatamiarash7/DockerSwarm-Traefik)

- To access external sources for prometheus there is multiple hosts in `extra_hosts` section. Change these values according to your needs.

## Install

Set your options :

- Traefik domains
- alert rules
- prometheus data sources

```shell
docker stack deploy -c docker-stack.yml Monitoring
```

Access Grafana : [http://grafana.localhost](http://grafana.localhost)  
Access Prometheus : [http://prometheus.localhost](http://prometheus.localhost)

## Extra sources

You can update or remove this sources

- [Docker Registry v2](https://docs.docker.com/registry)
- [PiHole](https://pi-hole.net)
  - Configure ENV data of PiHole server in `pihole/config` file
  - You should install piechart plugin : `grafana-cli plugins install grafana-piechart-panel`
  - You can use dashboard : `10176`
- [MinIO](https://min.io)
  - You can use [this dashboard](https://gist.github.com/hatamiarash7/d27f51c6c6e5ab97f3abdbacf03ae9c0)
- [Mikrotik](https://github.com/hatamiarash7/Mikrotik-Exporter)
  - You can use dashboard : `12055`
- [Traefik](https://github.com/hatamiarash7/Mikrotik-Exporter)
  - You can use dashboard : `11462`

---

## Support

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/D1D1WGU9)

<div><a href="https://payping.ir/@hatamiarash7"><img src="https://cdn.payping.ir/statics/Payping-logo/Trust/blue.svg" height="128" width="128"></a></div>

## Contributing

1. Fork it !
2. Create your feature branch : `git checkout -b my-new-feature`
3. Commit your changes : `git commit -am 'Add some feature'`
4. Push to the branch : `git push origin my-new-feature`
5. Submit a pull request :D

## Issues

Each project may have many problems. Contributing to the better development of this project by reporting them.
