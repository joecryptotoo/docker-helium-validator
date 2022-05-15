# docker-helium-validator

docker-compose.yml file for running a helium validator

To get started run:

```
NAT_EXTERNAL_IP=$(dig +short myip.opendns.com @resolver1.opendns.com) docker-compose up -d
```

To upgrade run:
```
NAT_EXTERNAL_IP=$(dig +short myip.opendns.com @resolver1.opendns.com) docker-compose pull validator
NAT_EXTERNAL_IP=$(dig +short myip.opendns.com @resolver1.opendns.com) docker-compose up -d validator
```
