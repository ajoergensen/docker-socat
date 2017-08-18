Simple socat container
======================

Listens on a port and forwards traffic to another host/port

#### Environment

These environment variable need to set

- `LOCAL_PORT` - The local port to listen to, remember to map the port from the host to the container
- `TARGET` - IP or DNS name of the target host
- `TARGET_PORT` - Port on target host to forward the traffic to
- `PROTO` - TCP or UDP, defaults to TCP

#### Usage

`docker pull ajoergensen/socat`

`docker run --name socat -e LOCAL_PORT=5000 -e TARGET=remotehost.lan -e TARGET_PORT=5000 -p 5000:5000 -d --rm ajoergensen/docker-socat`

