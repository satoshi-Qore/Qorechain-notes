# Light Node Troubleshooting

Community troubleshooting notes for QoreChain light node operators.

## Basic Checks

### Check running containers

```bash
docker ps
```

Confirm that the expected light node services are running.

### Check logs

```bash
docker logs qorechain-lightnode-sx
```

Use logs to identify startup errors, connection issues, or repeated restarts.

### Restart services

```bash
docker compose restart
```

Restarting can help after configuration changes or temporary network issues.

## Common Issues

### Docker service is not running

Check whether Docker is installed and active:

```bash
sudo systemctl status docker
```

If needed, start Docker:

```bash
sudo systemctl start docker
```

### Dashboard is not reachable

Check that the service is running and confirm the server firewall allows access to the dashboard port.

Example dashboard URL:

```text
http://YOUR_SERVER_IP:8420
```

### Node keeps restarting

Review logs carefully and check:

- Missing environment variables
- Incorrect Docker Compose configuration
- Low server resources
- Network or RPC connectivity problems

## Operator Notes

Keep a record of:

- VPS provider and server size
- Install date
- Docker version
- Error messages
- Fixes that worked

## Disclaimer

These are community-maintained notes and may change as QoreChain evolves.
