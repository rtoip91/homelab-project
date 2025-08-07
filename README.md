# Homelab Project

This repository contains Docker configurations for a homelab setup.

## Overview

This project uses Docker Compose to manage containerized services for a homelab environment.

## Prerequisites

- Docker
- Docker Compose

## Getting Started

1. Clone this repository
2. Make sure Docker and Docker Compose are installed on your system
3. Run the containers:

```bash
docker-compose up -d
```

## Project Structure

```
.
└── docker-compose.yaml    # Main Docker Compose configuration file
```

## Configuration

The project uses `docker-compose.yaml` to define and configure the services. A `.env` file is required to store environment variables for the services.

### Environment Variables

Create a `.env` file in the root directory with the following variables:

#### Traefik Configuration
```
TRAEFIK_LETSENCRYPT_EMAIL=your-email@domain.com
```

#### WireGuard Configuration
```
WG_HOST=your-wireguard-host
WG_PASSWORD=your-wireguard-password
WG_TZ=your-timezone
```

#### AdGuard Home Configuration
```
ADGUARD_DNS_HOST=your-dns-host
ADGUARD_ADMIN_HOST=your-admin-panel-host
```

#### Jellyfin Configuration
```
JELLYFIN_HOST=your-jellyfin-host
```

#### Gluetun VPN Configuration
```
VPN_SERVICE_PROVIDER=your-vpn-provider
VPN_TYPE=wireguard
WIREGUARD_PUBLIC_KEY=your-public-key
WIREGUARD_PRIVATE_KEY=your-private-key
WIREGUARD_ADDRESSES=your-wireguard-addresses
WIREGUARD_ENDPOINT_IP=your-endpoint-ip
WIREGUARD_ENDPOINT_PORT=your-endpoint-port
VPN_DNS_ADDRESS=your-dns-address
VPN_PORT_FORWARDING=on/off
VPN_PORT_FORWARDING_PROVIDER=your-provider
GLUETUN_TZ=your-timezone
UPDATER_PERIOD=24h
JELLYSEERR_HOST=your-jellyseerr-host
```

Make sure to replace all placeholder values with your actual configuration details. Keep this file secure as it contains sensitive information.

## Maintenance

To update the containers:

```bash
docker-compose pull
docker-compose up -d
```

To stop all services:

```bash
docker-compose down
```

## License

This project is open source and available under the MIT License.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
