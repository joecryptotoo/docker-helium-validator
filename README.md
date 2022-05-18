# docker-helium-validator

docker-compose.yml file for running a helium validator

## Getting started

Use dig to discover your public ip address and store it in the NAT_EXTERNAL_IP environment variable
```
sudo apt install dig
export NAT_EXTERNAL_IP=$(dig +short myip.opendns.com @resolver1.opendns.com)
```

Start the container using docker-compose
```
docker-compose up -d
```

To upgrade run:
```
docker-compose pull validator && docker-compose up -d validator
```
* This could be automated with a cron job.

Forward port 2154/tcp and 8080/tcp to your docker server

## Diagnostics commands

```
docker exec validator miner info summary
docker exec validator miner info height
docker exec validator miner peer listen
docker exec validator miner peer book -s
docker exec validator miner peer gossip_peers
docker exec validator miner peer session
docker exec validator miner info p2p_status
```
