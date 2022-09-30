# A docker compose for DNSCrypt proxy

## Dependencies

- docker
- docker compose

## Installation

```bash
git clone https://github.com/unleftie/dnscrypt-proxy-docker.git
cd dnscrypt-proxy-docker
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

This project is licensed under the [MIT](LICENSE.md).
