# dockerTIG

## Requirements

- Linux host
- Docker installed
  - `sudo apt install docker.io`
- Add user to docker group
  - `sudo usermod -aG docker $USER`
  - Restart connection to terminal
- Docker-compose installed
  - `sudo curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`
  - `sudo chmod +x /usr/local/bin/docker-compose`

## Instructions

- Clone the repo or copy 3 files into the same directory on a Linux host.
- Search for "ENTER_INFLUXDB_IP_HERE" in telegraf.conf and edit accordingly. Cannot be localhost or loopback.
- In that directory, run `docker-compose up`
- Visit the host IP at port 3000
- Default login credentails are `admin` and `password`.
- Add data source
- Select InfluxDB
- Set URL = `http://ENTER_HOST_IP_HERE:8086`
- InfluxDB Details:
  - Database = `telegraf`
  - User = `telegraf`
  - Password = `password`
- Save & Test
- Create Dashboards
  - Check out [dashboard 3967](https://grafana.com/grafana/dashboards/3967)
