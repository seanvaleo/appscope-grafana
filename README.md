# AppScope -> Grafana

This project provides a starting point for visualizing data from AppScope in a Grafana Dashboard.

### System Design

AppScope -> Cribl Edge -> InfluxDB <- Grafana

### Requirements

- Docker
- Docker Compose

### Usage

Start:
```
docker-compose up -d
```

Stop:
```
docker-compose down
```

### Using AppScope

Run AppScope from the host, if installed:
```
scope run -c edge -- <some_command>
```

Run AppScope from the included container:
```
docker ps # Find AppScope container ID
docker exec -it <container_id> /bin/bash
scope run -c edge -- <some_command>
```
