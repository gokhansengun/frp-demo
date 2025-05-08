# Getting Started

## Prerequisites

Search for `192.168.25.144` in the repository and replace it with your server's IP address.

## Running frp server parts

```bash
# copy the files over to the server, then run the following commands
cd servers
docker compose up -d
```

## Running frp client parts

```bash
cd clients
docker compose up -d
```

## Test

Make a request to customer A's server endpoint and verify that the request is responded with the client A's app.

```bash
curl http://frp-demo.192.168.25.144.nip.io:3001
```

Make a request to customer B's server endpoint and verify that the request is responded with the client B's app.

```bash
curl http://frp-demo.192.168.25.144.nip.io:3002
```
