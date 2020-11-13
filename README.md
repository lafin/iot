### Smarthome ![actions](https://github.com/lafin/smarthome/workflows/actions/badge.svg)
___

### Nodered
![](assets/flow.png)

### Settings nodered's flow
[here](example/flow1.json)

### Sketch (temperature+humidity+relay)
[here](example/example1.ino)

### Result
<img src="assets/screen.png" height="400">

### x86_64 (armhf, arm64)
```bash
$ mkdir -p homebridge nodered && \
  curl -O https://raw.githubusercontent.com/lafin/smarthome/master/docker-compose.yml && \
  curl -O https://raw.githubusercontent.com/lafin/smarthome/master/docker-compose.x86_64.yml && \
  curl -o homebridge/config.json https://raw.githubusercontent.com/lafin/smarthome/master/homebridge/config/config.json
$ docker-compose -f docker-compose.x86_64.yml pull
$ docker-compose -f docker-compose.yml -f docker-compose.x86_64.yml up -d
```

### How to add grafana and influxdb? [look here](https://github.com/lafin/grafana-influxdb)
<img src="assets/grafana.png" height="300">

### Zigbee
https://www.zigbee2mqtt.io/getting_started/what_do_i_need.html

### Existed issues
- doesn't work on a Docker for MacOS [#issues/68](https://github.com/docker/for-mac/issues/68)