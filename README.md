# dockerTIG

## Requirements

- linux host
- docker installed
  - `sudo apt install docker.io`
- docker-compose installed
  - `sudo curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`
  - `sudo chmod +x /usr/local/bin/docker-compose`

## Instructions

- Clone the repo or copy 3 files into the same directory on a Linux host.
- Search for "ENTER_INFLUXDB_IP_HERE" in telegraf.conf and edit accordingly. Cannot be localhost or loopback.
- In that directory, run `docker-compose up`
- Visit the host IP at port 3000
- Default login credentails are `admin` and `password`.
