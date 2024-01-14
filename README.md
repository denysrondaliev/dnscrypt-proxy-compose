# A docker compose for DNSCrypt proxy

## Dependencies

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose plugin](https://docs.docker.com/compose/install/linux/)

## Installation

```bash
git clone https://github.com/denysrondaliev/dnscrypt-proxy-compose.git
cd dnscrypt-proxy-compose
chmod 644 dnscrypt-proxy.toml
docker compose up -d
```

## Testing

```bash
DNSCRYPT_PROXY_IP=$(docker inspect dnscrypt-proxy | jq -r ".[] | .NetworkSettings | .Networks | .[] | .IPAddress")
host google.com $DNSCRYPT_PROXY_IP
```

## Uses the following Docker containers

- https://github.com/klutchell/dnscrypt-proxy

## 📝 License

This project is licensed under the [GPL-3.0](LICENSE)..
